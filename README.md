[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)


# \<sliding-pages\>

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="sliding-pages.html">
    <link rel="import" href="../paper-styles/color.html">

    <style is="custom-style" include="demo-pages-shared-styles">
      .container {
        width: 100%;
        height: 80vh;
        position: relative;
        margin-bottom: 8px;
      }
      sliding-pages > div {
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        user-select: none;
        cursor: pointer;
      }
      paper-fab:nth-of-type(1) {
        left: 8px;
      }
      paper-fab:nth-of-type(2) {
        right: 8px;
      } 
      sliding-pages div:nth-of-type(1) {
          --page-background-color: var(--paper-red-500);
      }
      sliding-pages div:nth-of-type(2) {
          --page-background-color: var(--paper-blue-500);
      }
      sliding-pages div:nth-of-type(3) {
          --page-background-color: var(--paper-green-500);
      }
      sliding-pages div:nth-of-type(4) {
          --page-background-color: var(--paper-yellow-500);
      }
      sliding-pages div:nth-of-type(5) {
          --page-background-color: var(--paper-purple-500);
      }

      input {
        display: block;
        margin-top: 8px;
      }
    </style>
  </template>
</custom-element-demo>
```
-->
```html
<div class="container">
  <sliding-pages active-index="1">
    <div>
      <h1>
        Page 1
      </h1>
      <div>
        Child div
      </div>
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

    <div>
      <h1>
        Page 4
      </h1>
    </div>

    <div>
      <h1>
        Page 5
      </h1>
    </div>
  </sliding-pages>
  <button onclick="prevPage()">Previous Page</button>
  <button onclick="nextPage()">Next Page</button>
  <input type="number" placeholder="Page Index" id="pageIndex" value="1">
</div>
```
<!---
```
<custom-element-demo>
  <template>
    <script>
      const pages = document.querySelector('sliding-pages');

      function prevPage() {
        const currIndex = parseInt(pages.getAttribute('active-index'));
        pages.setAttribute('active-index', (currIndex - 1));
      }
      function nextPage() {
        const currIndex = parseInt(pages.getAttribute('active-index'));
        pages.setAttribute('active-index', (currIndex + 1))
      }

      const input = document.getElementById('pageIndex');
      input.addEventListener('change', (e) => {
        e.preventDefault();

        const index = parseInt(e.target.value);
        pages.setAttribute('active-index', index);
      })
    </script>
  </template>
</custom-element-demo>

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
