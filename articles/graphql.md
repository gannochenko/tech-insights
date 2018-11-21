# GraphQL

Commonly used as an additional layer of abstraction above different data sources, including REST, SOAP and other, in order to provide an ability to nest entities and grab sub-trees of data structure.

Examples of declarations:<br />

Types:
~~~~
type Book {
    title: String,
    author: Author,
}

type Author {
    name: String,
    books: [Book],
}

type Query {
    author(id: String!): Author
}
~~~~

For each type except the built-in ones (like `String`) we need to write a resolver:
~~~~
const { find, filter } = require('lodash');

const authors = [...];
const books = [...];

module.exports = {
    Query: {
        author(parent, args, context, info) {
            return find(authors, {id: args.id});
        }
    },
    Author: {
        books(author) {
            return filter(books, {author: author.name});
        }
    },
};
~~~~

Then we call the query like this:
~~~~
query {
    author(id: "5") {
        name
        books {
            title
            author {
                name # the same as name above
            }
        }
    }
}
~~~~
