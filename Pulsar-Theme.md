 # Pulsar Theme for StashApp

&nbsp;
<p align="center">
    <a href="https://discord.gg/2TsNFKt">
        <img src="https://img.shields.io/discord/559159668438728723.svg?logo=discord" alt="Discord" />
    </a>
</p>

<img src="https://i.imgur.com/I8A2PwH.jpg" />
&nbsp;

A new custom theme for Stash. Installation is quick and easy so you should be ready to install it in just a few simple steps. 

Feel free to experiment with CSS and modify it to fit your needs. In case you have any issues or improvements we will be happy to hear from you on our **[Discord server](https://discord.gg/2TsNFKt)**!

The Theme will only change the look&feel of the Stash interface. It **will not** affect any other data, so you are all safe and sound! :heart:

&nbsp;

# Install

**1.** Open User **Interface** Configuration panel in **settings**. ( http://localhost:9999/settings?tab=interface ) 

**2.** Tick/Enable Custom CSS ✅  

**3.** Copy&Paste [CSS Code](#css-code) to the Custom CSS text area. 

**4.** Select one of the background images that you find at the top of the CSS code by removing the commentary ( _/*_ ) at the beginning of the line (_Aphonus_ is the standard background), or download the image as _"background.jpg"_, and place the image in `~/.stash` on macOS / Linux or `C:\Users\YourUsername\.stash` on Windows.

![Background Image Preview](https://i.imgur.com/4VChBGk.jpg)





&nbsp;


Enjoy!


&nbsp;


# CSS Code



```
/*	StashApp Pulsar Theme - Fonzie 2020 v1.1.2	*/

/* ========= General ========= */

body {
	background-image:url("https://i.imgur.com/gQtSoev.jpg");	/*	Aphonus	*/
/*	background-image:url("https://i.imgur.com/6BBd6aa.jpg");	/*	Plex		*/
/*	background-image:url("https://i.imgur.com/xAzxryr.jpg");	/*	Almora	*/
/*	background-image:url("https://i.imgur.com/0iN75zD.jpg");	/*	Dacirus	*/
/*	background-image:url("https://i.imgur.com/g5ECcdD.jpg");	/*	Drionope	*/
/*	background-image:url("https://i.imgur.com/dhVsc3d.jpg");	/*	Elein	*/
/*	background-image:url("https://i.imgur.com/B5hdvQG.jpg");	/*	FreePhion	*/
/*	background-image:url("https://i.imgur.com/LcSat6V.jpg");	/*	Lilac	*/
/*	background-image:url("https://i.imgur.com/kn9wixj.jpg");	/*	Nolrirus	*/
/*	background-image:url("https://i.imgur.com/190rDim.jpg");	/*	Ongion	*/
/*	background-image:url("https://i.imgur.com/IpvdJVn.jpg");	/*	PurpleRough */
/*	background-image:url("https://i.imgur.com/hAHylub.jpg");	/*	Tesioria	*/
/*	background-image:url("./background.jpg");				/*			*/
    
	width: 100%;
	height: 100%;
	padding: 0 0 0;
	background-size: cover;
	background-repeat: no-repeat;
	background-color:#127aa5;
	background-attachment: fixed;
	background-position: center;
}



/* --- Makes the background of the Navigation Bar at the Top half-transparent --- */
.bg-dark {background: rgba(10, 20, 25, 0.50)!important;}

/* --- The space between the Navigation Bar and the rest of the page --- */
.main { margin-top:18px }
.top-nav { padding: .13rem 1rem; }

/* --- Changes how the Bar at the top of the page behaves --- */
.fixed-bottom, .fixed-top { position: relative !important; top:0px !important}

/* The pagination at the top and at the bottom of the Scenes/Performer/Images/... pages; 
transparent background, rounded corners, etc. */
.filter-container, .operation-container {
    background-color: rgba(0, 0, 0, .22);
    box-shadow: none;
    margin-top: 6px;
    border-radius: 5px;
    padding: 5px;
}


/* --- The width of the page. Leaves some more space left and right. --- */
.container-fluid {
	width:96%!important; 
	min-width:920px; 
	margin-left: auto !important; 
	margin-right: auto !important; 
}




/* --- Changes the space between the button in the top right corner of the page --- */
.order-2 button { margin-left: 4px }


/* Each item on the Scenes/Performers/Tags/... pages */
.card {
	padding: 20px; 
	margin: 4px 0.50% 12px;
	background-color: rgba(6, 20, 25, .32);
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .55);
}

/* --- Increases the rounded borders of each item on the Scenes/Performers/... pages for 6px in 10px --- */
 .card { border-radius: 10px; }


.bg-secondary {
	background: none;
	background-color: rgba(5, 20, 25, .6) !important;
}
 
.text-white {
	color: #eee !important;
}




.border-secondary {
    border-color: #2f3335 !important;
}
 
.btn-secondary.filter-item.col-1.d-none.d-sm-inline.form-control {
    background-color: rgba(0, 0, 0, .08);
}

/* --- Changes the color and the background of the buttons and elements in the toolbar (Search, Sort by, # of Items, etc.) --- */
.btn-secondary {
    color: #f2f2f2;
    background-color: rgba(0, 0, 0, .08);
}
 
a {
    color: hsla(0, 10%, 95%, .75);
}
 
.btn.active {
    background-color: #2f3335;
    color: #f5f8fa;
}
 
minimal.w-100.active.btn.btn-primary {
    background-color: #2f4E72;
    color: #f5f8fa;
}
 
.btn-primary {
    color: #fff;
    background-color: #1f2326;
    border-color: #374242;
}

/*
.nav-tabs .nav-link.active {
    color: #eee;
}
*/





.nav-tabs .nav-link.active:hover {
    border-bottom-color: #eee;
    outline: 0;
}
 
.nav-tabs .nav-link {
    outline: 0;
}
 
.input-control,
.input-control:focus {
    background-color: rgba(16, 22, 26, .3);
}
 
 
.btn-primary:not(:disabled):not(.disabled).active,
.btn-primary:not(:disabled):not(.disabled):active,
.show>.btn-primary.dropdown-toggle {
    color: #fff;
    border-color: #eee;
}
 
.nav-pills .nav-link.active,
.nav-pills .show>.nav-link {
    color: #eee;
    background-color: #1f2326;
}
 
.btn-primary.focus,
.btn-primary:focus,
.btn-primary:not(:disabled):not(.disabled).active:focus,
.btn-primary:not(:disabled):not(.disabled):active:focus,
.show>.btn-primary.dropdown-toggle:focus {
	    box-shadow: none;
}

 
 
/* --- Changes the color of the active page in the Navgation Bar --- */ 
.btn-primary:not(:disabled):not(.disabled).active,
.btn-primary:not(:disabled):not(.disabled):active,
.show>.btn-primary.dropdown-toggle {
	color: #fff;
	background-color: rgba(22, 50, 60, .75);
	border-color: #eee;
}
 
 
 
input[type="range"]::-moz-range-track {
	background: hsla(0, 0%, 100%, .25);
}
 
input[type="range"]::-moz-range-thumb {
	background: #bcbcbc;
}
 
div.react-select__control {
    background-color: hsla(0, 0%, 39.2%, .4);
    color: #182026;
    border-color: #394b59;
    cursor: pointer;
}
 
.scene-wall-item-text-container {
    background: radial-gradient(farthest-corner at 50% 50%, rgba(50, 50, 50, .5) 50%, #323232 100%);
    color: #eee;
}
 
 
.container-fluid,.container-lg,.container-md,.container-sm,.container-xl {
    width: 100%;
    margin-right: 0px;
    margin-left: 0px;
 }







/* ================ Performer =============== */



/* --- Changes the width of the Performer Card from 280px to 205px and therefore the size of the image --- */
/* --- In Full screen HD 1920x1080 you now see 8 performers per row instead of 6 --- */
 .performer-card, .card-image {  width: 205px; }

/* --- Changes the height of the Performer Card from 420px to 306px to keep the 2x3 picture ratio --- */
.performer-card-image, .justify-content-center .card-image { height:306px } 



/* --- The name of the Performer. Different font, less space to the left & to the top, Text-Shadow --- */
.text-truncate { 
	margin-left:-2px; 
	margin-top: -2px; 
	width:120%; 
	font-family: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI" !important; 
	font-size: 20px; 
	line-height:26px; 
	font-weight:bold; 
	text-shadow: 2px 2px 1px #000 !important
}


/* --- Moves the Flag icon from the right side of the card to the left and makes the Flag image a little bit bigger --- */
.performer-card .flag-icon {
	height: 2rem;
	left: 0.6rem;
	bottom: 0.15rem;
	width: 28px; 
}

/* --- Age and # of Scenes move from the left side to the right of the card --- */
.text-muted {text-align:right}

/* --- Text Shadow for the "Stars in x scenes" link --- */
div.card.performer-card div.text-muted a {text-shadow: 1px 2px 2px #333}

/* --- Makes the card section (Name, Age, Flag, # of scenes) more compact --- */
.card-section { margin-bottom: -8px !important; padding: .5rem 0.7rem 0 !important;}
.card-section span {margin-bottom:3px}

/* --- Moves the "Favorite" banner a little more to the top left corner --- */
.rating-banner {
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(-41deg);
	top: 8px 
}






/* ==================== Performer Page ======================= */
/* === The page that you see when you click on the picture of a Performer === */

/* --- The picture of the Performer on the left. 3D effect thanks to background shadows and more rounded corners --- */
#performer-page .performer-image-container .performer 
{
    background-color: rgba(0, 0, 0, .48);
    box-shadow: 6px 6px 11px rgba(0, 10, 10, .62);
    border-radius: 14px !important;
}

/* --- Without this the shadow at the bottom from the previous Selector will not be correctly displayed --- */
.performer-image-container {padding-bottom: 11px}


/* --- The following 9 Selectors change the way the details box is displayed --- */
#performer-details-tabpane-details .text-input, #performer-details-tabpane-details .text-input:disabled, 
#performer-details-tabpane-details .text-input[readonly] {background-color: rgba(16,22,26,0.0);}

.text-input, input.form-control-plaintext { background-color:none;}
#performer-details .input-control, .text-input {box-shadow: none;}

#performer-details-tabpane-details { background-color: rgba(16,22,26,0.28); border-radius: 8px}
#performer-details-tabpane-details td { padding: 9px; }
#performer-details-tabpane-details tr:nth-child(odd) {     background-color: rgba(16,22,26,0.1); }
table#performer-details {color:#FFF; text-shadow: 1px 1px 1px #000;}
table#performer-details tbody tr td:nth-child(1), td:first-child {padding-left: 22px; width: 185px;}



/* --- Changes the way the name of the performer is displayed --- */
.performer-head h2 {font-family: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI" !important; font-weight:bold; text-shadow: 2px 2px 2px #111 }

/* --- Leave some space between the name and the Fav/Link/Twitter/IG icons --- */
#performer-page .performer-head .name-icons {margin-left: 22px}








/* ============ Scenes ============ */


/* --- Remove the comments if you don't want to see the Description Text of the scenes --- */
/* .card-section p {display:none} */


/* --- Remove the comments if you don't want to see the Resolution of the Video (480p, 540p, 720p, 1080p) --- */
/* .overlay-resolution {display:none} */



/* --- The name of the Scene. Different font, less space to the left and to the top, Text-Shadow --- */
h5.card-section-title {font-family: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI" !important; font-size: 1.22rem; font-weight:bold; line-height:132%; text-shadow: 2px 2px 1px #000 !important}


/* --- Removes the horizontal line that separates the date/description text from the Tags/Performer/etc. icons --- */
.scene-card.card hr, .scene-card.card>hr{
	border-top: 0px solid rgba(0,0,0,.01); 
}


/* --- Changes regarding the Scene Logo --- */
.scene-studio-overlay {
	opacity: .80;
	top: -3px;
	right: 2px;
}

/* --- The Resolution and the Time/Length of the video in the bottom right corner to make it easier to read --- */
.scene-specs-overlay {
	bottom:0px;
	color: #FFF;
	font-weight: bold;
	letter-spacing: 0.00rem;
	text-shadow: 1px 1px 2px #000;
}

/* --- Changes the spaces between the items on the Scenes page --- */
.zoom-0 {margin: 4px 0.25% 10px; !important }

/* --- Changes the size of the items on the Scenes page --- */
.zoom-1 {width: 335px!important}
.zoom-2 {width: 425px!important}


/* Improves the way the scene picture is displayed when the resolution isn't 16:9 (e.g. 4:3) --- */
.zoom-1 .video-section {object-fit: cover !important;height:187px;overflow:hidden;}
.zoom-1 .scene-card-preview { height: 188px; }
.zoom-1 .scene-card-video {
	width: 348px; 
	min-height:209px; 
	max-height: 405px; 
	height:auto; 
	object-fit: cover !important; 
	margin-top:-2%; 
	margin-left:-6px; 
	zoom:103%;  
}
.zoom-2 .video-section {height:240px; object-fit: cover !important; overflow:hidden;}
.zoom-2 .scene-card-video {min-height:199px; height:auto; object-fit: cover !important; margin-top:-2%; zoom:103%;  }


.scene-card-link {height:195px; overflow:hidden;}


/* --- Moves the Tags-, Performer-, O-Counter-, Gallery- and Movie-Icon from below the description to the bottom right corner of the card --- */
.scene-popovers, .card-popovers { 
	margin-bottom: 3px;
	margin-top:-44px;
	justify-content: flex-end;
}


/* --- Tightens the space between the Tags-, Performer-, O-Counter-, Gallery- and Movie-Icons --- */
.btn-primary { margin:0 -3px 0 -10px}




/* -- The whole section replaces the ratings banner with a star rating in the bottom left corner --- */ 
.rating-1 {width:22px}
.rating-2 {width:43px}
.rating-3 {width:65px} 
.rating-4 {width:86px}  
.scene-card.card .rating-5 {background:none;width:108px}
.rating-1, .rating-2, .rating-3, .rating-4, .scene-card.card .rating-5 {
	background:none;
	background-image:url("https://i.imgur.com/YM1nCqo.png");
	height:20px;
	background-size: 108px 20px;
} 

.scene-card.card .rating-banner {
	padding:0;
	left:5px;
	top:88%;
	background-position: left;
	font-size: .01rem;
	-webkit-transform: rotate(0deg);
	transform: rotate(0deg);
}

.zoom-0.card .rating-banner {top: 81%}
.zoom-2.card .rating-banner {top: 91%}
.zoom-3.card .rating-banner {top: 92%}






/* --- Improves how the Preview Videos in the Wall View are displayed --- */
.wall-item-container { height: 100%; }
.wall-item-media { height: auto;  width: 101%;     background-color: rgba(0, 0, 0, .0);}
.wall-item-text {margin-bottom:2px; color: #222; text-shadow: 1px 1px 1px #fff }
.wall-item-container {background-color: rgba(0, 0, 0, .20); }
.wall-item { height: auto; max-height:254px }



.scene-popovers .fa-icon {margin-right: 2px;}





/* ============== Studio ================= */


.studio-card {
	padding: 0 !important;
	padding-bottom:14px !important;
}

.studio-card-image {
	max-height: 175px;
	height:175px;
}
.studio-card .card-section {
	margin-top: 22px !important;
}



.zoom-1 {width:350px} 
.col-sm-9 {
	flex: 0 0 80%;
	max-width: 80%;
}








/* ============== TAGS =============== */


.tag-card { margin: 4px 0.45% 10px; padding:0px;}
.tag-card.zoom-0 { width: 335px; height:230px;}
#tags .card {padding:0 0 10px 0; }

.zoom-0 .gallery-card-image, .zoom-0 .tag-card-image {
	max-height: 195px;height:190px
}


.tag-card-header {height:190px;overflow:hidden;}

.zoom-0 .tag-card-image {
	zoom: 101%;
	object-fit: cover;
	overflow:hidden;
	width: 338px;
	margin-top: -2px;
	margin-left: -1%;
/*margin-bottom:7px;*/
}

.tag-card .scene-popovers, .tag-card .card-popovers { 
	margin-bottom: 4px;
	margin-top:-34px;
	padding-left:17px;
}

.zoom-0 .tab-pane .card-image { height:210px }




/* ==============  MOVIES ==============  */
/* --- Changes the width of the items so only the front cover is displayed. Also replaces the ratings banner with a star rating --- */

.movie-card .text-truncate {
	font-size: 17px !important;
	max-width:200px;
}

.movie-card-header {height:320px}

.movie-card-header .rating-banner {
	font-size: .002rem;
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(0deg);
	padding: 0;
	left: 3px;
	top: 75% !important;
	height: 25px;
	background-size: 135px 25px;
	background-position: left;
}

.movie-card-header .rating-1 {width:28px}
.movie-card-header .rating-2 {width:55px}
.movie-card-header .rating-3 {width:83px} 
.movie-card-header .rating-4 {width:110px}  
.movie-card-header .rating-5 {width:138px}

.movie-card-header .rating-5 {
	background:none;
	height: 25px;
	background-size: 135px 25px;
}

.movie-card-image {
	height:330px;
	max-height: 330px;
	width: 233px;
}





/* ==============  IMAGES ==============  */

div.image-section .rating-banner {
	font-size: .002rem;
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(0deg);
	padding: 0;
	left: 3px;
	top: 80% !important;
	height: 25px;
	background-size: 135px 25px;
	background-position: left;
}

div.image-section .rating-1 {width:28px}
div.image-section .rating-2 {width:55px}
div.image-section .rating-3 {width:83px} 
div.image-section .rating-4 {width:110px}  
div.image-section .rating-5 {width:138px}

div.image-section .rating-5 {
	background:none;
	height: 25px;
	background-size: 135px 25px;
}






/* ==============  MISC ==============  */


.svg-inline--fa.fa-w-18 {
	width: 1.4em;
}


.nav-link > .minimal {  margin: 1px;}


/* --- Makes the Zoom Slider on the Scenes, Images, Galleries and Tags pages longer and therefore easier to use --- */
input[type=range].zoom-slider{ max-width:140px;width:140px; }


.tag-item {
	background-color: #126a95;
	color: #EEE;
	font-weight:bold;
	font-size: 13px;
	line-height: 18px;
	margin: 4px;
	padding: 4px 7px;
}

.tag-details .logo {
    background-color: rgba(0, 0, 0, .48);
    box-shadow: 3px 3px 5px rgba(0, 0, 0, .42);
    border-radius: 9px !important;
}

.search-item {
	background-color: none;
	background-color: rgba(16,22,26,0.27) !important;
}

.btn-secondary.disabled, .btn-secondary:disabled {
	background-color: none;
	background-color: rgba(16,22,26,0.67) !important;
}
```