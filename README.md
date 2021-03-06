# inuit-flexgrid

Flexbox grid for [inuitcss](https://github.com/inuitcss/inuitcss).

Support for IE9 currently prevents inuitcss from using the flexbox layout mode. This plugin serves as an alternative to the core layout system.

## Installation

npm:

```
npm install inuit-flexgrid --save
```

Yarn:

```
yarn add inuit-flexgrid
```

Import the plugin in the *objects* section of main.scss:

```scss
@import "node_modules/inuit-flexgrid/objects/objects.grid";
```

## Examples

Cells are full-width and will stack on top of each other by default:

```html
<div class="o-grid">
  <div class="o-grid__cell">
  </div>
  <div class="o-grid__cell">
  </div>
</div>
```

Cells will in most cases be accompanied by utility classes that divide the grid into fractions. These are provided by inuitcss:

```html
<div class="o-grid">
  <div class="o-grid__cell u-1/2">
  </div>
  <div class="o-grid__cell u-1/2">
  </div>
</div>
```

## Modifier classes

Several modifier classes are provided. For example, `o-grid--auto` will divide the space equally between all containing cells without the need for width utility classes.

```html
<div class="o-grid o-grid--auto">
  <div class="o-grid__cell">
    50%
  </div>
  <div class="o-grid__cell">
    50%
  </div>
</div>
```

`o-grid` can be used with the following modifiers:

* `o-grid--flush`: Remove gutters.

* `o-grid--auto`: Automatically size cells by distributing them equally.

* `o-grid--center`: Horizontally center cells. Uses `justify-content: center`.
* `o-grid--right`: Align cells right. Uses `justify-content: flex-end`.
* `o-grid--left`: Align cells left. Uses `justify-content: flex-start` (which is default).

* `o-grid--middle`: Vertically center cells. Uses `align-items: center`.
* `o-grid--bottom`: Align cells to the bottom. Uses `align-items: flex-end`.

* `o-grid--around`: Distribute free space around the cells. Uses `justify-content: space-around`.
* `o-grid--between`: Distribute free space between the cells. Uses `justify-content: space-between`.

* `o-grid--reverse`: Place cells from right to left. Uses `flex-direction: row-reverse`.


## Configuration

### Gutter size

The default gutter size is equal to `$inuit-global-spacing-unit`. You can change the default by setting the `$inuit-flexgrid-gutter-width` variable before importing the grid object:

```scss
$inuit-flexgrid-gutter-width: 26px;
@import "node_modules/inuit-flexgrid/objects/objects.grid";
```
