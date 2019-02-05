# react-image-service-worker

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

>Component in Action

Observe the page Load time at the bottom right corner in both cases.

The first is via a webworker and the second is the regular get.

<img src="./screen/screen.gif">
