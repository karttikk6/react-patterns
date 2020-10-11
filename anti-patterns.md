# React anti patterns

1. bind() and arrow functions in Components - You must have bound your custom functions in the constructor function 
before using them as props for components. If you declare components using the extends keyword, then the custom functions (such as updateValue below) lose their this bindings. 
So, if you want to access this.state, or this.props or this.setState then you need to re-bind them.

2. Using indexes in key Prop - Key is an essential prop when you iterate over a collection of elements. Keys should be stable, predictable, and unique so that React can keep track of elements. Keys are used to help React easily reconcile(read: update) the differences between the virtual DOM and the real DOM. However, using certain set of values such as array indexes may break your application or render wrong data.
