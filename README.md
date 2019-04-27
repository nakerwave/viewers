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

## Examples

To see it in action, follow these links:  
[Intale viewer in the body](https://codepen.io/pichou/pen/jJXpxd)  
[Intale viewer in a div](https://codepen.io/pichou/pen/YgdRKq)

# Naker Pearl Viewer
#### A standalone library to add 3D model as illustration on your website

## Getting Started

Import the Javascript Pearl Viewer in the header of your website (current last version v1.0.1) :

```html
<script src="https://harbor.naker.io/pearl/v1.0.1/viewer.js"></script>
```

This line will import the `nakerpearl` global variable to your website.

## Usage

You then need to choose the html element which will be used to draw your model. You can just select this node by its `id` like this :
```javascript
var container = document.getElementById('container');
```

Use the render function of the viewer and your model url in order to automatically create your 3D illustration like so :

```javascript
nakerpearl.render({
  container: document.getElementById('container'),
  model: 'https://asset.naker.io/model/icosphere.gltf',
});
```

## Options

You can also add some options to the render function. Here is the list of the available once :

| Name           | Type         | Default      | Description                                                          |
| :------------- | :----------: | :----------: | -------------------------------------------------------------------- |
| modelFollowMouseRapidity  | _number_    | `1`       | Choose how fast the model rotates when the mouse is moving. Set it to 0 if you don't want it to rotate at all                                      |
| lightFollowMouseRapidity  | _number_    | `0`       | Choose how fast the light moves when the mouse is moving. Set it to 0 if you don't want it to move at all                                      |

```javascript
nakerpearl.render({
  container: document.getElementById('container'),
  model: 'https://asset.naker.io/model/icosphere.gltf',
  modelFollowMouseRapidity: 1,
  lightFollowMouseRapidity: 1,
});
```

If you need a specific options, we are open to it. Juste create an issue to share your idea and discuss it.

## Callback

It is possible to add a callback as a second argument of the render function, this function will be called when the model is loaded. The callback returns the pearl object :

```javascript
nakerpearl.render({
  container: document.getElementById('container'),
  project: 'your-project-id',
}, (pearl) => {
  // model loaded, do what you need!
});
```

## Examples

To see it in action, follow this link:  
[Pearl viewer](https://codepen.io/pichou/pen/dLaaBW)  
