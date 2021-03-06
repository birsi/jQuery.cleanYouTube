![Screenshot](https://raw.github.com/tom2strobl/jQuery.cleanYouTube/master/screenshot.png)

# jquery.cleanYouTube

A jQuery plugin for usage of the chromeless YouTube API with a very clean skin. It also clears the red Youtube-Play-Buttons at the start and the end of the video.

## WARNING

**This Plugin in still under HEAVY development and currently only works in Chrome perfectly. The CSS is messy, you can't define sizes and it may look weird in other browsers than the latest Chrome build.**

## Installation

In your head, include the provided CSS-File (I've stripped the whole CSS to a file so it's easy to customize). The font for the controls is already base-encoded within that CSS file.

    <link rel="stylesheet" href="/path/to/cleanYouTube.css">

Include the script *after* you included the jQuery library (unless you are packaging scripts somehow else):

    <script src="/path/to/jQuery.cleanYouTube.min.js"></script>
    
Then call the plugin on the element you want to insert the video to and at least specify the *videoid*:
    
    <script>
	$('.video').cleanYouTube({
		'videoid' : 'pg4mnnZStU8',
		'autoplay' : false,
    	'loop' : false
	});
	</script>

**Do not include the script directly from GitHub (http://raw.github.com/...).** The file is being served as text/plain and as such being blocked
in Internet Explorer on Windows 7 for instance (because of the wrong MIME type). Bottom line: GitHub is not a CDN.

## Options

### videoid

    videoid: 'c1PbjssaNAg'

Define the videoid from a YouTube URL. eg: http://www.youtube.com/watch?v= **c1PbjssaNAg**

### autoplay

    autoplay: false

If true, plays as soon as the video is loaded. Can be set to true or false.

### loop

    loop: false

If true, starts the video again when it reaches the end. Can be set to true or false.

## Testing

The code is currently only tested on the latest Chrome Build.

## Development

Pull requests are very welcome! Everyone is invited to improve the plugin, it's certainly not js-guru-like.

### Known issues

Altough it completely works in Chrome it drops two Errors from the YouTube API itself:

	Unable to post message to http://www.youtube.com. Recipient has origin http://...
	GET http://www.youtube.com/get_video... 404 (Not Found)

## Authors

[Thomas Strobl](https://github.com/tom2strobl)
