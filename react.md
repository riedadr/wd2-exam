# React

2. Write a react component "PrintHeadline" that renders a variable H1 headline using attribute "myHeadline" !

    ```js
    // Example usage: <PrintHeadline myHeadline="this is a variable Headline" />

    // Class Component
    class PrintHeadline extends React.Component {
        render() {
            return <h1>{this.props.myHeadline}</h1>
        }
    }
    
    // Functional Component
    function PrintHeadline(props) {
        return <h1>{props.myHeadline}</h1>;
    }
    ```

3. Which method must be implemented by a react component at least that returns HTML code?

    ```js
    // Class Component: render()
    render(){
        return(<h1>Hallo</h1>)
    }
    
    //Functional Component
    return(<h1>Hallo</h1>)
    ```

4. Which data structure should be used to access input data that is passed into a react component?

    ```js
    // Class Component: object
    this.props
    ```

5. When a react component’s state data changes, which method will be invoked to update the rendered markup?

    ```js
    // Class Component
    render()
    ```

6. Which data structure holds the state data in a react component?

    ```js
    // Class Component: object
    this.state
    ```

7. Which react method must be called to set a state property?

    ```js
    // Class Component: setState({key: value})
    this.setState((state) => {
        return {counter: state.counter + 1}
    })
    
    // Functional Component
    const [someState, setSomeState] = useState();
    setSomeState("muss zur Änderung aufgerufen werden");
    ```

8. Which react method must be called in a components constructor to properly handle passed input data?

    ```js
    // Class Component
    super(props)
    ```
