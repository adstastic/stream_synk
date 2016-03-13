# SyncStream

Ever wanted to watch a YouTube video with someone across the world as if they were right next to you? We can't do teleportation, but we can sync a video across many browser sessions. What's more, we even threw in a chat system so you can talk, etc! 

The current version was built at the Facebook London Hackathon over a day or so (+ a sleepless night, by the end my code became pretty sloppy.) I hope to make this proper over time! 

More details to come.

## Installation 

* npm install
* node app.js

## Usage

* All URL fields accept a full YouTube URL - things won't work so well if you mess with it.
* If the middle of the screen (the video section) is blank, refresh the page.
* Sessions are not (yet) private - anyone who happens to choose the same video as you becomes a guest in your session!
* The YouTube API doesn't really let you capture *seek* events so we had to work around it - to stop an infinite loop of craziness and video play-pause looping back and forth, there's a post-event timeout during which any action on the video player will not propogate to the other clients. Wait at least 1000 ms before doing anything.
