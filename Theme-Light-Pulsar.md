 # Light Pulsar Theme for StashApp

&nbsp;
<p align="center">
    <a href="https://discord.gg/2TsNFKt">
        <img src="https://img.shields.io/discord/559159668438728723.svg?logo=discord" alt="Discord" />
    </a>
</p>


<img src="https://i.imgur.com/kgh7m5X.jpg" />

<img src="https://i.imgur.com/14fjwYZ.jpg" />

<img src="https://i.imgur.com/Zs4rCOy.jpg" />

&nbsp;

A new custom theme for Stash. Installation is quick and easy so you should be ready to install it in just a few simple steps. 

Feel free to experiment with CSS and modify it to fit your needs. In case you have any issues or improvements we will be happy to hear from you on our **[Discord server](https://discord.gg/2TsNFKt)**!

The Theme will only change the look&feel of the Stash interface. It **will not** affect any other data, so you are all safe and sound! :heart:

&nbsp;

# Install

**1.** Open User **Interface** Configuration panel in **settings**. ( http://localhost:9999/settings?tab=interface ) 

**2.** Tick/Enable Custom CSS ✅  

**3.** Copy&Paste [CSS Code](#css-code) to the Custom CSS text area. 

**4.** Select one of the background images that you find at the top of the CSS code by removing the commentary ( _/*_ ) at the beginning of the line (_Flower_ is the standard background), or download the image as _"background.jpg"_, and place the image in `~/.stash` on macOS / Linux or `C:\Users\YourUsername\.stash` on Windows.







&nbsp;


Enjoy!


&nbsp;


# CSS Code



```
/*		Light Pulsar Theme - Fonzie 2021 v0.2		 */
/* ---------------------------------------------------- */
/* --------- Updated to Stash version 0.9.0-30 -------- */



/* ===================== General ===================== */

body {
	background-image:url("https://i.imgur.com/UwICmXP.jpg");	/* Flower		*/
/*	background-image:url("https://i.imgur.com/zqt3MFY.jpg");	/* Green Leaves 	*/
/*	background-image:url("https://i.imgur.com/vCotzwB.jpg");	/* White Desert		*/
/*	background-image:url("https://i.imgur.com/Lverfqy.jpg");	/* Tropic Beach		*/
/*	background-image:url("https://i.imgur.com/4jrpuyR.jpg");	/* White Blue Waves	*/
/*	background-image:url("https://i.imgur.com/KUtfQzs.jpg");	/* Bright Lights	*/
/*	background-image:url("./background.jpg");			/* Local BG		*/


	width: 100%;
	height: 100%;
	padding: 0 0 0;
	background-size: cover;
	background-repeat: no-repeat;
	background-color:#127aa5;
	background-attachment: fixed;
	background-position: center;
	color: #f9fbfd;
	color:#000;
}

h1, h2, h3{ 	color:#fff;}

:root {
	--HeaderFont: Helvetica, "Helvetica Neue", "The Sans", "Segoe UI";
	--std-txt-shadow: 2px 2px 1px #000;
	--light-txt-shadow: 1px 1px 3px #555;
	--white: #ffffff;
	--stars: url("https://i.imgur.com/YM1nCqo.png");
	--fourTwo: 0.35;
}


/* --- The Home button in the top left corner of each page. Remove the last 3 lines if you don't like the logo --- */
button.minimal.brand-link.d-none.d-md-inline-block.btn.btn-primary {
	text-transform: uppercase;
	font-weight: bold;
	margin-left:1px;
	background-image:url("./favicon.ico");
	padding-left:40px;
	background-repeat: no-repeat;
}

/* --- Makes the background of the Navigation Bar at the Top half-transparent --- */
.bg-dark {background: rgba(100, 200, 250, var(--fourTwo))!important;color:#000}
.form-group .bg-dark {background: rgba(130, 180, 205, 0.13)!important;}


/* --- The space between the Navigation Bar and the rest of the page --- */
.main { margin-top:18px }
.top-nav { padding: .13rem 1rem; }


/* --- Changes how the Bar at the top of the page behaves --- */
.fixed-bottom, .fixed-top { position: relative !important; top:0px !important} 


/* The pagination at the top and at the bottom of the Scenes/Performer/Images/... pages; 
transparent background, rounded corners, etc. */
.filter-container, .operation-container {
	background-color: rgba(100, 150, 160, .35);
	box-shadow: none;
	margin-top: 6px;
	border-radius: 5px;
	padding: 5px;
}


/* --- Changes the space between the button in the top right corner of the page --- */
.order-2 button { margin-left: 4px }

/* --- Space between the items in the Nav bar --- */
.nav-link > .minimal {  margin: 0px;}


/* Each item on the Scenes/Performers/Tags/... pages */
.card {
	padding: 20px; 
	margin: 4px 0.5% 14px;
	/* --- Adds a glowing shimmer effect --- */
	background-image: linear-gradient(130deg, rgba(60, 70, 85,0.21), rgba(150, 155, 160,0.30), rgba(35, 40, 45,0.20), rgba(160, 160, 165,0.21), rgba(70, 80, 85,0.27)); 
	background-color: rgba(106, 120, 125, .25); 
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .55);
	/* --- Increases the rounded borders of each item on the Scenes/Performers/... pages for 6px in 10px --- */
	border-radius: 10px;
}

/* --- Removes the glowing shimmer effect on the start page & the settings for readability purpose --- */
.mx-auto.card, .changelog-version.card {
	background-image: none !important; 
	background-color: rgba(16, 20, 25, .40) !important; 
}

/* --- Color that is used within .card secments --- */
.text-muted {	color: #eee !important;   	text-shadow: 1px 1px 2px #000;}


.bg-secondary {
	background: none;
	background-color: rgba(10, 25, 30, .3) !important;
}
 
.text-white {	color: #333 }
.border-secondary {	border-color: #2f3335 }
 
.btn-secondary.filter-item.col-1.d-none.d-sm-inline.form-control {
    background-color: rgba(0, 0, 0, .08);
}

/* --- Changes the color and the background of the buttons and elements in the toolbar (Search, Sort by, # of Items, etc.) --- */
.btn-secondary {
    color: #eef;
    background-color: rgba(45, 45, 45, .28);
    border-color: #3c3f45;
}
.btn-toolbar .btn-secondary {    color: #404049;     background-color: rgba(130, 130, 140, .28);}

 
a {	color: hsla(0, 10%, 10%, .85);}



/* --- Changes the color of the active page in the Navgation Bar --- */ 
.btn-primary:not(:disabled):not(.disabled).active,
.btn-primary:not(:disabled):not(.disabled):active,
.show>.btn-primary.dropdown-toggle {
	color: #fff;
	background-color: rgba(15, 150, 205, .6);
	border-color: #fff;
}

/* --- No border of the active element in the Navgation Bar --- */
.btn-primary.focus,
.btn-primary:focus,
.btn-primary:not(:disabled):not(.disabled).active:focus,
.btn-primary:not(:disabled):not(.disabled):active:focus,
.show>.btn-primary.dropdown-toggle:focus {box-shadow: none;}

.btn-primary:not(:disabled):not(.disabled).active,
.btn-primary:not(:disabled):not(.disabled):active,
.show>.btn-primary.dropdown-toggle {
	color: #fff;
	border-color: #eee;
    text-shadow: 1px 1px 2px #333;
    }

.container-fluid,.container-lg,.container-md,.container-sm,.container-xl {
	width: 100%;
	margin-right: 0px;
	margin-left: 0px;
}





/* ===================== Performer ========================= */


/* --- Changes the width of the Performer Card from 280px to a dynamic system and therefore the size of the image --- */
/* --- In Full screen HD 1920x1080 you now see 8 performers per row instead of 6 --- */
/*.performer-card-image, .performer-card, .card-image {  min-width: 160px; width: calc(108px + 10.625vw / 2); max-width: 230px }  */
/*.performer-card-image, .performer-card, .card-image {  min-width: 160px; width: calc(108px + 19vw / 3.6);width:212px; max-width: 230px } */
.performer-card-image, .performer-card, .card-image {  min-width: 160px; width: calc(100px + 11.2vw / 1.92);max-width: 230px } 


/* --- Changes the height of the Performer Card to keep the 2x3 picture ratio --- */
/*.performer-card-image, .justify-content-center .card-image { min-height:240px; height: calc((108px + 10.625vw / 2) * 1.5); max-height: 345px}  */
.performer-card-image, .justify-content-center .card-image { min-height:240px; height: calc((112px + 19vw / 3.6) * 1.5); max-height: 345px;} 
.performer-card-image, .justify-content-center .card-image { min-height:240px; height: calc((100px + 11.2vw / 1.92) * 1.5); max-height: 345px;} 

@media (max-width: 575px), (min-width: 1200px) {
.scene-performers .performer-card-image { height: auto; }
.scene-performers .performer-card { width: auto; }
}


/* --- Fixes an issue of the card when watching a scene --- */
.image-section { display: cover;}

/* --- The name of the Performer. Different font, less space to the left & to the top, Text-Shadow --- */
.text-truncate, .card.performer-card .TruncatedText {
	margin-left:-1.5%; 
	margin-top: -2px; 
	width: 120%; 
	font-family: var(--HeaderFont);
	font-size: 112%; 
	line-height:130%; 
	font-weight:bold; 
	text-shadow: var(--std-txt-shadow);
}

/* --- Makes the Performer Name smaller when the screen is too small --- */
@media (max-width: 1200px) { .card.performer-card .TruncatedText { font-size: 104%; } }



/* --- Moves the Flag icon from the right side of the card to the left and makes the Flag image a little bit bigger --- */
.performer-card .flag-icon {
    height: 2rem;
    left: 0.6rem;
    bottom: 0.10rem;
    width: 28px; 
}

/* --- Age and # of Scenes move from the left side to the right of the card --- */
.text-muted {text-align:right;margin-top:-2px;margin-bottom:1px}

/* --- "removes" the term 'old.' from "xx years old." when the resolution gets to small --- */ 
@media (max-width: 1520px) {
div.card.performer-card .text-muted {text-align:right;margin-top:-2px;margin-bottom:1px;margin-right:-33px}
}

/* --- To prevent overlapping in the performer card when watching a scene --- */
@media (max-width: 2000px) {
.tab-content div.card.performer-card .text-muted {margin-top:22px;margin-right:-3px}
.tab-content .performer-card.card .rating-1, 
.tab-content .performer-card.card .rating-2, 
.tab-content .performer-card.card .rating-3, 
.tab-content .performer-card.card .rating-4, 
.tab-content .performer-card.card .rating-5 {bottom: 53px !important;}
}


/* --- Text Shadow for the "Stars in x scenes" link --- */
div.card.performer-card div.text-muted a {text-shadow: 1px 2px 2px #333}

/* --- Makes the card section (Name, Age, Flag, # of scenes) more compact --- */
.card-section { margin-bottom: -8px !important; padding: .5rem 0.7rem 0 !important;}
.card-section span {margin-bottom:3px}
@media (max-width: 1500px) {	.card-section span {font-size:11px}	}

div.card-section hr {display:none}




/* --- Changes regarding the Favorite <3 --- */
.performer-card .favorite {
    color: #f33;
    -webkit-filter: drop-shadow(2px 2px 3px rgba(0, 0, 0, .95));
	filter: drop-shadow(2px 2px 3px rgba(0, 0, 0, .95));
	right: 3px;
	top: 5px;
}



/* --- Turns the Rating Banner in the top left corner into a Star Rating under the performer name --- */
.performer-card.card .rating-1, .performer-card.card .rating-2, .performer-card.card .rating-3, 
.performer-card.card .rating-4, .performer-card.card .rating-5
{
	background:none;
	background-size: 97px 18px;
	background-image:var(--stars);
	-webkit-transform:rotate(0deg);
	transform:rotate(0deg);
	padding:0;
	padding-bottom:1px;
	box-shadow: 0px 0px 0px rgba(0, 0, 0, .00);
	left:6px;
	width:97px;
	height:18px;
	text-align:left;
	position:absolute;
	top:auto;
	bottom: 34px;
	font-size:0.001rem;
}

/* --- Display only X amount of stars  -- */
div.performer-card.card .rating-banner.rating-1 {width:20px}
div.performer-card.card .rating-banner.rating-2 {width:39px}
div.performer-card.card .rating-banner.rating-3 {width:59px} 
div.performer-card.card .rating-banner.rating-4 {width:78px}  
div.performer-card.card .rating-banner.rating-5 {width:97px}  


.performer-card .btn {padding: .375rem .013rem}
.performer-card .fa-icon {margin: 0 2px}
.performer-card .card-popovers .fa-icon {margin-right: 3px}
.performer-card .svg-inline--fa.fa-w-18, .performer-card .svg-inline--fa.fa-w-16 {height: 0.88em}
.performer-card .favorite .svg-inline--fa.fa-w-16 {height:1.5rem}

div.performer-card div.card-popovers {
	margin-bottom: -3px;
	margin-left:1%;
	margin-top:-4px;
	margin-right: -3px;
	justify-content: flex-end;
	text-align:right;
}
.performer-card .card-popovers .btn-primary {
    margin: 0 0px 0 6px;
}



/* --- PerformerTagger Changes --- */

.PerformerTagger-performer {
	background-image: linear-gradient(130deg, rgba(50, 60, 75,0.25), rgba(150, 155, 160,0.32), rgba(35, 40, 45,0.26), rgba(160, 160, 165,0.27), rgba(50, 60, 65,0.37)); 
	background-color: rgba(16, 20, 25, .23); 
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .70);
	border-radius: 8px;
	margin: 1.1%;
  }
  
.tagger-container .input-group-text  {background:none;border:0;margin-right:5px;padding-left:0}
.PerformerTagger-details {	margin-left: 1.25rem; width:23.5rem;}

.tagger-container .btn-link{text-shadow: 1px 2px 3px #000;}
.tagger-container, .PerformerTagger {	max-width: 1850px;}

.PerformerTagger-header h2 {	
	font-family: Helvetica, "Helvetica Neue", "Segoe UI" !important; 
	font-size: 2rem; 
	line-height:130%; 
	font-weight:bold; 
	text-shadow: 2px 2px 1px #000 !important
}

.PerformerTagger-thumb {height: 145px;}
.PerformerTagger-performer-search button.col-6 {width:300px !important; flex-basis:100%;flex: 0 0 100%;
    max-width: 100%;}
.PerformerTagger-performer .performer-card {height:252px !important;}

.modal-backdrop 	 {	background-color: rgba(16, 20, 25, .25);}
.modal-backdrop.show {	opacity: 0.1;	}

.performer-create-modal {	max-width: 1300px; font-family: Helvetica, "Helvetica Neue", "Segoe UI" !important; }
.performer-create-modal .image-selection .performer-image { height: 95%; }
.performer-create-modal .image-selection {height: 485px;}

.performer-create-modal .no-gutters .TruncatedText {
	font-family: var(--HeaderFont);
	font-size: 115%;
	padding-top:2px;
	line-height:120%; 
	font-weight:bold; 
	text-shadow: var(--std-txt-shadow);
}
.performer-create-modal-field strong {margin-left: 6px}
.modal-footer {border-top: 0}






/* ========================= Performer Page ================================= */
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


/* --- The following 15 Selectors change the way the details box is displayed --- */
#performer-details-tabpane-details .text-input, #performer-details-tabpane-details .text-input:disabled, 
#performer-details-tabpane-details .text-input[readonly] {background-color: rgba(200,220,246,0.0);}
#performer-details-tabpane-details a { text-shadow: var(--light-txt-shadow)}

.text-input, input.form-control-plaintext { background-color:none;}
#performer-details .input-control, .text-input {box-shadow: none;}

div.react-select__control, #performer-details-tabpane-details {
	background-color: rgba(225,230,250,0.36); 
	border:1px solid #999; 
	max-width:1000px;
	box-shadow: 6px 6px 12px rgba(0, 10, 10, .22);
}
#performer-details-tabpane-details {border-radius: 10px}
#performer-details-tabpane-edit {max-width:1000px}

div.react-select__control .css-12jo7m5 {text-shadow: none; }

@media (min-width: 1200px) {
	#performer-details-tabpane-details td { padding: 9px; }
	table#performer-details tbody tr td:nth-child(1), td:first-child {padding-left: 22px; width: 185px;}
}
@media (max-width: 1200px) {
	table#performer-details tbody tr td:nth-child(1), td:first-child {padding-left: 11px; }
	#performer-page .performer-head {    margin-bottom: 1rem; }
	#performer-page { margin: 0 -6px 0 -15px; }
}
#performer-details-tabpane-details tr:nth-child(odd) {     background-color: rgba(16,22,26,0.1); }
table#performer-details {color:#FFF; text-shadow: 1px 1px 1px #000;}



/* --- Changes the way the name of the performer is displayed --- */
.performer-head h2 {font-family: var(--HeaderFont); font-weight:bold; text-shadow: 2px 2px 2px #111 }

/* --- Leave some space between the name and the Fav/Link/Twitter/IG icons --- */
#performer-page .performer-head .name-icons {margin-left: 22px}

/* --- Highlighter for active Details/Scenes/Images/Edit/Operations --- */
.nav-tabs .nav-item.show .nav-link, .nav-tabs .nav-link.active {
	background-color: rgba(135,160,165,0.5);
}

/* --- Changes the display of Performer Details Tab in the 0.9 version are arranged --- */
#performer-details-tabpane-details dl.row, dl.details-list dt, dl.details-list dd{ margin:0 0px;padding: 8px 10px 9px 14px}
#performer-details-tabpane-details dl.row:nth-child(odd),
#performer-details-tabpane-details dl.details-list dt:nth-of-type(odd),
#performer-details-tabpane-details dl.details-list dd:nth-of-type(odd) {	background-color: rgba(16,22,26,0.1);}
#performer-details-tabpane-details dt.col-xl-2,
#performer-details-tabpane-details dl.details-list dt {	text-shadow: var(--light-txt-shadow); font-weight: normal;}
#performer-details-tabpane-details ul.pl-0 {margin-bottom: 0rem;}
#performer-details-tabpane-details dl.details-list { grid-column-gap: 0}


/* --- Resets the fields in Performer Edit Tab in the 0.5 developmental version back to way it was in the 0.5 version --- */
#performer-edit {margin:0 0 0 10px}
#performer-edit .col-sm-auto, #performer-edit .col-sm-6, #performer-edit .col-md-auto, #performer-edit .col-lg-6, #performer-edit .col-sm-4, #performer-edit .col-sm-8 { width: 100%;max-width: 100%; flex: 0 0 100%; }
#performer-edit .col-sm-auto div, #performer-edit label.form-label { float:left; width:17%;}
#performer-edit .col-sm-auto div, #performer-edit label.form-label { font-weight:normal; color: #FFF; text-shadow: var(--std-txt-shadow); }

#performer-edit select.form-control, #performer-edit .input-group, #performer-edit .text-input.form-control { float:right; width:83%; }
#performer-edit .form-group, .col-12 button.mr-2 {margin-bottom: 0.35rem}
#performer-edit .mt-3 label.form-label { float:none; width:auto; }

#performer-edit select.form-control, #performer-edit .input-group, #performer-edit .text-input.form-control {width: 100%;}
#performer-edit textarea.text-input {min-height: 9ex;}

#performer-edit .form-group:nth-child(17) .text-input.form-control {width:85%;}

@media (max-width: 750px) {
#performer-edit .col-sm-auto div, #performer-edit label.form-label { float:left; width:22%;}
#performer-edit select.form-control, #performer-edit .input-group, #performer-edit .text-input.form-control { float:right; width:78%; }
}

@media (max-width: 500px) {
#performer-edit .col-sm-auto div, #performer-edit label.form-label { float:left; width:60%;}
#performer-edit li.mb-1, 
#performer-edit select.form-control, 
#performer-edit .input-group, #performer-edit .text-input.form-control { float:left; width:89%; }
}





/* ======================= Scenes ======================== */


/* --- Remove the comments if you don't want to see the Description Text of the scenes --- */
/* .card-section p {display:none} */


/* --- Remove the comments if you don't want to see the Resolution of the Video (480p, 540p, 720p, 1080p) --- */
/* .overlay-resolution {display:none} */



/* --- The name of the Scene. Different font, less space to the left and to the top, Text-Shadow --- */
h5.card-section-title, .scene-tabs .scene-header {	
	font-family: var(--HeaderFont);
	font-size: 1.25rem;
	font-weight:bold;
	line-height:132%;
	text-shadow: var(--std-txt-shadow);
}
.scene-tabs .scene-header { font-size: 24px; margin-bottom:25px }


#TruncatedText .tooltip-inner {width:365px; max-width:365px}
.tooltip-inner {	font-family: var(--HeaderFont);
	background-color: rgba(16, 20, 25, .99); 
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .55);
 font-weight:bold;font-size:14px;}

/* --- Removes the horizontal line that separates the date/description text from the Tags/Performer/etc. icons --- */
.scene-card.card hr, .scene-card.card>hr{	border-top: 0px solid rgba(0,0,0,.1);	}


/* --- Changes regarding the Scene Logo --- */
.scene-studio-overlay {
	opacity: .80;
	top: -3px;
	right: 2px;
}

/* --- The Resolution and the Time/Length of the video in the bottom right corner to make it easier to read --- */
.scene-specs-overlay {
	font-family: Arial, Verdana,"Segoe UI" !important;
	bottom:1px;
	color: #FFF;
	font-weight: bold;
	letter-spacing: 0.035rem;
	text-shadow: 2px 2px 1px #000, 4px 4px 5px #444, 7px 0px 5px #444, -3px 2px 5px #444, -5px 0px 5px #444, -1px -4px 5px #444, 3px -2px 6px #444;
}
.overlay-resolution {color:#eee;}

/* --- Changes the spaces between the items on the Scenes page --- */
.zoom-0 {margin: 4px 0.50% 10px; !important }


.scene-card-link {height:195px; overflow:hidden;}


/* --- Tightens the space between the Tags-, Performer-, O-Counter-, Gallery- and Movie-Icons --- */
.btn-primary { margin:0 -3px 0 -9px}

/* --- Moves the Tags-, Performer-, O-Counter-, Gallery- and Movie-Icon from below the description to the bottom right corner of the card --- */
.scene-popovers, .card-popovers { 
	min-width:0;
	margin-bottom: 3px;
	margin-top:-40px;
	justify-content: flex-end;
}

/* --- Adds an invisible dot after the description text, Also leaves ~80 pixels space to enforce a line break, 
so it leaves some space in the bottom right corner of the card for the icons in the Selector above --- */
.card-section p:after 
{
	font-size: 1px;
	color: rgba(0,0,0, .01);
	padding-right: 3.2vw; 
	margin-right: 2.8vw; 
	content: " ";
}




/* -- The whole section replaces the ratings banner with a star rating in the bottom left corner --- */ 
.scene-card.card .rating-1 {width:22px}
.scene-card.card .rating-2 {width:43px}
.scene-card.card .rating-3 {width:65px} 
.scene-card.card .rating-4 {width:86px}  
.scene-card.card .rating-5 {background:none; width:108px}
.rating-1, .rating-2, .rating-3, .rating-4, .scene-card.card .rating-5 {
	background:none;
	background-image:var(--stars);
	height:20px;
	background-size: 108px 20px;
} 

.scene-card.card .rating-banner {
	padding:0;
	left:5px;
	top:89%;
	background-position: left;
	font-size: .01rem;
	-webkit-transform: rotate(0deg);
	transform: rotate(0deg);
}


.zoom-0.card .scene-card.card .rating-banner {top: 81%}
.zoom-2.card .scene-card.card .rating-banner {top: 91%}
.zoom-3.card .scene-card.card .rating-banner {top: 92%}



/* --- Improves how the Preview Videos in the Wall View are displayed --- */
.wall-item-container {width: 100%; background-color: rgba(0, 0, 0, .10); overflow:hidden }
.wall-item-media { height:100%; background-color: rgba(0, 0, 0, .0);overflow:hidden }
.wall-item-anchor { width: 102%; overflow:hidden }
.wall-item-text {margin-bottom:0px; color: #111; text-shadow: 1px 1px 1px #fff }	


.scene-popovers .fa-icon {margin-right: 2px;}

/* --- Changes the Organized Button color when watching a video. Organized = Green, Not Organized = Red --- */
.organized-button.not-organized { color: rgba(207,10,20,.8); }
.organized-button.organized {	color: #06e62e;}


/* --- Changes the font in the File Info section --- */
div.scene-file-info .TruncatedText, div.scene-file-info .text-truncate {
	margin-left:-1.5%; 
	margin-top: -1px; 
	width: 120%; 
	font-family: var(--HeaderFont);
	font-size: 110%; 
	line-height:120%; 
	font-weight:bold; 
	text-shadow: var(--std-txt-shadow);
}


#scene-edit-details .pl-0 {
    padding-left: 10px!important;
}


/* Zoom 0 */
.zoom-0 { width:290px}
.zoom-0 .video-section {height:181px;}
.zoom-0 .scene-card-preview-image, .zoom-0 .scene-card-preview { height:195px; }
.zoom-0 .scene-card-preview, .zoom-0 .scene-card-preview-video, .zoom-0 .scene-card-video {
	width: 290px;
	min-height:181px;
	max-height: 200px;
}

/* Zoom 1 */
.zoom-1 { min-width: 300px; width: calc(234px + 24vw /3.84);max-width: 430px}
/* Improves the way the scene picture is displayed when the resolution isn't 16:9 (e.g. 4:3) --- */
.zoom-1 .video-section {height:calc((233px + 24vw / 3.84)/1.65);max-height: 258px}
.zoom-1 .scene-card-preview-image, .zoom-1 .scene-card-preview { height:100%; max-height: 260px}

/*
.zoom-1 .scene-card-preview-image, .zoom-1 .scene-card-preview { height:calc((237px + 24vw / 3.84)/1.65); max-height: 260px}
*/
.zoom-1 .scene-card-preview, .zoom-1 .scene-card-preview-video, .zoom-1 .scene-card-video {
	min-width: 300px; width: calc(228px + 17vw / 1.92);max-width: 470px;
	height:calc((234px + 26vw / 3.84)/1.65);
	max-height: 265px;
}

/* Zoom 2 */
.zoom-2 { min-width: 350px; width: calc(310px + 26vw / 3.84);max-width: 495px}
.zoom-2 .video-section {height:calc((310px + 26vw / 3.84) /1.65);max-height:295px}
.zoom-2 .scene-card-preview-image, .zoom-2 .scene-card-preview { height:calc((313px + 26vw / 3.84) /1.65); max-height:292px}

.zoom-2 .scene-card-preview, .zoom-2 .scene-card-preview-video, .zoom-2 .scene-card-video {
	min-width: 350px; width: calc(330px + 28vw / 3.84);max-width: 530px;
	height:calc((310px + 28vw / 3.84) /1.65);
	max-height: 298px;
}


/* Zoom 3 */
.zoom-3 { min-width: 400px; width: calc(530px + 18vw / 5.76);max-width: 590px}
.zoom-3 .video-section {height:375px;}
.zoom-3 .scene-card-preview-image, .zoom-3 .scene-card-preview { height:395px; }
.zoom-3 .scene-card-preview, .zoom-3 .scene-card-preview-video, .zoom-3 .scene-card-video {
	width: 600px;
	min-height:385px;
	max-height: 400px;
}


.zoom-0 .video-section, .zoom-1 .video-section, .zoom-2 .video-section, .zoom-3 .video-section 
{object-fit: cover !important;overflow:hidden;}

.zoom-0 .scene-card-preview, .zoom-0 .scene-card-preview-video, .zoom-0 .scene-card-video,
.zoom-1 .scene-card-preview, .zoom-1 .scene-card-preview-video, .zoom-1 .scene-card-video, 
.zoom-2 .scene-card-preview, .zoom-2 .scene-card-preview-video, .zoom-2 .scene-card-video,
.zoom-3 .scene-card-preview, .zoom-3 .scene-card-preview-video, .zoom-3 .scene-card-video {
	object-fit: cover !important;
	margin-top:-2%;
	margin-left:-6px;
	transform: scale(1.04);
}

/* --- Shrink the Player Height just a little bit to avoid the scroll bar --- */
#jwplayer-container {    height: calc(99.5vh - 4rem);}


div.tagger-container .btn-link { 	
	font-family: var(--HeaderFont);
	font-size: 110%; 
	color: #ddf; 
	text-shadow: var(--std-txt-shadow); 
}







/* ============== Studio ================= */


.studio-card {	padding: 0 4px 14px;}

.studio-details input.form-control-plaintext {	background-color: rgba(16,22,26,.0); }
.studio-details .react-select__control--is-disabled  {	background: none; border:0}

.studio-details .form-group, .studio-details td { padding: 8px; }
.studio-details table td:nth-child(1) {color:#FFF; text-shadow: 1px 1px 1px #000;}

.studio-card-image {	max-height: 175px; height:175px;}
.studio-card-image { min-width: 260px; width: calc(238px + 19vw / 3.8); max-width: 360px; margin: 0 6px;}
.studio-card .card-section {	margin-top: 22px;}

.no-gutters .TruncatedText, .tag-card .TruncatedText, div.card.studio-card .TruncatedText, .tagger-container .TruncatedText  {
	font-family: var(--HeaderFont);
	font-size: 125%; 
	line-height:125%; 
	font-weight:bold; 
	text-shadow: var(--std-txt-shadow);
}

.no-gutters .TruncatedText {font-size: 115%;}

/* --- The following 15 Selectors modify the info box on the left after clicking on a movie --- */
.studio-details .text-input, #performer-details-tabpane-details .text-input:disabled, 
.studio-details .text-input[readonly] {background-color: rgba(16,22,26,0.0);}

.text-input, input.form-control-plaintext { background-color:none;}
.studio-details .input-control, .text-input {box-shadow: none;}

.studio-details table { margin-top: 20px; background-color: rgba(15,20,30,0.20); border-radius: 10px; margin-bottom:20px;}
.studio-details .form-group, .studio-details .row {background-color: rgba(15,20,30,0.20); margin:0;}
.studio-details .no-gutters {background: none !important; }

.studio-details table div.react-select__control {background: none; border: 0px;margin:0}
.studio-details table .css-1hwfws3 { padding:0px; }

.studio-details .form-group, .movie-details td { padding: 8px; }
.studio-details .form-group td:nth-child(1), 
.studio-details table tbody tr td:nth-child(1), td:first-child {padding-left: 12px; width: 130px;}

.studio-details table tr:nth-child(odd) {     background-color: rgba(16,22,26,0.1); }
.studio-details .form-group, .studio-details table td:nth-child(1) {color:#FFF; text-shadow: 1px 1px 1px #000;}


.studio-card.card .rating-1, .studio-card.card .rating-2, .studio-card.card .rating-3, 
.studio-card.card .rating-4, .studio-card.card .rating-5
{
	background:none;
	height: 25px;
	background-size: 135px 25px;
	background-image:var(--stars);
	-webkit-transform:rotate(0deg);
	transform:rotate(0deg);
	padding:0;
	padding-bottom:1px;
	box-shadow: 0px 0px 0px rgba(0, 0, 0, .00);
	left:10px;
	text-align:left;
	position:absolute;
	top:auto;
	bottom: 20% !important;
	font-size:0.001rem;
}

.studio-card.card .rating-5{width:135px;} 
.studio-card.card .rating-4{width:109px;} 
.studio-card.card .rating-3{width:81px;} 
.studio-card.card .rating-2{width:55px;} 
.studio-card.card .rating-1{width:28px;} 

div.studio-card.card .card-popovers {	margin-top: -34px;}

.studio-details dl.details-list{ grid-column-gap: 0}
.studio-details dt, .studio-details dd {padding: 6px 0 8px 8px}



/* ============== TAGS =============== */

.tag-card.card hr, .tag-card.card>hr{ border-top: 0px solid rgba(0,0,0,.1); }

.tag-card { margin: 4px 0.5% 10px; padding:0px;}

.tag-card.zoom-0 {
	min-width: 230px; width: calc(200px + 18vw / 1.1); max-width: 350px;
	min-height:168px; height:calc(130px + 14vw / 1.1); max-height:250px;
}
.tag-card.zoom-0 .tag-card-image {	min-height: 100px; max-height: 210px; height: calc(95px + 15vw / 1.1);}

@media (min-width: 1200px){
.row.pl-xl-5, .row.px-xl-5 {
	padding-left: 0.2rem!important; 
	padding-right: 0.2rem!important;
}
}

.tag-card.zoom-1 {
	min-width: 260px; width: calc(238px + 25vw / 2.3); max-width: 460px;
	min-height:193px; height:calc(140px + 19vw / 2.3); max-height:285px;
}
.tag-card.zoom-1 .tag-card-image {	min-height: 120px; max-height: 240px; height: calc(100px + 19vw / 2.3);}

.tag-card.zoom-2 {
	min-width: 290px; width: calc(280px + 38vw / 2.45); max-width: 650px;
	min-height:170px; height:calc(180px + 28vw / 2.45); max-height:485px;
}
.tag-card.zoom-2 .tag-card-image {	min-height: 175px; max-height: 440px; height: calc(120px + 30vw / 2.45);}



#tags .card {padding:0 0 10px 0; }

.tag-card-header {height:190px;overflow:hidden;}

.zoom-0 .tag-card-image, .zoom-1 .tag-card-image, .zoom-2 .tag-card-image {
zoom: 101%;
object-fit: cover;
overflow:hidden;
width: 101%;
margin-top: -2px;
margin-left: -1%;
}

.tag-card .scene-popovers, .tag-card .card-popovers { 
	width:50%;
	margin-left:50%;
	justify-content: flex-end;
	float:right;
	margin-bottom: 4px;
	margin-top:-36px;
	padding-left:17px;
}

.zoom-0 .tab-pane .card-image { height:210px }


/* --- Moves the Tag name into the Tag Picture --- */
.tag-details .text-input[readonly] {background-color: rgba(0,0,0,.0);}
.tag-details .table td:first-child {display:none}
.tag-details .logo {margin-bottom: 12px;}

.tag-details .form-control-plaintext, .tag-details h2 {
	margin-top:-76px;
	margin-left:0%;
	font-weight: bold;
	font-family: Helvetica, "Helvetica Neue", "Segoe UI" !important;
	letter-spacing: 0.11rem;
	font-size:44px;
	text-shadow: 2px 2px 3px #111, 4px 4px 4px #282828, 6px 1px 4px #282828, -3px 3px 3px #444, -2px -2px 4px #282828;
	text-align:center; 
}
@media (max-width: 1300px) {.tag-details .form-control-plaintext {font-size:26px; 	margin-top:-50px;}}

.tag-details .logo { min-width:300px}





/* ==============  MOVIES ==============  */

/* --- Changes the width of the items so only the front cover is displayed. Also replaces the ratings banner with a star rating --- */

.movie-card .text-truncate, div.card.movie-card .TruncatedText {
	font-size: 17px !important;
	font-family: var(--HeaderFont);
	text-shadow: var(--std-txt-shadow);
	font-weight: bold;
	max-width:210px;
	white-space: nowrap;
	overflow: hidden; 
	text-overflow: ellipsis;

}

.movie-card-header {height:320px}

.movie-card-header .rating-banner {
	font-size: .002rem;
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(0deg);
	padding: 0;
	left: 3px;
	top: 77% !important;
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
	background-image:var(--stars);
	height: 25px;
	background-size: 135px 25px;
}

.movie-card-image {
	height:345px;
	max-height: 345px;
     width: 240px;
}




/* --- The following 15 Selectors modify the info box on the left after clicking on a movie --- */
.movie-details .text-input, #performer-details-tabpane-details .text-input:disabled, 
.movie-details .text-input[readonly] {background-color: rgba(16,22,26,0.0);}

.text-input, input.form-control-plaintext { background-color:none;}
.movie-details .input-control, .text-input {box-shadow: none;}

.movie-details table { margin-top: 20px; background-color: rgba(15,20,30,0.20); border-radius: 10px 10px 0px 0px; margin-bottom:0;}
.movie-details .form-group {background-color: rgba(15,20,30,0.20); margin:0;}

.movie-details table div.react-select__control {background: none; border: 0px;margin:0}
.movie-details table .css-1hwfws3 { padding:0px; }

.movie-details .form-group, .movie-details td { padding: 8px; }
.movie-details .form-group td:nth-child(1), 
.movie-details table tbody tr td:nth-child(1), td:first-child {padding-left: 12px; width: 120px;}

.movie-details table tr:nth-child(odd) {     background-color: rgba(16,22,26,0.1); }
.movie-details .form-group, .movie-details table td:nth-child(1) {color:#FFF; text-shadow: 1px 1px 1px #000;}

/*
.movie-details div.form-group:nth-of-type(3) { border-radius: 0px 0px 20px 10px; background-color: rgba(16,22,26,0.3); margin-bottom:15px }
.movie-details div.form-group {display: flex; flex-wrap: wrap; overflow: hidden; text-overflow:ellipsis;}
.movie-details div.form-group label.form-label {width: 120px; padding:0 20px 0 5px}
.movie-details div.form-group div {width:65%; text-align:left; 	}
*/

/* --- 0.60 dev adjustments --- */
.studio-details .studio-details, .movie-details .movie-details {background-color: rgba(15,20,30,0.20); border-radius: 10px; margin-bottom:15px; }
.movie-details .movie-details dt.col-3 {padding:4px 0 4px 16px; width: 120px;}
.movie-details .movie-details dd.col-9 {padding:4px 16px 4px 3px;}
.studio-details dl.details-list dt:nth-of-type(odd),
.studio-details dl.details-list dd:nth-of-type(odd),
.movie-details dl.details-list dt:nth-of-type(odd),
.movie-details dl.details-list dd:nth-of-type(odd),
.movie-details dl.row:nth-child(odd) { background-color: rgba(16,22,26,0.1); margin-right:0px; padding-left:7px;margin-bottom:5px}
.movie-details dl.details-list dt, .movie-details dl.details-list dd {padding-left: 7px;}
.movie-details dl.details-list { grid-column-gap: 0}
.studio-details h2, .movie-details .movie-details h2 {	font-family: var(--HeaderFont);font-weight:bold;text-shadow: var(--std-txt-shadow);padding:7px 0 5px 12px;}

.movie-details .movie-images {margin:0 5px 20px 5px;}
.movie-details .movie-images img {border-radius: 14px; max-height:580px;}
.movie-details .movie-image-container{
	margin:0.3rem;
	margin-right:0.8rem;
	background-color: rgba(0, 0, 0, .48);
	box-shadow: 6px 6px 11px rgba(0, 10, 10, .62);
}

form#movie-edit { margin-bottom:15px}






/* ==============  IMAGES ==============  */

div.image-card .rating-banner {
	font-size: .002rem;
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(0deg);
	padding: 0;
	left: 3px;
	top: 72% !important;
	height: 25px;
	background-size: 135px 25px;
	background-position: left;
}

div.image-card .rating-1 {width:28px}
div.image-card .rating-2 {width:55px}
div.image-card .rating-3 {width:83px} 
div.image-card .rating-4 {width:110px}  
div.image-card .rating-5 {width:138px}

div.image-card .rating-5 {
	background:none;
	background-image:var(--stars);
	height: 25px;
	background-size: 135px 25px;
}

div.image-card .scene-popovers, div.image-card .card-popovers {
	margin-top: -2px;
	justify-content: flex-end;
}
div.image-card hr, .scene-card.card>hr{
	border-top: 0px solid rgba(0,0,0,.1); 
}







/* ==============  GALLERIES ==============  */

div.gallery-card hr, .scene-card.card>hr{
	border-top: 0px solid rgba(0,0,0,.1); 
}

div.gallery-card .rating-banner {
	font-size: .002rem;
	padding: 8px 41px 6px;
	line-height: 1.1rem;
	transform: rotate(0deg);
	padding: 0;
	left: 3px;
	top: 70% !important;
	height: 25px;
	background-size: 135px 25px;
	background-position: left;
}

div.gallery-card .rating-1 {width:28px}
div.gallery-card .rating-2 {width:55px}
div.gallery-card .rating-3 {width:83px} 
div.gallery-card .rating-4 {width:110px}  
div.gallery-card .rating-5 {width:138px}

div.gallery-card .rating-5 {
	background:none;
	background-image:var(--stars);
	height: 25px;
	background-size: 135px 25px;
}

div.gallery-card .scene-popovers, div.gallery-card .card-popovers {
	margin-bottom: -8px;
	margin-top: -24px; 
	justify-content: flex-end;
}








/* ==============  MISC ==============  */

.svg-inline--fa.fa-w-18 {width: 1.4em;}

/* --- Makes the Zoom Slider on the Scenes, Images, Galleries and Tags pages longer and therefore easier to use --- */
input[type=range].zoom-slider{ max-width:140px;width:140px; }

/* --- Changes the zoom slider color --- */
input[type=range]::-webkit-slider-runnable-track {background-color: #88afcc !important;}


.tag-details .logo {
    background-color: rgba(0, 0, 0, .48);
    box-shadow: 3px 3px 5px rgba(0, 0, 0, .42);
    border-radius: 9px !important;
}

.search-item {
    background-color: none;
    background-color: rgba(16,22,26,0.27);
}

.btn-secondary.disabled, .btn-secondary:disabled {
    background-color: none;
    background-color: rgba(16,22,26,0.67);
}

/* --- Edit & Delete buttons when clicking on a studio, tag or movie --- */
.details-edit {margin-left:3%}

/* --- Adds a text shadow to the statistics on the startpage --- */
.stats .title {
	color:#fff;
	text-shadow: 2px 2px 4px #282828;
}


.popover {
	padding:2px;
	background-color: rgba(5,30,35,0.85); 
	box-shadow: 3px 3px 6px rgba(20, 20, 20, .8);
}
.hover-popover-content {
	background-image: linear-gradient(160deg, rgba(230,255,240,0.80), rgba(120,130,155, 0.45), rgba(180,190,225, 0.45), rgba(120,130,165, 0.55), rgba(255,235,235,0.70)); 
	background-color: rgba(205,210,225,0.31) !important; 
}

.tag-item {
	font: normal 13px "Lucida Grande", sans-serif, Arial, Verdana;
	background-image: linear-gradient(210deg, rgba(30,95,140,0.36), rgba(10,60,95, 0.45), rgba(20,65,105, 0.83), rgba(5,90,140,0.35)); 
	background-color: rgba(60,120,230,0.8); 
	color: #fff;
	letter-spacing: 0.07rem;
	line-height: 18px;
	margin: 3px 3px;
	padding: 6px 8px;
}

/* --- Adjust the lengths of the Performer, Movies and Tags fields while editing a scene while the scene plays --- */
#scene-edit-details .col-sm-9 {
    flex: 0 0 100%;
    max-width: 100%;
}

/* --- Cuts the name of Performers, Movies and Tags short if they go longer than the length of the field --- */
div.react-select__control .react-select__multi-value {
  max-width: 285px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}




/* --- several Performer and Scene Scaping changes --- */
.modal-content, .modal-lg, .modal-xl  {
	max-width: 1400px; 
	width:100%;
} 

.modal-header, .modal-body, .modal-footer {	background: rgba(10,120,170,0.94);}
.performer-create-modal {max-width:1300px;}

.modal-body .col-form-label, .modal-body .col-6, .modal-footer, .modal-header .col-form-label {text-shadow: var(--std-txt-shadow);}

.modal-body .col-6 strong {font-weight: normal; font-size:14px}
.modal-body .no-gutters {margin-bottom: 8px}

.modal-body .dialog-container .col-lg-3 {
	flex: 0 0 12%;
	max-width: 12%;
	text-shadow: var(--std-txt-shadow);
}

.modal-body .dialog-container .offset-lg-3{margin-left:12%;} 
.modal-body .dialog-container .col-lg-9{flex:0 0 88%; max-width:88%;} 


.input-control, .input-control:disabled, .input-control:focus, .modal-body div.react-select__control, .modal-body .form-control {
	background: rgba(15,15,20,0.36);
}


.scraper-table tr:nth-child(2n) {    background: rgba(15,15,20,0.18);}

.nav-pills .nav-link.active, .nav-pills .show>.nav-link { 	background: rgba(15,15,20,0.50);}


.btn-secondary:not(:disabled):not(.disabled).active, 
.btn-secondary:not(:disabled):not(.disabled):active, 
.show>.btn-secondary.dropdown-toggle { 	background: rgba(15,15,20,0.50);}


/* --- Background when searching for a scene in Tagger view --- */
.search-result { 	background: rgba(0,0,0,0.22);}
.selected-result { 	background: rgba(25,120,25,0.28);}
.search-result:hover { background: rgba(12,62,75,0.35);}


.markdown table tr:nth-child(2n) {background: rgba(25,20,25,0.20);}
.markdown code, .markdown blockquote, .markdown pre {background: rgba(25,20,25,0.30);}


/* --- Changes the size of the Custom CSS field in the settings --- */
#configuration-tabs-tabpane-interface textarea.text-input { min-width:60ex; max-width:55vw !important; min-height:50ex;}


div.dropdown-menu,div.react-select__menu{background-color:rgba(35,37,44,0.55);color:#f5f8fa}

div.dropdown-menu .dropdown-item, div.dropdown-menu .react-select__option, div.react-select__menu .dropdown-item, div.react-select__menu .react-select__option
{color:#f5f8fa;background-color:rgba(35,37,44,0.55);}

div.dropdown-menu .dropdown-item:focus,div.dropdown-menu .dropdown-item:hover,div.dropdown-menu .react-select__option--is-focused,div.react-select__menu .dropdown-item:focus,div.react-select__menu .dropdown-item:hover,div.react-select__menu .react-select__option--is-focused{background-color:rgba(24,130,195,0.85)}


.toast-container {
    left: 74%;
    top: 1rem;
}

/* --- Settings / About adjustments --- */
#configuration-tabs-tabpane-about .table {width:100%}
#configuration-tabs-tabpane-about .table td {padding-top:18px}


#queue-viewer .current {
    background-color: rgba(15,20,30,0.30);
}

/* Folder when doing selective scan or configuration */
.input-group .form-control {color: #d9f0f7; }


div.modal-body b, .form-label h6 {text-shadow: var(--std-txt-shadow);}


.modal-body .btn-primary:not(:disabled):not(.disabled).active, .modal-body .btn-primary:not(:disabled):not(.disabled):active {
color: #fff; 
     background-color: #008558; 
     border-color: #0d5683;
}

.modal-body .btn-primary {
    color: #fff;
    background-color: #666;
    border-color: #666;
}

.input-group-prepend div.dropdown-menu
{
	background: rgba(50,90,105,0.94);
	padding:15px;
	box-shadow: 2px 2px 6px rgba(0, 0, 0, .70);
}

.saved-filter-list .dropdown-item-container .dropdown-item {margin-top:3px;}
.set-as-default-button {margin-top: 8px;}



/* --- Specific Light Modifications --- */

a.minimal, button.minimal {
	color: #fff;
    	text-shadow: 1px 1px 2px #000;
}

.top-nav a.minimal, .top-nav button.minimal {
	color: #333;
    	text-shadow: 1px 1px 2px #ddd;
}

.top-nav { box-shadow: 2px 2px 6px rgba(120, 150, 160, .55)}


.pagination .btn:last-child {border-right: 1px solid #202b33;}
.pagination .btn:first-child {border-left: 1px solid #202b33;}

.nav-tabs .nav-link { color: #000038;}


.scene-card .card-section {color:#fff;text-shadow: 0px 0px 1px #111;}
.changelog-version, .tab-content {color: #fff}
.tab-content .bg-dark {color:#fff} 

#performer-details-tabpane-details {color: #000}
.scraper-table a {color:#dde}
.image-tabs, .gallery-tabs, .scene-tabs  {
	background-image: linear-gradient(130deg, rgba(60, 70, 85,0.21), rgba(150, 155, 160,0.30), rgba(35, 40, 45,0.22), rgba(160, 160, 165,0.21), rgba(50, 60, 65,0.30)); 
	background-color: rgba(106, 120, 125, .29); 
}

.table-striped.table-bordered, .table-striped.table-bordered a {color:#000}

.nav-tabs .nav-link.active { color: #2866d0;}

.PerformerScrapeModal-list .btn-link { color: #a9d0ff;}

.tab-content .scene-file-info a {color: #cde}

.grid-card .card-check { top:.9rem;width: 1.5rem;}
.LoadingIndicator .spinner-border, .LoadingIndicator-message { color:#37e}


```
