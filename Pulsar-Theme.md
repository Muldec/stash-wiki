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
/*	StashApp Pulsar Theme - Fonzie 2020 v1.1.0	*/

/* ================= General ===================== */

body {
	background-image:url("https://i.imgur.com/gQtSoev.jpg");	/*	Aphonus		*/
/*	background-image:url("https://i.imgur.com/6BBd6aa.jpg");	/*	Plex		*/
/*	background-image:url("https://i.imgur.com/xAzxryr.jpg");	/*	Almora		*/
/*	background-image:url("https://i.imgur.com/0iN75zD.jpg");	/*	Dacirus		*/
/*	background-image:url("https://i.imgur.com/g5ECcdD.jpg");	/*	Drionope	*/
/*	background-image:url("https://i.imgur.com/dhVsc3d.jpg");	/*	Elein		*/
/*	background-image:url("https://i.imgur.com/B5hdvQG.jpg");	/*	FreePhion	*/
/*	background-image:url("https://i.imgur.com/LcSat6V.jpg");	/*	Lilac		*/
/*	background-image:url("https://i.imgur.com/kn9wixj.jpg");	/*	Nolrirus	*/
/*	background-image:url("https://i.imgur.com/190rDim.jpg");	/*	Ongion		*/
/*	background-image:url("https://i.imgur.com/IpvdJVn.jpg");	/*	PurpleRough 	*/
/*	background-image:url("https://i.imgur.com/hAHylub.jpg");	/*	Tesioria	*/
	background-image:url("./background.jpg");		/*	Local Background Image	*/
    
	width: 100%;
	height: 100%;
	padding: 0 0 0;
	background-size: cover;
	background-repeat: no-repeat;
	background-color:#127aa5;
	background-attachment: fixed;
	background-position: center;
}

* {scrollbar-color: hsla(0, 0%, 80%, .35) transparent;}



.main { margin-top:20px }
.top-nav {
    padding: .13rem 1rem;
}

.fixed-bottom, .fixed-top { position: relative !important; top:0px !important}

.filter-container, .operation-container {
    background-color: rgba(0, 0, 0, .22);
    box-shadow: none;
    margin-top: 6px;
    border-radius: 5px;
    padding: 5px;
}



.bg-dark {background-color:#18587e !important}
.bg-dark {background: rgba(10, 20, 25, 0.48)!important;}

#root {
	position: absolute;
	width: 100%;
	height: 100%;
	z-index: 2;
}

.order-2 button { margin-left: 4px }


.card {
	background-color: #30404d;
	border-radius: 6px;
	padding: 20px;
	margin: 4px 0.50% 12px;
	background-color: rgba(6, 20, 25, .32);
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .55);
}
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
 
