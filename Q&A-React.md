Certainly! Let's break down the key concepts and questions related to React:

### 1. What is React?
**Definition:** React is a JavaScript library for building user interfaces, particularly for single-page applications where a dynamic and interactive user experience is required.

### 2. What are the major features of React?
- **Component-Based Architecture:** UI is divided into reusable components.
- **JSX:** A syntax extension that allows writing HTML-like code in JavaScript.
- **Virtual DOM:** Efficient updates to the real DOM by using a virtual representation.
- **One-Way Data Binding:** Data flows in one direction, making it easier to understand how data changes affect the UI.
- **Hooks:** Functions that let you use state and other React features in functional components.

### 3. What is JSX?
**Definition:** JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code within JavaScript. It is then compiled to JavaScript functions.

**Example:**
```jsx
const element = <h1>Hello, world!</h1>;
```

### 4. What is the difference between Element and Component?
- **Element:** A plain object describing what should appear in the UI. For example, `<div>Hello</div>` is an element.
- **Component:** A function or class that optionally accepts inputs (props) and returns a React element describing what should appear on the screen. Components can be reused and are more complex than elements.

### 5. How to create components in React?
- **Functional Component:**
```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```
- **Class Component:**
```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

### 6. When to use a Class Component over a Function Component?
- **Class Component:** Use when you need to use lifecycle methods or manage state using `this.state` and `this.setState()`.
- **Function Component:** Preferable for simpler components, especially when using React Hooks for managing state and side effects.

### 7. What are Pure Components?
**Definition:** Pure components are components that implement `shouldComponentUpdate` with a shallow prop and state comparison to prevent unnecessary re-renders.

**Example:**
```jsx
class MyComponent extends React.PureComponent {
  render() {
    // Component logic here
  }
}
```

### 8. What is state in React?
**Definition:** State is a built-in object that stores property values that belong to a component. State can be modified using `setState()` in class components or `useState()` in functional components.

### 9. What are props in React?
**Definition:** Props (short for properties) are read-only attributes passed from a parent component to a child component to configure or render it. Props cannot be changed by the child component.

### 10. What is the difference between state and props?
- **State:** Managed within a component and can change over time. Used for dynamic data.
- **Props:** Passed from parent to child components and are immutable within the child component. Used for static or external data.

### 11. Why should we not update the state directly?
**Reason:** Directly modifying state bypasses React’s state management and lifecycle methods, which can lead to unpredictable behavior and rendering issues. Always use `setState()` or `useState()` for updates.

### 12. What is the purpose of the callback function as an argument of `setState()`?
**Purpose:** To perform actions based on the state update. It runs after the state has been updated and the component has re-rendered.

**Example:**
```jsx
this.setState({ count: this.state.count + 1 }, () => {
  console.log('State updated:', this.state.count);
});
```

### 13. What is the difference between HTML and React event handling?
**Difference:** 
- **HTML:** Uses string-based event handling attributes (e.g., `onclick="handleClick()"`).
- **React:** Uses a camelCase syntax and functions (e.g., `onClick={this.handleClick}`).

### 14. How to bind methods or event handlers in JSX callbacks?
**Options:**
- **Bind in constructor:**
```jsx
constructor(props) {
  super(props);
  this.handleClick = this.handleClick.bind(this);
}
```
- **Arrow functions in render:**
```jsx
<button onClick={() => this.handleClick()}>Click</button>
```

### 15. How to pass a parameter to an event handler or callback?
**Example:**
```jsx
<button onClick={() => this.handleClick(param)}>Click</button>
```

### 16. What are synthetic events in React?
**Definition:** Synthetic events are React’s cross-browser wrapper around the browser’s native events. They are normalized and consistent across different browsers.

### 17. What are inline conditional expressions?
**Definition:** Techniques for conditionally rendering elements in JSX using ternary operators or logical AND (`&&`).

**Example:**
```jsx
{isLoggedIn ? <LogoutButton /> : <LoginButton />}
```

### 18. What is "key" prop and what is the benefit of using it in arrays of elements?
**Definition:** The `key` prop helps React identify which items have changed, are added, or are removed. It improves performance by optimizing the re-rendering of lists.

### 19. What is the use of refs?
**Definition:** Refs are used to access and interact directly with DOM elements or React component instances.

### 20. How to create refs?
**Example:**
```jsx
const inputRef = useRef(null);
<input ref={inputRef} />
```

### 21. What are forward refs?
**Definition:** Forward refs allow components to forward refs to their children, enabling access to child DOM nodes or components.

**Example:**
```jsx
const FancyInput = forwardRef((props, ref) => (
  <input ref={ref} {...props} />
));
```

### 22. Which is the preferred option with callback refs and `findDOMNode()`?
**Preferred:** Callback refs are preferred as `findDOMNode()` is considered legacy and less efficient.

### 23. Why are String Refs legacy?
**Reason:** String refs are considered legacy because they are less flexible and less reliable compared to callback refs and `React.createRef()`.

### 24. What is Virtual DOM?
**Definition:** The Virtual DOM is a lightweight copy of the real DOM. React uses it to optimize rendering by updating only the parts of the real DOM that have changed.

### 25. How Virtual DOM works?
**Process:**
1. **Render:** React creates a virtual representation of the UI.
2. **Diffing:** React compares the new virtual DOM with the previous one.
3. **Reconciliation:** React updates the real DOM based on the differences.

### 26. What is the difference between Shadow DOM and Virtual DOM?
- **Shadow DOM:** Encapsulates styles and structure of a component, providing a separate DOM tree.
- **Virtual DOM:** A performance optimization for updating the real DOM efficiently by minimizing direct manipulations.

### 27. What is React Fiber?
**Definition:** React Fiber is a complete rewrite of the React core algorithm that improves rendering performance and introduces features like incremental rendering and better support for async rendering.

### 28. What is the main goal of React Fiber?
**Goal:** To enable incremental rendering, allowing React to pause, abort, and continue rendering work, improving user experience and performance.

### 29. What are controlled components?
**Definition:** Controlled components are form elements whose value is controlled by React state. Changes are handled through event handlers.

**Example:**
```jsx
<input type="text" value={this.state.value} onChange={this.handleChange} />
```

### 30. What are uncontrolled components?
**Definition:** Uncontrolled components store their own state internally and access values through refs rather than state.

**Example:**
```jsx
<input type="text" ref={this.inputRef} />
```

### 31. What is the difference between `createElement` and `cloneElement`?
- **`createElement`:** Creates a new React element.
- **`cloneElement`:** Clones and returns a new element with additional props.

### 32. What is Lifting State Up in React?
**Definition:** Moving state from a child component to its parent so that multiple child components can share and synchronize the state.

### 33. What are the different phases of component lifecycle?
- **Mounting:** Component is being created and inserted into the DOM.
- **Updating:** Component is being re-rendered due to state or prop changes.
- **Unmounting:** Component is being removed from the DOM.

### 34. What are the lifecycle methods of React?
**Class Component Lifecycle Methods:**
- **Mounting:** `constructor()`, `componentDidMount()`
- **Updating:** `shouldComponentUpdate()`, `componentDidUpdate()`
- **Unmounting:** `componentWillUnmount()`

### 35. What are Higher-Order components?
**Definition:** Higher-Order Components (HOCs) are functions that take a component and return a new component with enhanced functionality.

**Example:**
```jsx
function withLogging(WrappedComponent) {
  return class extends React.Component {
    componentDidMount() {
      console.log('Component mounted');
    }
    render() {
      return <WrappedComponent {...this.props} />;
    }
  };
}
```

### 36. How to create props proxy for HOC component?
**Example:**
```jsx
const withPropsProxy = (WrappedComponent) => {
  return class extends React.Component {
    render() {
      const

 newProps = { ...this.props, newProp: 'value' };
      return <WrappedComponent {...newProps} />;
    }
  };
};
```

### 37. What is context?
**Definition:** Context provides a way to pass data through the component tree without having to pass props down manually at every level.

### 38. What is children prop?
**Definition:** The `children` prop is a special prop that allows components to pass nested elements to their children.

**Example:**
```jsx
function Container({ children }) {
  return <div>{children}</div>;
}
```

### 39. How to write comments in React?
**Syntax:**
```jsx
{/* This is a comment */}
```

### 40. What is the purpose of using super constructor with props argument?
**Purpose:** To initialize the parent class (React.Component) with the props, allowing access to `this.props` in the constructor of a class component.

**Example:**
```jsx
constructor(props) {
  super(props);
  this.state = { /* state initialization */ };
}
```

### 41. What is reconciliation?
**Definition:** Reconciliation is the process by which React updates the DOM with changes based on the virtual DOM’s diffing algorithm.

### 42. How to set state with a dynamic key name?
**Example:**
```jsx
this.setState(prevState => ({
  [dynamicKey]: newValue
}));
```

### 43. What would be the common mistake of a function being called every time the component renders?
**Mistake:** Defining a function inside the render method. This creates a new function on every render, causing unnecessary re-renders of child components.

### 44. Does `lazy` function support named exports?
**No:** `React.lazy` supports default exports only. Named exports should be wrapped in a default export.

### 45. Why does React use `className` over `class` attribute?
**Reason:** `class` is a reserved keyword in JavaScript, so React uses `className` to avoid conflicts.

### 46. What are fragments?
**Definition:** Fragments let you group multiple elements without adding extra nodes to the DOM.

**Example:**
```jsx
<>
  <Child1 />
  <Child2 />
