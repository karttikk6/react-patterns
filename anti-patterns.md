# React anti patterns

1. bind() and arrow functions in Components - You must have bound your custom functions in the constructor function 
before using them as props for components. If you declare components using the extends keyword, then the custom functions (such as updateValue below) lose their this bindings. 
So, if you want to access this.state, or this.props or this.setState then you need to re-bind them.