.btn-secondary {
    color: #eee;
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
 
.nav-tabs .nav-link.active {
    color: #eee;
}
 
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
 
.btn-primary:not(:disabled):not(.disabled).active,
.btn-primary:not(:disabled):not(.disabled):active,
.show>.btn-primary.dropdown-toggle {
	color: #fff;
	background-color: rgba(22, 50, 60, .74);
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







/* ========== Performer =============== */

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


.container-fluid {
	width:96%!important; 
	min-width:920px; 
	margin-left: auto !important; 
	margin-right: auto !important; 
}

.performer.image {
  background-size: contain !important;
}

#performer-page .performer-image-container .performer 
{
    background-color: rgba(0, 0, 0, .48);
    box-shadow: 5px 5px 7px rgba(0, 0, 0, .42);
    border-radius: 14px !important;
}

.performer-card, .card-image {  width: 205px; }

.performer-card-image {object-fit: fill !important}
.performer-card-image, .justify-content-center .card-image 
{ height:306px }
.card { border-radius: 10px !important; }

.flag{text-align:left; margin-top:-1px; margin-left:-8px; }
.flag-img { width: 26px; margin-right:10px }
.performer-card .flag-icon {
    height: 2rem;
    left: 0.5rem !important;
    bottom: 0.15rem;
    width: 27px; 
}


.text-muted {text-align:right}

.card-section {
margin-bottom: -4px !important;
padding: .5rem 0.7rem 0 !important;
}


.card-section span {margin-bottom:3px}


.rating-banner {
padding: 8px 41px 6px;
line-height: 1.1rem;
transform: rotate(-41deg);
top: 8px }



/* ========== Performer Page =============== */


#performer-details-tabpane-details .text-input, 
#performer-details-tabpane-details .text-input:disabled, 
#performer-details-tabpane-details .text-input[readonly] {
    background-color: rgba(16,22,26,0.0);
}

.text-input, input.form-control-plaintext 
{
    background-color: none !important;
}

#performer-details  .input-control, .text-input { box-shadow: none; }

#performer-details-tabpane-details
{    background-color: rgba(16,22,26,0.28); }

#performer-details-tabpane-details td {    padding: 8px; }
#performer-details-tabpane-details tr:nth-child(odd) { background-color: rgba(16,22,26,0.1); }
table#performer-details {color:#FFF; text-shadow: 1px 1px 1px #000 !important}




/* ============ Scenes ============ */


/*.card-section p {display:none} */

.scene-card.card hr, .scene-card.card>hr{
	border-top: 0px solid rgba(0,0,0,.1);
}

.search-item {
    background-color: none;
    background-color: rgba(16,22,26,0.27) !important;
}

.btn-secondary.disabled, .btn-secondary:disabled {
    background-color: none;
    background-color: rgba(16,22,26,0.67) !important;
}

.scene-studio-overlay {
    opacity: .75;
    top: -4px;
}
.scene-studio-overlay {
    right: 2px;
}
.scene-specs-overlay {bottom:0px;
    color: #fff;
    font-weight: bold;
    letter-spacing: 0.00rem;
    text-shadow: 1px 1px 2px #000;
}


.zoom-0 {margin: 4px 0.25% 10px; !important }

.zoom-1 {width: 335px!important}
.zoom-2 {width: 425px!important}
.zoom-1 .video-section {object-fit: cover !important;height:187px;overflow:hidden;}
.zoom-1 .scene-card-preview { height: 188px; }
.zoom-1 .scene-card-video {width: 348px; min-height:209px; max-height: 405px; height:auto; object-fit: cover !important; margin-top:-2%; margin-left:-6px; zoom:103%;  }

.zoom-2 .video-section {height:240px; object-fit: cover !important; overflow:hidden;}
.zoom-2 .scene-card-video {min-height:199px; height:auto; object-fit: cover !important; margin-top:-2%; zoom:103%;  }


.scene-card-link {height:195px; overflow:hidden;}

.scene-popovers, .card-popovers { 
margin-bottom: 3px;
margin-top:-44px;
justify-content: flex-end;
}


/* .overlay-resolution {display:none} */


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

.scene-popovers .fa-icon {margin-right: 4px;}



.scene-card.card .rating-banner {
padding:0;
left:5px;
top: 88%;
background-position: left;
font-size: .01rem;
-webkit-transform: rotate(0deg);
transform: rotate(0deg);
}

.zoom-0.card .rating-banner {top: 81% !important;}
.zoom-2.card .rating-banner {top: 91% !important;}
.zoom-3.card .rating-banner {top: 92% !important;}


h5.card-section-title {font-family: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI" !important; font-size: 1.22rem; font-weight:bold; line-height:132%; text-shadow: 2px 2px 1px #000 !important}


.performer-head h2 {font-family: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI" !important; font-weight:bold; text-shadow: 2px 2px 2px #111 }
#performer-page .performer-head .name-icons {
    margin-left: 20px;
}

#performer-page .col-sm-6 { 
flex: 0 0 64%;
max-width: 64%;
}

#performer-page .offset-sm-1 {
    margin-left: 1%;
}



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

.fixed-bottom, .fixed-top { position: absolute; top:1px}


.zoom-1 {width:350px}
.col-sm-9 {
    flex: 0 0 80%;
    max-width: 80%;
}








/* ============== TAGS =============== */


.tag-card {	margin: 4px 0.45% 10px;	padding:0px;}
.tag-card.zoom-0 {    width: 335px;	height:230px;}
#tags .card {padding:0 0 10px 0 !important; }

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

.movie-card .text-truncate {
	font-size: 17px !important;
	max-width:200px;
}

.movie-card-header {height:320px}

.movie-card-header .rating-banner {
	font-size: .006rem;
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




/* ==============  MISC ==============  */


.svg-inline--fa.fa-w-18 {
    width: 1.4em;
}


.btn-primary { margin:0 -3px 0 -10px}
.nav-link > .minimal {  margin: 1px;}


.wall-item-container {
    height: 97%; }

input[type=range].zoom-slider{ max-width:140px;width:140px }



.tag-item {
	background-color: #556699;
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
```