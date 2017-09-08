# Strapper
Making Bootstrap the rapid prototyping tool that it should be.

## Getting started
Out of the box file can be found at `src/css/strapper.min.css`.

Include the file after Bootstrap and before your own custom styles:
```html
<head>
  ...
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/css/bootstrap.min.css" integrity="sha384-rwoIResjU2yc3z8GV/NPeZWAv56rSmLldC3R/AZzGRnGxQQKnKkoFVhFQhNUwEyJ" crossorigin="anonymous">
  <link rel="stylesheet" href="...strapper.min.css">
  <link rel="stylesheet" href="...">
  ...
</head>
```

## Personalization
The source code can be found at `./src/scss/strapper.scss`. This can be edited to your own specifications and desires.

In order to do this, you can clone the repository by running:
```
$ git@github.com:ccabo1/strapper.git
```
Once this is completed, make sure your packages are up to date and configured:
```
$ npm install
```
To get to work, run:
```
$ gulp
```
Keep running this while you edit the `scss` file. Gulp will automatically compile the `scss` on save into the minified `css` file in the `css` folder. If there are any errors with compilation, they will come up in the terminal window running `gulp`.

If you have any problems or feature requests, [open an issue.](https://github.com/ccabo1/strapper/issues)

## Intuition
Bootstrap, in large part, does a great job of doing what it sets out to: Bootstrap websites are naturally responsive, mobile-first, structured, accessible, etc. The one place where Bootstrap needs improvement is, ironically enough, __bootstrapping__--that is, quickly putting together website for proof of concept that can later be personalized.

Strapper aims to fix this problem by adding a small set of classes on top of Bootstrap's existing framework to make positioning, sizing, and basic styling easier. I found myself repeatedly writing the very same classes for every project, so I thought it best to combine them into a reusable, modular CSS framework.

## Functionality

### Padding
Quickly add the padding you need to an element.
* `pad-0`: no padding at all
* `pad-1`: padding of `1rem`
* `pad-2`
* `pad-3`
* `pad-0-1`: no padding on top and bottom, `1rem` padding on either side
* `pad-0-2`
* `pad-1-0`
* `pad-2-0`
* `pad-1-2`
* `pad-2-1`

### Spacing
Add in a full-width spacer between elements.
* `space-0`: `0rem` tall spacer
  * Good especially with `inline` aligned items to ensure everything stays on the right line.
* `space-1`: `1rem` tall spacer
* `space-2`
* `space-3`
* `space-4`

### Margins
Customize space between elements with ease.
* `marg-0`: no margin
* `marg-top-0`: no top margin
* `marg-top-1`: `1rem` top margin
* `marg-top-2`
* `marg-bot-0`
* `marg-bot-1`
* `marg-bot-2`
* `marg-right-0`
* `marg-right-05`: `0.5rem` right margin
* `marg-right-1`
* `marg-left-0`
* `marg-left-05`
* `marg-left-1`

### Borders, lines, and dividers
Better organize your website with delineating borders and lines.
* `border`: standard gray border
* `light-border`: lighter gray border
* `line-0`: full-width line with no vertical margins
* `line-1`: fill-width line with `1rem` top and bottom margins
* `line-2`
* `light-line`: addition to `line` classes for a lighter color to match the `light-border`

### Coloring and typography
Quickly set standard colors and styles for text and elements alike.
* `black`: set the background to black
* `white`
* `light-gray`
* `gray`
* `white-blue`
* `purple`
* `green`
* `blue`
* `black-text`: set text color to black
  * `black-text-important`: set color to black in all cases
  * `black-text-hover`: set color to black on hover
* `white-text`
  * `white-text-important`: set color to black in all cases
  * `white-text-hover`: set color to black on hover
* `gray-text`
* `light-gray-text`
* `blue-gray-text`
* `blue-text`
* `purple-text`
* `green-text`
* `no-decoration`: remove decoration, especially underlining on link hover
* `bold`: bolden text
* `italic`: italicize text
* `caps`: capitalize text

### Shading
Add extended depth with shading classes.
* `shade-1`: lightest and shortest shadow
* `shade-2`
* `shade-3`
* `shade-4`: darkest and longest shadow
* `hover`: appended to a shade class to shorten and darken the element on hover

### Interactivity
Make elements do the job they are supposed to.
* `cursor`: changes the cursor to a `hand/pointer`--the same as when hovering a link, for example.
* `animate`: apply a `0.2s` transition to an element

### Positioning
Display elements the way you want them to.
* `absolute`: absolute position
* `fixed`: fixed position
* `relative`
* `inline`: display inline
* `block`: display block
* `full-width`: `100%` width
* `left`: text align left
* `float-left`: float items left
* `right`
* `float-right`
* `center`: full-width with center alignment
* `background-image`: center and properly size a background image
  * Use a unique ID to add the background image easily with CSS
  * `parallax`: give the background image a parallax scrolling effect on larger devices

### Modules
Additional, reusable modules for displaying information.
* `ul.horizontal`: horizontal, simple left-aligned list. Good for navigation and icons.
  * `right`: append this class in order to right align the horizontal form
  * Padding between items is `1rem` by default
