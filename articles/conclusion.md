# Conclusion (Do-s and Don't-s)

* Do tree shaking. For instance, get rid of modules like `underscore-mixin` or refactor it, because you import the whole `underscore` by using that. Instead, import only used functions.
* Don't do unreasoned inheritance, use composition instead
* Don't do `.bind()`, write arrow functions (it wont hurt, because you are not going to use inheritance)
* Don't write custom solutions, especially in the test assignment, make everything reasonably close to documentation
* Don't mess up with `controlled` and `uncontrolled` components
* Don't use `derived state` at all (use `reselect`?)
* Learn how to use `Reflection` and `yield`
* Prefer `pure function` components to regular components
