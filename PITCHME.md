# Let's talk about React!

---
## What is React?

1. Library (not a "framework")
2. Declarative
3. Component based 
4. Technology agnostic
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

At its purest, React Components are simple transformation functions which take input and return HTML.

---
## Composition!

```
const AppComponent = (props) => {
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

JSX is a simple way to express UI. It is an expression, which allows a programmer to do interesting things. It is not a template, and is not defined in its own file.

---
## React Lifecycle

List the methods here

---
## Components can have State



---
## Developer Experience

---
## Tooling Support

---
## Testing

---
## But does it work with Typescript?

---
## As compared to Angular

---
## Component vs Component

---
## How Might a Transition Work?

---
## Modules!

Mention angular wrapper here

---
## Some Projects Already Use React!

Workbooks
Adam's Mobile apps (yep, React Native give yous mobile support)

---
## Advanced Land

High order functions to replace Transclusion

---
## Why you should not use React

![pop](/img/popularity.png)

---
## Why you should use React

* Well supported
* Simple API
* Does one thing well
* Makes it easy to reason about your UI

---
## Applause

---
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
