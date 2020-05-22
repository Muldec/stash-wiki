**Custom CSS** allows you to modify Stash's stock style sheets.

The following is a list of some useful CSS snippets. You may use them by copying-and-pasting them into the Custom CSS editor found in the `Settings` > `Interface Configuration` panel or by navigating to `127.0.0.1:9999/settings?tab=interface`

Note: Future releases of Stash may break these CSS tweaks. CSS tweaks may not appear without flushing the Stash browser cache first on Chrome.

# Scenes

## Fit more thumbnails on each row
Reduce left and right padding on Scene and Performer grid pages allowing for more thumbnails on each row.

```css
.grid { padding: 0px !important; }`
```

## Allow for longer string when displaying "Studio as Text" on scene thumbnails

```css
.scene-studio-overlay {
	font-weight: 600 !important;
	opacity: 1 !important;
	width: 60% !important;
	text-overflow: ellipsis !important;
}
```

## Hide scene specs (resolution, duration) from scene card

```css
.scene-specs-overlay {
  display: none;
}
```

## Hide studio logo/text from scene card

```css
.scene-studio-overlay {
  display: none;
}
```
## Make the list of tags take up less width
```css
.bs-popover-bottom {
  max-width: 500px
}
```

# Performers

## Show entire performer image in performer card

```css
.performer.image {
  background-size: contain !important;
}
```

# Galleries

## Grid view for galleries

```css
.col.col-sm-6.mx-auto.table .d-none.d-sm-block {
    display: none !important;
}
.col.col-sm-6.mx-auto.table .w-100.w-sm-auto {
    width: 175px !important;
    background-color: rgba(0, 0, 0, .45);
    box-shadow: 0 0 2px rgba(0, 0, 0, .35);
}
.col.col-sm-6.mx-auto.table tr {
    display: inline-table;
}
```