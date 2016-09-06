# React-Times

> A time picker react-component, no jquery-rely.

![react-times](./intro_src/react-times.gif)

## Install

dependencies:

- [`moment`](https://github.com/moment/moment/)
- [`react`](https://github.com/facebook/react)
- [`react-dom`](https://github.com/facebook/react)

> NO JQUERT RELY 😤😤😤

So generally speaking, you should have `react` & `react-dom` in your project. If not:

```bash
$ npm install react react-dom --save-dev
```

and:

```bash
$ npm install react-times --save-dev
```

## Usage

Until now, this Component has only one theme -- The Material Design Theme. I'll working on more themes later.

```javascript
// basic usage

// in some react component
import React from 'react';
import TimePicker from 'react-times';
require('react-times/css/react_times.css');

export default class SomeComponent extends React.Component {
  // do some work
  onHourChange(hour) {
    // do something
  }

  onMinuteChange(minute) {
    // do something
  }

  onFocusChange(focusStatue) {
    // do something
  }

  render() {
    <TimePicker
      onFocusChange={this.onFocusChange.bind(this)}
      onHourChange={this.onHourChange.bind(this)}
      onMinuteChange={this.onMinuteChange.bind(this)}
    />
  }
}
```

## API

### Props

- `defaultTime`:

Must be a string, with `${hour}:${minute}` format, default now(by using `moment()`):

```
defaultTime="11:11"
defaultTime="11:01"
defaultTime="1:01"
defaultTime="1:1"
```

- `focused`

Whether the timepicker pannel is focused or not when it did mount. Default `false`

```
focused={false}
focused={true}
```

- `onFocusChange`

The callback func when component `focused` state is changed.

- `onHourChange`

The callback func when component `hour` state is changed.

```javascript
onHourChange(hour) {
  // ...
}
```

- `onMinuteChange`

The callback func when component `minute` state is changed.

```javascript
onMinuteChange(minute) {
  // ...
}
```

## TODOS

- Hight Order Component
- Test
- Color Palette
- Themes

## Thanks

Thanks to the Airbnb's open source project: [react-dates](https://github.com/airbnb/react-dates), I have learn a lot from that. Thanks.

## License

```
MIT License

Copyright (c) 2016 ecmadao

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```