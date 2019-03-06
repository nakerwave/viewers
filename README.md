![alt text](https://asset.naker.io/image/main/logo.png)

# Naker Viewer
#### A standalone library to easily add naker scene anywhere online

## Getting Started

Import the Javascript viewer in the header of your website (current last version v1.0.0) :

```html
<script src="https://harbor.naker.io/v1.0.0/viewer.js"></script>
```

This line will import the `naker` global variable to your website.

## Usage

You then need to choose the html element which will be used to build your naker scene. You can just select this node by its `id` like this :
```javascript
var container = document.getElementById('container');
```

Use the render function of the viewer and your `project id` in order to automatically create your scene like so :

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
});
```
You can find your `project id` from the url when you edit it.

## Options

You can also add some options to the render function. Here is the list of the available once :

| Name           | Type         | Default      | Description                                                          |
| :------------- | :----------: | :----------: | -------------------------------------------------------------------- |
| loadervisible  | _boolean_    | `true`       | Choose if the loader is visible                                      |
| fogstart       | _boolean_    | `true`       | When scene finish loading, you can have fog animation which fade out |
| scrollarrow    | _boolean_    | `true`       | Draw an arrow at the bottom of the screen to push user to scroll     |

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
  loadervisible: false,
  fogstart: true,
  scrollarrow: true,
});
```

If you need a specific option for your project, we are open to it. Juste create an issue to share your idea and discuss it.

## Callback

It is possible to add a callback as a second argument of the render function, this function will be called when the project is completly loaded. The callback returns the scene object which contains your scene elements like point-of-views and contents :

```javascript
naker.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
}, (scene) => {
  // Scene loaded, do what you need dude
});
```
