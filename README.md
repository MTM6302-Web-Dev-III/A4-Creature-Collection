# Start here

Run index.html through a local development server. Work in script.js below the supplied array. The empty gallery is intentional.

## Supplied controls
- `#theme`: values `forest`, `sky`, `desert`.
- `#layout`: values `cards`, `detailed`, `compact`.
- `#collection`: empty list where entries go.
- `#status`: live feedback paragraph.

CSS reads `data-theme` on `<body>` and `data-layout` on `#collection`. You can set these using `dataset` or `setAttribute()`.

## Entry structure
Generate this structure for each creature using a loop. Replace the example values with properties from the supplied array. Use DOM methods or HTML strings; do not manually repeat the cards in index.html.

```html
<li class="creature">
  <img src="assets/moss-dragon.svg" alt="A green dragon with leafy horns and small wings.">
  <div class="creature-info">
    <h3>Moss Dragon</h3>
    <p class="creature-description">A gentle gardener who grows tiny forests wherever it naps.</p>
  </div>
</li>
```

## Suggested build order
1. Generate the collection and confirm all images load.
2. Make the theme control change the body attribute.
3. Make the layout control change the list attribute.
4. Save both control values together after a change.
5. Check for saved data on startup and restore the controls and attributes.

All illustrations are supplied locally. No API, image downloads, frameworks, or build tools are needed.
