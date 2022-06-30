# React Basic

<details>
<summary>**Create a Simple JSX Element**</summary>
    
    ```jsx
    const JSX = (
      <h1>Hello JSX!</h1>
    );
    ```
</details>    
- **Create a Complex JSX Element**
    
    ```jsx
    const JSX = (
      <div>
        <h1>HEADING ONE</h1>
        <p>This is Paragraph.</p>
        <ul>
          <li>List One</li>
          <li>List Two</li>
          <li>List Three</li>
        </ul>
      </div>
    );
    ```
    
- **Add Comments in JSX**
    
    ```jsx
    const JSX = (
      <div>
        {/* This is comment */}
        <h1>This is a block of JSX</h1>
        <p>Here's a subtitle</p>
      </div>
    );
    ```
    
- **Render HTML Elements to the DOM**
    
    ```jsx
    const JSX = (
      <div>
        <h1>Hello World</h1>
        <p>Lets render this to the DOM</p>
      </div>
    );
    ReactDOM.render(JSX, document.getElementById('challenge-node'));
    ```
    
- **Define an HTML Class in JSX**
    
    ```jsx
    const JSX = (
      <div className="myDiv">
        <h1>Add a class to this div</h1>
      </div>
    );
    ```
    
- **Learn About Self-Closing JSX Tags**
    
    ```jsx
    const JSX = (
      <div>
        <h2>Welcome to React!</h2> <br/>
        <p>Be sure to close all tags!</p>
        <hr/>
      </div>
    );
    ```
    
- **Create a Stateless Functional Component**
    
    ```jsx
    const MyComponent = function() {
      return(
        <div>Hello World!</div>
      );
    }
    ```
    
- **Create a React Component**
    
    ```jsx
    class MyComponent extends React.Component {
      constructor(props) {
        super(props);
      }
      render() {
        return(
          <div>
            <h1>Hello React!</h1>
          </div>
        );
      }
    };
    ```
    
- **Create a Component with Composition**
    
    ```jsx
    const ChildComponent = () => {
      return (
        <div>
          <p>I am the child</p>
        </div>
      );
    };
    
    class ParentComponent extends React.Component {
      constructor(props) {
        super(props);
      }
      render() {
        return (
          <div>
            <h1>I am the parent</h1>
            <ChildComponent/>
          </div>
        );
      }
    };
    ```
    
- **Use React to Render Nested Components**
    
    ```jsx
    const TypesOfFruit = () => {
      return (
        <div>
          <h2>Fruits:</h2>
          <ul>
            <li>Apples</li>
            <li>Blueberries</li>
            <li>Strawberries</li>
            <li>Bananas</li>
          </ul>
        </div>
      );
    };
    
    const Fruits = () => {
      return (
        <div>
          <TypesOfFruit/>
        </div>
      );
    };
    
    class TypesOfFood extends React.Component {
      constructor(props) {
        super(props);
      }
    
      render() {
        return (
          <div>
            <h1>Types of Food:</h1>
            <Fruits/>
          </div>
        );
      }
    };
    ```
    
- **Compose React Components**
    
    ```jsx
    class Fruits extends React.Component {
      constructor(props) {
        super(props);
      }
      render() {
        return (
          <div>
            <h2>Fruits:</h2>
            <NonCitrus/>
            <Citrus/>
          </div>
        );
      }
    };
    
    class TypesOfFood extends React.Component {
      constructor(props) {
         super(props);
      }
      render() {
        return (
          <div>
            <h1>Types of Food:</h1>
            <Fruits/>
            <Vegetables />
          </div>
        );
      }
    };
    ```
    
- **Render a Class Component to the DOM**
    
    ```jsx
    class TypesOfFood extends React.Component {
      constructor(props) {
        super(props);
      }
      render() {
        return (
          <div>
            <h1>Types of Food:</h1>
            <Fruits/>
            <Vegetables/>
          </div>
        );
      }
    };
    
    ReactDOM.render(<TypesOfFood/>, document.getElementById("challenge-node"));
    ```
    
- **Write a React Component from Scratch**
    
    ```jsx
    class MyComponent extends React.Component{
      constructor(props){
        super(props);
      }
      render(){
        return(
          <div className="challenge-node">
            <h1>My First React Component!</h1>
          </div>
        );
      }
    };
    
    ReactDOM.render(<MyComponent/>, document.getElementById("challenge-node"));
    ```
    
- **Pass Props to a Stateless Functional Component**
    
    ```jsx
    const CurrentDate = (props) => {
      return (
        <div>
          <p>The current date is: {props.date}</p>
        </div>
      );
    };
    
    class Calendar extends React.Component {
      constructor(props) {
        super(props);
      }
      render() {
        return (
          <div>
            <h3>What date is it?</h3>
            <CurrentDate date={Date()}/>
          </div>
        );
      }
    };
    ```