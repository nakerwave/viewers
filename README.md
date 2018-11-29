# Naker Viewer
A standalone library to easily add naker scene anywhere online

## Getting Started

Import the Javascript viewer in the header of your website (current last version v1.0.0) :

```html
<script src="https://harbor.naker.io/v1.0.0/viewer.js"></script>
```

This line will import the naker global variable to your website.

## Usage

You then need to choose the html element which will be use to build the naker scene. Just select this node by its id like this :
```javascript
var container = document.getElementById('container');
```

Use the render function of the viewer and your project id in order to automatically create your scene like so :

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
});
```

## Options

You can also add options to the render function. The only one available now is the loader option, wether to show the scene loader or not :

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
  loader: false
});
```

If you need a specific option for your project, we are open to it. Juste create an issue to share your idea and discuss it.

## Callback

This is possible to add a callback as a second argument of the render function, this function will be called when the project is completly loaded :

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
}, () => {
  // Scene loaded, do what you need dude
});
```
