# SASS Mixins, variables and usage of an array

** Little exercise to define and use

## 1. Installing

*   Initialize a package.json (`npm init` and then answer the questions).
*   if you do not have [nodemon] installed (https://npmjs.org/package/nodemon) which will used to run tasks when changes are detected, install it globally (`npm i -g nodemon`)
*   [node-sass](https://npmjs.org/package/node-sass) which will compile the SCSS files into CSS (install it locally, as a development `npm i -D node-sass`)
*   Open the `package.json` and add "start" script like this:

    <pre>"scripts": {
      "start": "node-sass --watch --output dist --source-map true --source-map-contents sass --output-style compressed sass/styles.scss",
      "test": "echo \"Error: no test specified\" && exit 1"
    },</pre>

    Now, in the terminal, run `npm run start`.
    Make a change to your SCSS file and save to check.
*   If you want to run [live-server](https://npmjs.org/package/live-server), open a new tab in your terminal (`CTRL + SHIFT + T`) and run the command live-server.

## 2. Using the Variables

* See the predefined variable in the upper section of styles.scss
* Use them where aprobiate
* The cards' border radius is two times the predefined value. Try to use the variable with a mathematical operation

## 3. A mixin for horizontal lists

** There are several lists that are displayed horizontally. By using a mixin you could avoid repeating the same code over and over again. Think of the properties that all these lists have in common.

* Define a mixin called horizontal-list with the common properties in _mixin.scss
* use the mixin in styles.scss

## 3. A mixin for sprites

** Also the properties for icons sprites are always pretty much the same.

* Define a mixin called `icon-sprite` which accepts the parameters `$x` and `$y`
* `$x` and `$y` shall be used for the `background-position`
* use the mixin `icon-sprite` for the `.cards` :after pseudo element and adjust to show the correct icon for each sport which is indicated by the classes `basketball`, `baseball` or `soccer`

## 4. Looping through an array to generate color schemes

* Take a look at the example at the beginning of the file `_color-scheme.scss`
* A two dimensional array is defined there and the looped through. The aim is to generate different color schemes depending on the defined class name
* Do the exact same with the classnames `basketball`, `baseball` or `soccer` and their according colors which are given in a comment
* Try to describe what is happening at each step in comments.