</>
```

### 47. Why are fragments better than container divs?
**Reason:** Fragments do not add extra nodes to the DOM, which helps keep the DOM structure cleaner and avoids unnecessary elements.

### 48. What are portals in React?
**Definition:** Portals allow rendering children into a different part of the DOM outside of the parent component’s DOM hierarchy.

**Example:**
```jsx
ReactDOM.createPortal(child, container)
```

### 49. What are stateless components?
**Definition:** Stateless components are components that do not manage state and only rely on props for rendering.

**Example:**
```jsx
function StatelessComponent(props) {
  return <div>{props.text}</div>;
}
```

### 50. What are stateful components?
**Definition:** Stateful components manage their own state and use it to control rendering and behavior.

**Example:**
```jsx
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return <div>{this.state.count}</div>;
  }
}
```

### 51. How to apply validation on props in React?
**Method:** Use `PropTypes` to define expected types and required props.

**Example:**
```jsx
import PropTypes from 'prop-types';

MyComponent.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number
};
```

### 52. What are the advantages of React?
- **Component-Based Architecture:** Modular and reusable components.
- **Virtual DOM:** Efficient rendering and updates.
- **Declarative Syntax:** Easier to understand and debug.
- **Strong Community and Ecosystem:** Wide range of libraries and tools.

### 53. What are the limitations of React?
- **Learning Curve:** Requires understanding JSX, components, and state management.
- **Boilerplate:** Often involves additional setup and tooling.
- **SEO Challenges:** Client-side rendering can be challenging for SEO unless server-side rendering is used.

### 54. What are error boundaries in React v16?
**Definition:** Error boundaries are components that catch JavaScript errors anywhere in their child component tree and log those errors or display fallback UI.

**Example:**
```jsx
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError() {
    return { hasError: true };
  }

  componentDidCatch(error, info) {
    console.error(error, info);
  }

  render() {
    if (this.state.hasError) {
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children;
  }
}
```

### 55. How were error boundaries handled in React v15?
**Answer:** React v15 did not have error boundaries. Error handling in v15 was typically done with try-catch blocks and error handling in lifecycle methods.

### 56. What are the recommended ways for static type checking?
- **PropTypes:** For runtime type checking of props.
- **TypeScript:** For static type checking and integrating types into your development workflow.

### 57. What is the use of `react-dom` package?
**Definition:** The `react-dom` package provides DOM-specific methods to mount and unmount React components and manage updates to the DOM.

### 58. What is the purpose of the `render` method of `react-dom`?
**Purpose:** To render a React component tree into the DOM.

**Example:**
```jsx
ReactDOM.render(<App />, document.getElementById('root'));
```

### 59. What is `ReactDOMServer`?
**Definition:** `ReactDOMServer` is used for server-side rendering of React components, allowing you to generate HTML on the server.

### 60. How to use `innerHTML` in React?
**Example:**
```jsx
<div dangerouslySetInnerHTML={{ __html: '<p>HTML content</p>' }} />
```
**Caution:** Use `dangerouslySetInnerHTML` sparingly to avoid XSS attacks.

### 61. How to use styles in React?
**Options:**
- **Inline Styles:**
```jsx
const style = { color: 'blue' };
<div style={style}>Hello</div>
```
- **CSS Modules:** 
```jsx
import styles from './styles.module.css';
<div className={styles.myClass}>Hello</div>
```
- **Styled Components:** Use libraries like `styled-components` for CSS-in-JS.

### 62. How are events different in React?
**Difference:** React wraps native events in synthetic events, which are normalized and consistent across browsers.

### 63. What will happen if you use `setState` in the constructor?
**Outcome:** Using `setState` in the constructor will not have any effect because the component is not yet mounted. Initialization of state should be done directly in the constructor.

### 64. What is the impact of indexes as keys?
**Impact:** Using array indexes as keys can lead to performance issues and component state problems, especially when items are reordered or removed. It’s better to use unique IDs.

### 65. Is it good to use `setState()` in `componentWillMount()` method?
**Answer:** No, `componentWillMount()` is deprecated. Use `componentDidMount()` for making changes to state or side effects.

### 66. What will happen if you use props in initial state?
**Answer:** It can lead to problems if the props change after initial render. Use `getDerivedStateFromProps` or `componentDidUpdate` for synchronizing state with props.

### 67. How do you conditionally render components?
**Methods:**
- **Ternary Operator:** 
```jsx
{isLoggedIn ? <LogoutButton /> : <LoginButton />}
```
- **Logical AND (`&&`):**
```jsx
{showContent && <Content />}
```

### 68. Why we need to be careful when spreading props on DOM elements?
**Reason:** Spreading props on DOM elements can inadvertently pass unwanted attributes or props to the DOM, leading to potential bugs or warnings.

### 69. How do you use decorators in React?
**Answer:** Decorators are a proposed feature and are not part of the core React library. They can be used with tools like Babel to modify class behavior.

### 70. How do you memoize a component?
**Methods:**
- **`React.memo`:** For functional components.
```jsx
const MemoizedComponent = React.memo(Component);
```
- **`useMemo` and `useCallback`:** For optimizing specific functions or values.

### 71. How do you implement Server-Side Rendering (SSR)?
**Method:** Use `ReactDOMServer.renderToString()` or frameworks like Next.js for server-side rendering to generate HTML on the server.

### 72. How to enable production mode in React?
**Method:** Set the `NODE_ENV` environment variable to `"production"` during build and deployment.

### 73. What is CRA and its benefits?
**Definition:** CRA (Create React App) is a tool for setting up a new React project with a modern build setup. Benefits include zero configuration, built-in development tools, and optimized builds.

### 74. What is the lifecycle methods order in mounting?
**Order:**
1. `constructor()`
2. `static getDerivedStateFromProps()`
3. `render()`
4. `componentDidMount()`

### 75. What lifecycle methods are

 going to be deprecated in React v16?
**Deprecated Methods:**
- `componentWillMount()`
- `componentWillReceiveProps()`
- `componentWillUpdate()`

### 76. What is the purpose of `getDerivedStateFromProps()` lifecycle method?
**Purpose:** To derive state from props before rendering. It’s called right before rendering, both on the initial mount and on subsequent updates.

### 77. What is the purpose of `getSnapshotBeforeUpdate()` lifecycle method?
**Purpose:** To capture some information from the DOM before it is potentially changed. Useful for reading layout information.

### 78. Do Hooks replace render props and higher-order components?
**Answer:** Hooks provide a simpler and more direct way to reuse stateful logic and side effects, which can often replace the need for render props and higher-order components.

### 79. What is the recommended way for naming components?
**Recommendation:** Use PascalCase for component names (e.g., `MyComponent`) to distinguish them from HTML elements and JavaScript functions.

### 80. What is the recommended ordering of methods in a component class?
**Recommended Order:**
1. Constructor
2. Static methods (e.g., `getDerivedStateFromProps`)
3. Lifecycle methods
4. Event handlers
5. Render method

### 81. What is a switching component?
**Definition:** A switching component (often used with React Router) renders different components based on the current URL or route.

### 82. Why do we need to pass a function to `setState()`?
**Reason:** To ensure that state updates are based on the previous state, especially when updates are asynchronous or depend on the current state.

### 83. What is Strict Mode in React?
**Definition:** Strict Mode is a development-only feature that helps identify potential problems in an application by activating additional checks and warnings.

### 84. What are React Mixins?
**Definition:** Mixins were a way to reuse code across multiple components but are now deprecated in favor of higher-order components and hooks.

### 85. Why is `isMounted()` an anti-pattern and what is the proper solution?
**Reason:** `isMounted()` is considered unreliable. Use `componentDidMount()` and `componentWillUnmount()` to handle setup and cleanup.

### 86. What are the Pointer Events supported in React?
**Supported Events:**
- `onPointerDown`
- `onPointerUp`
- `onPointerMove`
- `onPointerEnter`
- `onPointerLeave`
- `onPointerCancel`

### 87. Why should component names start with a capital letter?
**Reason:** Component names must start with a capital letter to distinguish them from HTML tags and to enable JSX to properly recognize them.

### 88. Are custom DOM attributes supported in React v16?
**Yes:** React v16 supports custom attributes as long as they do not clash with standard HTML attributes or React-specific attributes.

### 89. What is the difference between constructor and `getInitialState`?
- **Constructor:** Initializes state and binds methods in ES6 classes.
- **`getInitialState`:** Was used in React's earlier versions (before ES6 classes) to initialize state.

### 90. Can you force a component to re-render without calling `setState`?
**Method:** Yes, you can force a re-render by calling `forceUpdate()`, but this is generally discouraged. `setState` should be used for state changes.

### 91. What is the difference between `super()` and `super(props)` in React using ES6 classes?
- **`super()`:** Calls the parent class constructor without passing props.
- **`super(props)`:** Calls the parent class constructor and passes props, allowing access to `this.props` in the constructor.

### 92. How to loop inside JSX?
**Method:** Use JavaScript array methods like `map()` to iterate and render elements.

**Example:**
```jsx
const items = ['Item1', 'Item2', 'Item3'];
const listItems = items.map((item, index) => <li key={index}>{item}</li>);
return <ul>{listItems}</ul>;
```

### 93. How do you access props in attribute quotes?
**Example:**
```jsx
const Greeting = ({ name }) => <div>Hello, {name}</div>;
```

### 94. What is React PropType array with shape?
**Definition:** A way to validate the shape of array elements using PropTypes.

**Example:**
```jsx
MyComponent.propTypes = {
  items: PropTypes.arrayOf(PropTypes.shape({
    id: PropTypes.number,
    name: PropTypes.string
  }))
};
```

### 95. How to conditionally apply class attributes?
**Example:**
```jsx
const className = isActive ? 'active' : 'inactive';
<div className={className}>Content</div>
```

### 96. What is the difference between React and ReactDOM?
- **React:** Core library for building components and managing the virtual DOM.
- **ReactDOM:** Provides methods to render React components to the actual DOM.

### 97. Why is ReactDOM separated from React?
**Reason:** Separation allows React to focus on building components and managing state while ReactDOM handles the specific tasks related to DOM manipulation.

### 98. How to use React label element?
**Example:**
```jsx
<label htmlFor="inputId">Label</label>
<input id="inputId" />
```

### 99. How to combine multiple inline style objects?
**Example:**
```jsx
const style1 = { color: 'red' };
const style2 = { fontSize: '20px' };
const combinedStyle = { ...style1, ...style2 };

<div style={combinedStyle}>Styled Text</div>
```

### 100. How to re-render the view when the browser is resized?
**Method:** Use the `resize` event listener to handle window size changes.

**Example:**
```jsx
useEffect(() => {
  const handleResize = () => {
    // handle resize
  };

  window.addEventListener('resize', handleResize);

  return () => {
    window.removeEventListener('resize', handleResize);
  };
}, []);
```

Feel free to ask if you need more details on any of these topics!
