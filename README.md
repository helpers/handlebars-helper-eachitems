# {{eachItems}} [![NPM version](https://badge.fury.io/js/helper-eachItems.png)](http://badge.fury.io/js/helper-eachItems)

> {{eachItems}} block helper, iterating over a list of items

## Quickstart
In the root of your project, run the following in the command line:

```bash
npm i handlebars-helper-eachItems --save-dev
```

### Assemble config
If you use [Assemble config](http://assemble.io) and Grunt, in your Gruntfile simply add `handlebars-helper-eachItems` to the `helpers` property in the [Assemble](http://assemble.io) task or target options:

```javascript
grunt.initConfig({
  assemble: {
    options: {
      // the 'handlebars-helper-eachItems' module must also be listed in
      // devDependencies for assemble to automatically resolve the helper
      helpers: ['handlebars-helper-eachItems', 'foo/*.js']
    }
    ...
  }
});
```

You can now use begin using the helper in your templates:

```handlebars
{{#eachItems pages}}
  <li{{#is ../page.dest this.dest}} class="active"{{/is}}>
    <a href="{{relative ../page.dest this.dest}}">{{@number}}</a>
  </li>
{{/eachItems}}
```


## Author

+ [github/Jon Schlinkert](http://github.com/Jon Schlinkert)
+ [twitter/Jon Schlinkert](http://twitter.com/Jon Schlinkert)


## License and Copyright

Licensed under the [MIT License](./LICENSE-MIT)
Copyright (c) Jon Schlinkert, contributors.