# State and Props
In a React component, props are variables passed to it by its parent component. State on the other hand is still variables, but directly initialized and managed by the component.
The state can be initialized by props.

For example, a parent component might include a child component by calling
```
<ChildComponent />
```

The parent can pass a prop by using this syntax:
```
<ChildComponent color=green />
```
Inside the ChildComponent constructor we could access the prop:
```
class ChildComponent extends React.Component {
  constructor(props) {
    super(props)
    console.log(props.color)
  }
}
```
and any other method in this class can reference the props using this.props.

Props can be used to set the internal state based on a prop value in the constructor, like this:
```
class ChildComponent extends React.Component {
  constructor(props) {
    super(props)
    this.state.colorName = props.color
  }
}
```
Props should never be changed in a child component, so if there’s something going on that alters some variable, that variable should belong to the component state.

Props are also used to allow child components to access methods defined in the parent component. This is a good way to centralize managing the state in the parent component, and avoid children to have the need to have their own state.

Most of your components will just display some kind of information based on the props they received, and stay stateless.
[Source](https://reactjs.org/docs/components-and-props.html)
