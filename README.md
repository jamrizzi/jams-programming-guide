# Jam's Programming Guide
An opinionated programming guide for consistent and collaborative programming

### The rule above all rules is __consistency__
For example, if the codebase is not ending lines with semicolons, then don't end lines with semicolons

## Basic Constructs

### Use verbs for function names
#### INCORRECT :-1:
```js
function paymentForm() {
  // renders payment form
}
```
#### CORRECT :+1:
```js
function renderPaymentForm() {
  // renders payment form
}
```

## JavaScript

### Use single quotes for strings
#### INCORRECT :-1:
```js
const myString = "I am a string";
```
#### CORRECT :+1:
```js
const myString = 'I am a string';
```

## React

### Order lifecycle methods in the following order

* `constructor() {}`
* `componentWillMount() {}`
* `componentDidMount() {}`
* `componentWillUpdate() {}`
* `componentDidUpdate() {}`
* `renderSomeJSX() {}` _Custom render functions_
* `render() {}`
* `handleSomeEvent() {}` _Event handlers_
* `someHelperFunction() {}` _Helper functions_

### Avoid using the document object
_You should avoid accessing the real dom_
#### INCORRECT :-1:
```js
const myElement = document.getElementById('some-element');
```
_If you must access the real dom, use refs_
#### CORRECT :+1:
```js
const myElement = this.refs.someElement;
```
