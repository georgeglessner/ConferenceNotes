# Get to Know Webpack
> Jonathan Kemp

As web development becomes more compolex, we need tooling to help us build modern websites. 

Starter kits exist so that we can start writing the code withought having to udnerstand the tools. 

When everything works out of the box, you might not know what's really under the hood. Understanding how the tools work help us make better decisions about our code. 

### Why Webpack
- script loading is synchronous
	- this is why you put script tags at bottom of page

### Javascript Modules
- closures
- RequireJS
-Node.js and CommonJS (npm)
	- every file is a module with its own scope and context. 

### Browserify
- A tool for compiling CommonJS modules for the browser


Webpack took over in the role of universal module bundler due to broader feature set.

### Getting started
- webpack is a static module bundler for moder js apps
- combining all dependencies into one file
- builds internal dependency graphy and generates one or more bundles depending on those

When webpack proccesses your application, it starts from a list of modules defined on the command line or in its config file.

command to run webpack -> `npx webpack`

### Modules
- webpack supports them out of the box, even though some browsers do not. 
	- webpack transpiles for the code so older browsers can also run it


As of version 4, webpack doesn't require any configuration

Most projects will need a more complex serup, which is why webpack supports a configuration file. 

### Asset management
- manage assets like images and fonts with webpack

### Loaders
- out of the box, webpack only understands JS and JSON
- loaders allow webpack to process other file types

Webpack v4+ will minify your code by default in production. 




