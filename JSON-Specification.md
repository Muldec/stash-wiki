# Introduction

The Metadata given to Stash can be exported into the JSON format. This structure can be modified, or replicated by other means. The resulting data can then be imported again, giving the possibility for automatic scraping of all kinds. The format of this Metadata bulk is a folder Structure, containing the folders 
  
downloads, galleries, performers, scenes, studios  
  
as well as a file called  
  
mappings.json
  
The mappings file contains a reference to all files within the folders, by including their checksum. All files in the aforementioned folders are named by their checksum (like 967ddf2e028f10fc8d36901833c25732.json), which (at least in the case of galleries and scenes) is generated from the file that this metadata relates to. The algorithm for the checksum is MD5. 

# Content of the jsons

In the following, the values of the according jsons will be shown. The meaning from most of them should be obvious due to the previous explanation or from the possible values stash offers when editing, otherwise a short comment will be added.  
The json values are given as strings, if not stated otherwise. Every new line will stand for a new value in the json. If the value is a list of objects, the values of that object will be shown indented.  
Talking about the performer.json and the later ones is referring to a singular json contained within the directory the name is referring to, named by the checksum which is given from the mappings.json.  
If a value is empty in any but the mappings.json file, it can be left out of the file entirely. In the mappings.json however, all values must be present, if there are no objects of a type (for example, no performers), the value is simply null.  
Many files have an created_at and updated_at, both are kept in the following format:  
YYYY-MM-DDThh:mm:ssTZD  
example:  
"created_at": "2019-05-03T21:36:58+01:00"

## mappings.json

performers  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;name  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;checksum  
studios  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;name  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;checksum  
galleries  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;path   
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;checksum  
scenes  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;path   
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;checksum  

## performer.json

name  
url  
twitter  
instagram  
birthdate  
ethnicity  
country  
eye_color  
height  
measurements  
fake_tits  
career_length  
tattoos  
piercings  
image (base64 encoding of the image file)  
created_at  
updated_at  

## studio.json

name  
url  
image (base64 encoding of the image file)  
created_at  
updated_at  

## scene.json
title  
studio  
url  
date  
rating (integer)  
details  
performers (list of strings, performers name)  
tags (list of strings)  
markers     
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;title  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;seconds  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;primary_tag  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tags (list of strings)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;created_at  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;updated_at  
file (not a list, but a single object)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;size (in bytes)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;duration (in seconds)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;video_codec (example value: h264)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;audio_codec (example value: aac)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;width (integer, in pixel)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;height (integer, in pixel)  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;framerate  
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;bitrate (integer, in Bit)  
created_at  
updated_at  

## gallery.json  

title  
performers (list of strings, performers name)  


