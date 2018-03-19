<div align="center"><strong>React Expand</strong></div>

<div align="center">
  <a href="https://david-dm.org/sonybinhle/react-expand-animated">
    <img src="https://david-dm.org/sonybinhle/react-expand-animated.svg" alt="Dependency Status" />
  </a>

  <a href="https://david-dm.org/sonybinhle/react-expand-animated#info=devDependencies">
    <img src="https://david-dm.org/sonybinhle/react-expand-animated/dev-status.svg" alt="devDependency Status" />
  </a>

  <a href="https://travis-ci.org/sonybinhle/react-expand-animated">
    <img src="https://travis-ci.org/sonybinhle/react-expand-animated.svg" alt="Build Status" />
  </a>
  
  <a href='https://coveralls.io/github/sonybinhle/react-expand-animated?branch=master'>
    <img src='https://coveralls.io/repos/github/sonybinhle/react-expand-animated/badge.svg?branch=master' alt='Coverage Status' />
   </a>

</div>

## react-expand-animated 0.0.1

Simple expandable wrapper component with height, opacity animation. 

## Install

`npm i react-expand-animated`

## Usage

```jsx harmony
import React, { Component } from 'react';
import Expand from 'react-expand-animated';

class App extends Component {
  state = { open: false };

  toggle = () => {
    this.setState(prevState => ({ open: !prevState.open }));
  };

  render() {
    return (
      <Fragment>
        <button onClick={this.toggle}>Open</button>
        <Expand open={this.state.open}>
          <div style={{ width: '300px', height: '400px', color: 'red' }}>Hello</div>
        </Expand>
      </Fragment>
    );
  }
}

export default App;
```
## Props
| Props  | Type | Required | Default | Description |
| ------------- | ------------- |  ------------- |  ------------- |  ------------- |
| children  | node  | true | undefined | The expanded or collapsed content |
| open  | bool | false | false | When set to true expand the children component otherwise collapse it |
| duration  | number | false | 1000 | Animation duration in ms |
| easing  | string | false | 'ease-in-out' | Css3 Animation's type |
| className  | string | false | '' | Wrapper's className |
| tag  | string | false | 'div' | Wrapper's tag |

## Development

Dev: `npm run dev`

Build: `npm run build`

Test: `npm test`

Test Coverage: `npm run test:cov`
