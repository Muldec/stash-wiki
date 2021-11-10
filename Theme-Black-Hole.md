&nbsp;
# Install

**1.** Open User **Interface** Configuration panel in **settings**. ( http://localhost:port/settings?tab=interface ) 

**2.** Tick/Enable Custom CSS ✅ 

**3.** Copy&Paste [CSS Code](#css-code) to the Custom CSS text area. 

# Notes

Just a simple all black theme.<br>
Everything in this css is commented, so if you don't like something just remove it!<br>
Don't like the color of the border, or the border at all, change it or remove it!<br>
If you're not sure DM me on Discord.

# Important changes
1. By default scrubber is hidden.<br>
2. By default hovering on performers images when checking them below a scene/gallery makes them bigger, useful if you're not really sure who the hell is that person!!! This is a little tricky when you have a lot of performers on an item but I manage to check them all. To achieve this I had to "break" tags, now they never to go a new line.<br>
3.  Made checkboxes, on scenes/galleries/etc., a little bigger so it's easier to click on them and not on the item itself.<br>
4. Removed transparency from logos when on scenes/etc., it's easier to see them and it's not a big deal since they disappear when you hover on an item to check it.<br>
5. You can set a custom background from an online image and yes you can use gifs but mind the size :)<br>
By default it's set to "contain" so if the image is extremely small, well you get the catch... shouldn't be a problem with bigger images.

&nbsp;

Have fun and in doubt you should find me on Discord!

&nbsp;


# CSS Code



```css
/* Black Hole Theme by BViking78 v1.0 */
/* STASH GENERAL */
/* Set Background to Black & Optional Custom Image */
body {
	background: black url("") no-repeat fixed center;
	background-size: contain;
}

/* Change Top Nav Bar Colors */
.bg-dark {
    background-color: #000000!important;
}

/* Set Red Border on Button on Hover */
.btn-primary.btn:hover {
  border: 1px solid red;
}

/* Set Background to Transparent for Tags/Performers Popups*/
.fade.hover-popover-content {
  background: transparent;
}

/* Zoom Performers image when Hover*/
.hover-popover-content {
  max-width: initial;
}
.image-thumbnail:hover {
  height: 100%;
}

/* Set Opacity Studio Logo to 100% */
.scene-studio-overlay {
	opacity: 100%;
}

/* Making Checkbox Slightly Bigger */
.grid-card .card-check {
	top: 0.9rem;
	width: 1.75rem;
}

/* Center Titles on Cards */
.grid-card a .card-section-title {
	text-align: center;
}

/* STASH MAIN PAGE*/
/* Change Card Header Color */
.card-header {
  background: black;
  border: 1px solid white;
}
/* Change Markdown Color */
.card-body {
  background: black;
  border: 1px solid white;
}

/* STASH SCENES*/
/* Cards Section */
.card-section {
  background: black;
}

/* Cards Bottom */
.card-popovers {
  background: transparent;
}
.scene-card {
  background: black;
  border: 1px solid red;
}

/* SCENE PAGE */
/* Hide the scene scrubber */
.scrubber-wrapper {
  display: none;
}

/* IMAGES*/
/* Set Cards Background to Black */
.image-card {
	background: black;
	border: 1px solid red;
}

/* GALLERIES */
/* Set Cards Background to Black */
.gallery-card {
	background: black;
	border: 1px solid red;
}

/* PERFORMERS */
/* Set Cards to Black */
.performer-card {
	background: black;
	border: 1px solid red;
}

/* STUDIOS */
/* Set Cards to Black */
.studio-card {
	background: black;
	border: 1px solid red;
}

/* TAGS */
/* Set Cards to Black */
.tag-card {
	background: black;
	border: 1px solid red;
}

/* SETTING */
/* Left Menu to Black */
.col {
	background: black;
}
/* Setting Text Input Border to White */
.input-control, .text-input {
	border: 1px solid white;
}
```