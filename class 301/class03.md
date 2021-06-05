# Passing Functions as Props
## How do I pass an event handler (like onClick) to a component?
Pass event handlers and other functions as props to child components:
```
<button onClick={this.handleClick}> 
```

[Source](https://reactjs.org/docs/faq-functions.html)  

## How do I bind a function to a component instance?
There are several ways to make sure functions have access to component attributes like this.props and this.state, depending on which syntax and build steps you are using.

### 1. Bind in constructor
```
class Foo extends Component {
  constructor(props) {
    super(props);
    this.handleClick = this.handleClick.bind(this);
  }
  
  handleClick() {
    console.log('Click happened');
  }
  
  render() {
    return <button onClick={this.handleClick}>Click Me</button>;
  }
}
```
### 2. Bind in render
```
class Foo extends Component {
  handleClick() {
    console.log('Click happened');
  }

  render() {
    return (
      <button onClick={this.handleClick.bind(this)}>
        Click Me
      </button>
    )
  }
}
```

[Source](https://betterprogramming.pub/passing-functions-to-react-components-2a02d1b2b806)
