# react-image-service-worker
[![Build Status](https://travis-ci.com/fragm3/react-image-service-worker.svg?branch=master)](https://travis-ci.org/nitish24p/react-worker-image)
A tiny 3.4K(1.4K gzipped) React component to fetch image resources via web workers

[react-image-service-worker](https://www.npmjs.com/package/react-image-service-worker) is a React component, which uses service workers to load images. Thereby not blocking the main thread and speeding up page load time.

## Installation
Using npm

```bash
npm install react-image-service-worker

yarn add react-image-service-worker
```

## Usage

`react-image-service-worker` exports one react component which takes `src` as a prop, and an optional prop of `placeholder`, `style` and `imageClass` which are applied to the img tag.

```js
const ImageWorker = require('react-image-service-worker').default;

or

import ImageWorker from 'react-image-service-worker';

```
usage in code
```jsx
<ImageWorker src='http://image-url' />
```

## Props List


| Prop type        | Required           | type  |
| ------------- |:-------------:| --------------:|
| src      | yes |  string |
| placeholder      | optional      |   string or Component|
| style | optional     |    Object |
|imageClass | optional | string
|containerClass | optional | string

The above props are applied to the img tag.

Found a bug file them [here](https://github.com/fragm3/react-image-service-worker/issues).

## Component in Action

Example:

```
import React, { Component } from 'react';
import ImageWorker from 'react-image-service-worker';

class App extends Component {
  render() {
    return (
      <div>
        <ImageWorker src='https://www.gettyimages.com/gi-resources/images/CreativeLandingPage/HP_Sept_24_2018/CR3_GettyImages-159018836.jpg' />
        {/* <img src="https://www.gettyimages.com/gi-resources/images/CreativeLandingPage/HP_Sept_24_2018/CR3_GettyImages-159018836.jpg" /> */}
      </div>
    );
  }
}

export default App;

```

Using service worker for loading images, the results are: 

![With service worker](https://i.imgur.com/FHed0eL.png)

Without service worker(normal get request), the results are:
![Without service worker, normal get request](https://i.imgur.com/EtK2CLy.png)
