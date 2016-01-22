react-remarkable
=================

A React component for rendering Markdown with [remarkable](https://github.com/jonschlinkert/remarkable).

The original project is: https://github.com/acdlite/react-remarkable

This version is forked from: https://github.com/matthewmueller/react-remarkable 

This version is an experiment and may lose compatibility with the original, 
please use one of the above if you are looking for a *stable* project.


```
npm install --save react-remarkable
```

## Usage

```jsx

var React = require('react');
var Markdown = require('react-remarkable');

var MyComponent = React.createClass({

  render: function() {
    return (
      <div>
        {/* Pass Markdown source to the `source` prop */}
        <Markdown source="**Markdown is awesome!**" />

        {/* Or pass it as children */}
        {/* You can nest React components, too */}
        <Markdown>
        {`
          ## Reasons React is great

          1. Server-side rendering
          2. This totally works:

          <SomeOtherAmazingComponent />

          Pretty neat!
        `}
        </Markdown>
      </div>
    );
  }

});

```

Available props:

- `options` - Hash of Remarkable options
- `source`  - Markdown source. You can also pass the source as children, which allows you to mix React components and Markdown.
- `container` - Element to use as container. Defaults to `span`.

## License
MIT
