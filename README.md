# Ember-text-measurer

This addon provides a very simple service to measure the width of a string
using an in-memory canvas, so it doesn't cause any layout reflow for max
performance.

### Installation

`ember install ember-text-measurer`

### Usage

This addon just provides a service that you can inject wherever you need.
The service has one single method `measure(string, font = null)` that will
return the width of the text.

```js
textMeasurer.measure('foobar', '24px arial');             // ~ 68.02px
textMeasurer.measure('foobar', '20px arial');             // ~ 56.64px
textMeasurer.measure('foobar', '20px Times New Roman');   // ~ 52.19px
```

### What can I do with this?

Check [THE DEMO](https://ember-text-measurer.pagefrontapp.com) for some ideas ;-)

### Browser compatibility

Pretty good, in theory all back to IE9, although IE9 might give slightly unnacurate results,
probably not innacurate enough to be a problem.