#frame-scss
##Sassy CSS framework

Includes functions/mixins for media queries/breakpoints, flexible responsive grids, effects and shapes. Also included are some functions/mixins to more easily debug your own custom Sass :)

Work in progress, stay tuned!

###Main features
- Easy configuration of media queries and breakpoints. Set them the way you want or need them.
- 10, 11 or 12 columns? It doesn't matter, you define the widths and how each column reacts to different breakpoints.
- Cool transition mixin! Just define the easing, time and delay properties in the main `_frame.scss` and you're ready to go. Now all your transitions automatically have these same default properties.
- Lots of type check functions, sort functions, and more list and map related functions!
- Includes [normalize.css v3.0.2](git.io/normalize) and some other basic useful style classes.
- Some basic shapes and effects, such as hexagons, triangles, gradients and fancy text shadows.
- Extended debug functions and mixins. Output variables in the console or the compiled CSS to see what their actual values are. This makes developing your own stuff even easier :)

###How to use
1. Copy the `_frame.scss` and `_frame-basics.scss` files into your project folder.
2. Update the `@import` rules so they point to the right file(s) in the `source` folder of this package.
3. Now you can change the default values of the settings variables so it suits your project.

All main variables and settings are placed in `_frame.scss`. Here you can add colors, fonts, breakpoints, or custom variables specific for you project. If you need any of these values, just call the appropiate `frame-` function (eg. `$frame-colors` -> `frame-color()`). That's it. _Please note that removing any of the `$frame-` prefixed variables will break the framework._

In `_frame-basics.scss` you can remove (by adding comments) any predefined style classes wich you don't plan to use. This will keep the compiled CSS file clean and small.

If you plan to use the grid system or the predefined icon fonts functions, you must also copy the `_frame-grid.scss` and `_frame-iconfont.scss` files to your project folder. Don't forget to update the `@import` rules for these files too ;)

###To do:
- Add gaps to blockgrid (high)
- Optimize `frame-grid-columns` function (high)
- Optimize blockgrid output, combine selectors/breakpoints with the same width where possible (high)
- Optimize the output from `create-media-query` (eg. `@include add-breakpoint('xl' 'lg' 'md', 'max')` will no compile to `@media screen and (max-width: 1460px), screen and (max-width: 1219px), screen and (max-width: 1043px)` but must become `@media screen and (max-width: 1460px)`) (high)
- Add flexgrid grid system (medium priority as <= IE10 does not fully support flexbox)
- Complete `slice/splice` functions (medium)
- Complete `_sort-regular` function (medium)
- Extend documentation for certain functions (medium)
- Add table-/inlinegrid systems (low priority, perhaps even skip this one)
- Add more shapes (low priority)
- It's probably a good idea to create a couple of examples (low priority)
