# Let's talk about React!

---
## What is React?

1. Library (not a "framework")
2. Declarative
3. Component based 
4. ??
5. Profit 💰🤑💰🤑💰🤑!

---
## Oh no, not another frontend thing!

![angst](/img/frontend-angst.jpg)

---
## React is different, it's gonna be great!*

*MIT Licensed - this statement comes with no warranty or guarantee of fitness!

---?image=/img/krouse.jpg&size=cover
## Did Steve Tell You That?!

Yep, back in about 2014, he did, and turned out he was right!

---
## &lt;Hello name="World">

```
const Hello = (props) => <h1>Hello, {props.name}</h1>
```

```
class Hello extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

At its purest, React Components are simple transformation functions which take input and spit out HTML.

---
## Composition!

```
const App = (props) => {
  return <div>
    <Hello name={props.names[0]}/>
    <Hello name="Hal"/>
    <Hello name="Dave"/>
  </div>
}
```

---
## Don't call it HTML!

#### Please, it's JSX

```
const Hello = (props) => <h1>Hello, {props.name}</h1>
```

```
var Hello = function Hello(props) {
  return React.createElement(
    "h1",
    null,
    "Hello ",
    props.name
  );
};
```

---
# Why you should not use React

✨ It's New! ✨

- Not really: https://github.com/facebook/react/releases/tag/v0.3.0 -




- Projects that already used react
- Simple API
- Simple Representation of a UI Component
- Functional
- Working with Typescript
- Working with Angular
- Within Modules

- Everything is a function
- Bye transclusion (remember everything is a function)


# 
