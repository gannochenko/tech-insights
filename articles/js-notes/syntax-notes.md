# Syntax notes

## Arrow functions

We cant do `.bind()` on arrow function, but we can attach the handler like the following:
~~~~
<div onClick={() => {this.props.doSomething('with-arg')}}>Click me</div>
~~~~

To return an object:
~~~~
arr.map(item => ({someting: iterm}))
~~~~
