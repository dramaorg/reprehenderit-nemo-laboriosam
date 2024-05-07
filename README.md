# @dramaorg/reprehenderit-nemo-laboriosam

[![Build Status](https://img.shields.io/github/actions/workflow/status/carloscuesta/@dramaorg/reprehenderit-nemo-laboriosam/ci.yml?branch=master&style=flat-square)](https://github.com/dramaorg/reprehenderit-nemo-laboriosam/actions?query=workflow%3ACI+branch%3Amaster)
[![Codecov](https://img.shields.io/codecov/c/github/carloscuesta/@dramaorg/reprehenderit-nemo-laboriosam.svg?style=flat-square)](https://codecov.io/gh/carloscuesta/@dramaorg/reprehenderit-nemo-laboriosam)
[![Npm Version](https://img.shields.io/npm/v/@dramaorg/reprehenderit-nemo-laboriosam.svg?style=flat-square)](https://www.npmjs.com/package/@dramaorg/reprehenderit-nemo-laboriosam)
[![Npm Downloads](https://img.shields.io/npm/dt/@dramaorg/reprehenderit-nemo-laboriosam.svg?style=flat-square)](https://www.npmjs.com/package/@dramaorg/reprehenderit-nemo-laboriosam)

> A simple and reusable React-Native [error boundary](https://reactjs.org/docs/error-boundaries.html#introducing-error-boundaries) component 🐛

## Install

```bash
yarn add @dramaorg/reprehenderit-nemo-laboriosam
```

## Documentation

- [Installation](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/install)
- [Usage](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/usage/recovering-errors)
  - [Recovering Errors](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/usage/recovering-errors)
  - [Logging Errors](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/usage/logging-errors)
  - [Rendering a Fallback Component](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/usage/rendering-a-custom-fallback-ui)
- [API](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/errorboundary)
  - [`ErrorBoundary`](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/errorboundary)
  - [`FallbackComponent`](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/fallbackcomponent)
- [FAQ](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/faq)

## API

### [`ErrorBoundary`](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/errorboundary)

These are the props that you can pass to the `ErrorBoundary` component:

| Property            | Type              | Required | Default             |
|---------------------|-------------------|----------|---------------------|
| `Children`          | `React.Children`  | `true`   |                     |
| `FallbackComponent` | `React.Component` | `false`  | `FallbackComponent` |
| `onError`           | `Function`        | `false`  |                     |

#### `Children`

Any children that can throw an error. 

#### [`FallbackComponent`](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/fallbackcomponent)

The fallback component that will be rendered after catching an error.
By default the library comes with a built-in component.

#### `onError`

A function that receives two arguments:

- `error`: The error catched by the component.
- `stackTrace`: The stacktrace of the error.

```js
onError(error: Error, stackTrace: string): void
```

### [`FallbackComponent`](https://@dramaorg/reprehenderit-nemo-laboriosam.js.org/api/fallbackcomponent)

These are the props that the `FallbackComponent` receives:

| Property   | Type       | Default |
|------------|------------|---------|
| error      | `Error`    |         |
| resetError | `Function` |         |

#### `error`

The error object.

#### `resetError`

A function to reset the error state. You'll want to call this function to recover from the error state.

```js
resetError(): void
```

## Demo

<img
  src='https://user-images.githubusercontent.com/7629661/111866027-bc158e00-896a-11eb-8140-cfdc5d19527c.gif'
  alt='@dramaorg/reprehenderit-nemo-laboriosam'
  width='354px'
/>
