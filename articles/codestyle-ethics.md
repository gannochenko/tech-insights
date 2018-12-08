# Code style and ethics (Do-s and Don't-s)

## Ethics

* Choose Simplicity over Complexity
    * Do not go too much in code generalization, you will die in frustrations about the architecture
    * Do not go too much in code specialization, you will produce code that is impossible to maintain
* Learn how to learn
* Do not implement or make room for features "in advance"
* Do not perform pre-optimization

## Code style

### General

* OOP and inheritance
    * Use class inheritance as little as possible (only when really needed and useful)
    * Use class composition as much as possible
    * Don't nest inheritance too deep, 3 levels max (deeper means harder to understand)
    * Never ever use inheritance in React
* Don't write custom solutions, especially when you work in a big team, make everything reasonably close to documentation
* Split your code onto functions wisely:
    * do not create functions that appear only once and contain one line of code
    * do not create functions that do multiple things
    * come up with meaningful names, starting from a verb
* In general, any nesting increases overal complexity, unless it is required by the data structures like trees, you need to make structures as flat as possible
* Try to make a folder structure of the project as shallow as possible

### Javascript

* Do tree shaking. For instance, get rid of modules like `underscore-mixin` or refactor it, because you import the whole `underscore` by using that. Instead, import only used functions.
* React:
    * Don't do `.bind()`, write arrow functions (it wont hurt, because you are not going to use inheritance)
    * Don't mess up between `controlled` and `uncontrolled` components when doing forms, choose either one or another
    * Don't use `derived state`, use [reselect]() instead
    * Prefer `pure function` components to regular components
    * Never ever use component inheritance
