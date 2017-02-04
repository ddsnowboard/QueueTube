QueueTube
=================

A webapp that allows you to queue youtube videos for easy music listening. It will work on PC, but the main appeal is that it works on your phone, allowing you to use YouTube as a free but otherwise nearly drop-in replacement for Spotify. The killer features are being able to keep listening to videos while you are searching (which works on the YouTube app but not on the website) and being able to queue videos to watch later (which used to exist but no longer).

The theoretical market for this is me, a college student who doesn't pay for Spotify and wants to listen to music through a Bluetooth speaker or headphones from their phone without having to pick a new song every 5 minutes.


##Functional spec

###Search Screen

When you first load the site, you are greeted with a search box. In a perfect world, there is a blinking cursor sitting in it, awaiting your search, but that sounds like it would be hard to implement. If it just has the word "Search..." in grey text, that would be fine. Ideally, it would be in the center of the window to start, and then when you click it would move to the top of the screen. NB: This may not work too well on mobile. If there is a choice between reliable functionality and working very nicely in ideal cases, the prior is the right decision.

Once the user clicks on the search box and types a search, the search results come up on the screen, with the search box staying static at the top of the screen even as the user scrolls through the search results. Each video has a thumbnail on the left side, the title of the video in big letters, and then below that, the uploader of the video. On the right side of the screen, there will be a green plus-sign. From a design perspective, this may not be perfect, but it will improve ease-of-use, which is more important to me. If the user clicks on the title or the thumbnail, the video will start playing immediately, opening the Player Screen. If the user clicks on the green plus-sign, the video will be added to the queue. If there is nothing in the queue, the video will start playing in the background, not bringing up the Player Screen, but putting it in the lower-right corner, similar to the YouTube Android app. This will also cause a button to appear on the top right corner, moving the search box over, that shows the Queue Screen. If the user clicks on the mini-player, the Player Screen appears.

The user can scroll through videos, and when they scroll to the bottom of the page, the next page will be automatically loaded and appended to the end of the screen, allowing in effect infinite scrolling.

###Player Screen

The Player Screen looks almost exactly like the equivalent screen on the YouTube Android app. The video is playing on the top half (covering the search box), and there is a button on the top left corner (if possible, below the video otherwise) that looks like a down arrow and minimizes the video, exposing the search page below. Below the video is the name of the video, the poster of the video, and below that are some related videos, provided by YouTube.

###Queue Screen

This just shows the queued videos in order. It looks similar to the search box, except instead of a green plus sign, there is a red X, and to the left of the thumbnail, there is a "handle" that allows the user to drag videos around the queue. The currently playing video has some sort of highlight on it to indicate that it is playing. If the currently playing video is dragged, the queue works normally, such that the video after the new position of the currently playing video plays.
