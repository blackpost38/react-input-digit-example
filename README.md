react input digit example
===

You can check the example in `src/App.js`

```
import React, { Component } from 'react';
import DigitInput from 'react-input-digit';
import logo from './logo.svg';
import './App.css';

class App extends Component {
  constructor(props) {
    super(props);

    this.state = { value: 38 };
    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e, { value }) {
    this.setState({ value });
  }

  render() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h1 className="App-title">Welcome to React</h1>
        </header>
        <p className="App-intro">
          <DigitInput
            value={this.state.value}
            onChange={this.handleChange}
          />
        </p>
      </div>
    );
  }
}

export default App;
```