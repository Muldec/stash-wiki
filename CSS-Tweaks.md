**Custom CSS** allows you to modify Stash's stock style sheets.

The following is a list of some useful CSS snippets. You may use them by copying-and-pasting them into the Custom CSS editor found in the `Settings` > `Interface Configuration` panel or by navigating to `127.0.0.1:9999/settings?tab=interface`

Note: Future releases of Stash may break these CSS tweaks. CSS tweaks may not appear without flushing the Stash browser cache first on Chrome.

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