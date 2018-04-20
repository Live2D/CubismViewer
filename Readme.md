# Cubism DIY Viewer

Welcome to the *Unity*-based Cubism 3 do-it-yourself viewer. Came here looking for the official Live2D homepage?
Go [here](http://www.live2d.com/products/cubism3).


## Do-it-yourself!?

Instead of providing a complete solution like the 2.x viewers did,
this project aims to serve as a starting point and to provide common functionality
for making it easy to create a viewer tailored to your needs.

Want to preview models easily without access to *Unity*? Create a viewer with built-in functionality.

Need model related data in your app that you can't create in Cubism itself?
Customize the viewer to create just the data you need.


## Design

The viewer itself basically is a single `MonoBehaviour`.
You customize the viewer by attaching other `MonoBehaviour`s to it.
As *Plugin* is a somewhat reserved term in *Unity* (and because I like *Ruby*),
let's call such custom behaviours *gem*s.


## Built-in *Gem*s

This project contains a few *gem*s to get you started.


### `CameraControls`

This *gem* allows you to move the canvas and zoom-in.
Hotkeys default to `Spacebar + Left Mouse Button + Drag` for navigating the canvas, and
`Mouse Wheel Scroll Up/Down` for zooming.


### `SimpleAnimator`

This *gem* allows you to play back a single animation at a time.


### `TwoColorThemer`

This *gem* allows you to quickly theme the viewer using a 2 color theme.
The background color will be set to the primary color of the theme.
You can register any number of UI elements you want themed, too, through the *Inspector*.
Hotkey defaults to `Left Control + T` for switching between themes.


## User *Gem*s

- [DenchiSoft/CubismViewerGems](https://github.com/DenchiSoft/CubismViewerGems)


## Getting Started

First, you have to download a few files and get them into a *Unity* project:

1. Download the latest [SDK](https://live2d.github.io/#unity) and import it into your project.
1. Make sure to restart *Unity*.
1. Download the latest [Components for Unity](https://github.com/Live2D/CubismUnityComponents/tree/develop) into your project. Overwrite any previous SDK files with the new ones.
1. Download/Clone this repository into your project.
1. Copy the *Mono* `System.Windows.Forms.dll` into your project. (Check out `./Assets/Live2D/Cubism/Viewer/Plugins/System.Windows.Forms.txt` for instructions).
1. Set `API Compability Level` to *.NET 2.0* (default is *.NET 2.0 Subset*) in the *Player Settings*.

From here things are easy because you do the rest completely inside the *Unity Editor*:

6. Create an empty *GameObject* and add the `CubismViewer` component to it.
1. Assign the `Main Camera` in your scene to the `CubismViewer` through the *Inspector*.
1. Create an UI button and add the `CubismViewer.ShowFileDialog` method of the `CubismViewer` object to `On Click ()`.
1. Hit play, click the UI button. A file dialog should open.
1. Select a `model3.json` file via the file dialog. The model should be displayed.
1. Add *gem*s to the `CubismViewer` object for additional functionality.


## Contributing

Wrote a cool *gem*? We're looking forward to it.
You can either submit its source code or a link (as Live2D Community or as pull requests).

Besides that, there are many other ways to contribute to the project, too:
logging bugs, submitting pull requests on this GitHub, and reporting issues and making suggestions at Live2D Community.


### Forking And Pull Requests

We very appreciate your pull requests whether they bring fixes, improvements, or even new features.  
Note, however, that the wrapper is designed to be as lightweight and shallow as possible and
should therefore only be subject to bug fixes and memory/performance improvements.  
To keep the main repository as clean as possible, create a personal fork and feature branches there as needed.


### Bugs

We are regularly checking issue-reports and feature requests at Live2D Community.
Before filing a bug report, please do a search in Live2D Community to see if the issue-report or feature request has already been posted.
If you find your issue already exists, make relevant comments and add your reaction.


### Discussion Etiquette

Please limit the discussion to English and keep it professional and things on topic.


## License

If you plan on using this project or parts of it for non-personal or non-in-house use,
make sure to read the [license](http://live2d.com/eula/live2d-open-software-license-agreement_en.html) carefully.
Otherwise, you shouldn't have to worry to much as the license that applies to the source code in this project
allows you to modify all sources without the need to submit any changes you made.
