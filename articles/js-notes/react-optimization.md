# React optimization

* Do code splitting
    * Per-page with [react router](https://reactjs.org/docs/code-splitting.html)
    * Per-component with [react-loadable](https://github.com/jamiebuilds/react-loadable)
* Analyze the performance with `?react_perf` and [Chrome React dev tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
* Re-structure the code or use `shouldComponentUpdate` or use `PureComponent` (does shallow prop difference)
* Always implement the component with increasing the complexity if necessary: start with `pure function` component, and only then to `Component` if you want to get the ability to use state and have an instance
* Use [why-did-you-update](https://www.npmjs.com/package/why-did-you-update)
* Instead of writing `.bind()` to `on*`-methods inside `render`, you can use arrow function declaration for methods!
* Analyze what is inside of your bundle


