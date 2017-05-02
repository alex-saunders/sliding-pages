[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/alex-saunders/sliding-pages)

# \<sliding-pages\>

[DEMO](https://alex-saunders.github.io/sliding-pages/components/sliding-pages/demo/)

`<sliding-pages>` is a simple carousel style element for moving between pages. The transitions are based on native app transitions and are implemented using the [FLIP](https://aerotwist.com/blog/flip-your-animations/) animation technique for optimal performance. Page transitions can be actived by either swiping left or right or by chaing the `active-index` property.

## Usage

The following code implements the `<sliding-pages>` element:

```html
<sliding-pages active-index="1">
  <div>
    <h1>
      Page 1
    </h1>
  </div>
  <div>
    <h1>
      Page 2
    </h1>
  </div>
  <div>
    <h1>
      Page 3
    </h1>
  </div>
</sliding-pages>
```

![Example](https://media.giphy.com/media/l0IydXtLion5ge2pW/giphy.gif)

## Properties
| Property      | Type          | Description                                                  |
| ------------- | ------------- | ------------------------------------------------------------ |
| active-index  | Number        | The index of the current active page (note: this is 0-based) |

`<sliding-pages>` has no public methods as it's behaviour is purely defined by the `active-index` property. I.e. to go to the next page, increment active-index and to go to the previous page, decrement. This property is both observed and reflects to attribute i.e. one can manually change the active-index property to trigger a page change or if the page is swiped left or right, the active-index property will update to display this.
