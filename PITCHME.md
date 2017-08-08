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

```
const Wrapper = (props) => <ul>{props.children}</ul>

<Wrapper>
  <li>Apple</li>
  <li>Pear</li>
</Wrapper>

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

Mounting > Updating > Unmounting

* componentWillMount
* render
* componentDidMount
* componentWillReceiveProps
* shouldComponentUpdate
* componentWillUpdate
* componentDidUpdate
* componentWillUnmount

---
## Components can have State

* setState
* forceUpdate

---
## Developer Experience

```
  render () {
    let charts = this.charts.map((chart, idx) =>
      <Chart
        //key={idx}
        type={chart.type}
        ...
      />
    )

    return <div className="charts">{charts}</div>
  }
```

![debugging](/img/debugging.png)

---
## But does it (JSX) work with Typescript?

# YES

```
declare namespace JSX {
  interface IntrinsicElements {
    foo: { requiredProp: string; optionalProp?: number }
  }
}

<foo requiredProp="bar" />; // ok
<foo />; // error, requiredProp is missing
```

---
## Let's talk about Angular!

![wat](https://media.giphy.com/media/Eq3pvFO7d2mIw/giphy.gif)
(wat)

---
## React Component Vs Angular Component

```
const Hello = (props) => <h1>Hello, {props.name}</h1>
```

```
let helloWorldTemplate = '<h1>Hello, {$ctrl.name}</h1>'

angular.component('HelloWorld', {
  bindings: {
    name: '='    
  },
  templateUrl: helloWorldTemplate,
})
```

---
## Salient Differences

1. React does not use templates
2. React does not use watchers or two way binding
3. React's lifecycle is explicitly defined
4. React is WYSIWYG

---
## How Might a Transition Work?

1. Compatible with our Flux implementation
1. Module talk and my Component doc should help
1. Imagine the UI is a tree of nodes, where each node is a Component
1. Start out at the leaf nodes of the application
1. Replace Angular Components with React Components defined in JS Modules!
1. Work your way up

---
## Angular + React??

Lots of these wrappers exist:

```
// Our React component
import { HelloWorld } from './hello'
// Our Angular << React wrapper
import { react2angular } from 'react2angular'

angular
  .module('looker.silly.components', [])
  .component('HelloWorld', react2angular(HelloWorld, []))
```

---
## Hackday React!

##### Workbooks!

![workbook](/img/workbook.jpg)

##### Adam's Mobile Hackday Popular Content App That Let's Click on Popular Dashboards and View them on your Mobile Device 

---
## Advanced Land

* High order functions
* Good tooling support
* Testing is great

---
## One Last Thing!

#### Java > Nashorn > React

The (🦃(🦆)) turducken of backend rendering!

---
## Why you should not use React

![pop](/img/popularity.png)

---
## Why you should use React

* Well supported by tools and community
* Simple API
* Does one thing well
* Makes it easy to reason about your UI

---
## Should we use React?

* Angular 1.x is a dead end
* React is a simple, lightweight Component library
* Works with our other technologies
* So, yes! (IMHO!)

(Really we should lean on folks like Will Scullin who has React experience, and get everyone on board before making a final final decision.)

---
## Applause

![clap](https://media.giphy.com/media/a0Lgc1JvbfS4o/giphy.gif)

---
## Reference

* [React](https://facebook.github.io/react/)
* [Lifecycle Methods](https://facebook.github.io/react/docs/react-component.html)

---
## Notes
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
