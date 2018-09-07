# vue-bottom-scroll-listener

A simple Vue component that lets you listen for when you have scrolled to the bottom.

Heavily inspired of [react-bottom-scroll-listener](https://github.com/karl-run/react-bottom-scroll-listener)

## Installation

npm:
`npm install vue-bottom-scroll-listener`

yarn:
`yarn add vue-bottom-scroll-listener`

## Usage

### Simple
```
<bottom-scroll @on-bottom="onBottomCallback"/>
```

### Options
```
<bottom-scroll @on-bottom="onBottomCallback" :debounce="200" :offset="0">
  <p>optional inner content</p>
</bottom-scroll>
```
__Props__

* `@on-bottom` __(required):__ callback invoked when bottom is reached
* `:debounce`: _(default: 200)_ integer in ms, how much debounce there should be on callback
* `:offset`: _(default: 0)_ offset from bottom in pixels. E.g. 300 if it should invoke `onBottom` 300px before the bottom.

## Demo

https://eregnier.github.io/vue-bottom-scroll-listener/dist/js/
