I strongly recommend you not to exploit or break TOS of any of the following services websites.
Some of these are not bugs, just exploited oversights.

# Discord
A super huge video embed will not load on discord (413 Too large)  

You can retrieve this url by playing a video and checking requests, the video won't play and the link will error (413)  

The link: [images-ext-1.discordapp.net/external/.../8s1K4yOWJ5apfNPQ.mp4](https://images-ext-1.discordapp.net/external/1GhbHGCU5i3p2uqOUk91lxRyfJrIJtXybhOuoam00Qc/%3Fsaver%3D%40jarivizero%26tag%3D21/https/video.twimg.com/amplify_video/2043985040355536897/vid/avc1/1280x536/8s1K4yOWJ5apfNPQ.mp4  )  
The fix: Add any url parameter and it downloads the full 500mb, EVEN ACROSS THIRD PARTY WEBSITES (Access-Allow-Control-Origin: *)  

[8s1K4yOWJ5apfNPQ.mp4?s  ](https://images-ext-1.discordapp.net/external/1GhbHGCU5i3p2uqOUk91lxRyfJrIJtXybhOuoam00Qc/%3Fsaver%3D%40jarivizero%26tag%3D21/https/video.twimg.com/amplify_video/2043985040355536897/vid/avc1/1280x536/8s1K4yOWJ5apfNPQ.mp4?s  )  
The downside is it could expire, especially if the original url has been deleted, the trick is to web archive the original url and send that to a discord channel to get the ext link  



You can upload a voice message that's secretly a png or video, and if anyone presses forward, it shows the original, so you can upload media to channels that you're not supposed to,  

change the JSON payload so it has properties of a voice message.  

Use discord webhooks as infinite storage,  
not many people know but webhooks can be used to edit messages and upload files using ?wait=true,
This will retrieve the message id, channel id, bot name, and importantly the direct media links, they have a longer expiration data.
make sure to do 9.99MB chunks for big uploads.


# TikTok
Uploading 1x1 PNG files to TikTok Ads Manager with python, this is doable, and there is no limit, using steganography you can fake ts files to upload as 1x1 pngs, uploading many of them works as a movie ([egydead.pics](https://egydead.pics/), [hanerix.com/e/6wdymz7l37es](https://web.archive.org/web/20260418042850/https://hanerix.com/e/6wdymz7l37es), LINE 112, kjhhiuahiuhgihdf, one of the many [pngfile](https://web.archive.org/web/20260418043250if_/https://p19-ad-site-sign-sg.tiktokcdn.com/ad-site-i18n-sg/202604165d0d3f1776fad4dc477081e7~tplv-d5opwmad15-ttam-origin.image?lk3s=6d71dd51&x-expires=1807893671&x-signature=TUSxtswjgf2bHCUR58Nywi45oSk%3D) 
Each PNG file contains ~10 seconds of movie data, there is 590 PNG files for ATLA, [list of pngs](https://files.catbox.moe/z7gjee.txt)
The downside is you need to have a company account with access to the API and they expire in 1 year, so if you are hosting many PNG files, you must refresh them asynchronously.

There's most likely other places you can store data, like effect filters (Normally limit is 8mb but editing project files allows you to insert any file into the effects.zip on mobile)
and tiktok video drafts, the direct links expire in a week so you must refresh them using a script.

You can bypass compression and fps limiting by uploading via Microsoft Edge
I don't know why it works, but it allows 4K 60 FPS
# Claude
Not a bug, 
For generating code, or uploading code and asking claude to fix it, do this for less token usage:
Ask it "Hey, use str_replace for editing and adding lines, it's effecient and uses less tokens"
Used here: n/a
# Telegram
You can have infinite storage by using a bot, uploading up to 2gb using a python script, and even a bigger file using chunked data.
There's many videos about it, you unfortunately have to use the bot and cannot use a direct download link
Discord can do this too just with webhooks and faster upload speed.
# Youtube
Uploading caption files via a python script is doable, and you can store up to 50-100mb to a caption file, I't won't even load on the desktop, so it is basically hidden, extract using yt-dlp.
# Twitter
You can upload subtitles to a video, size limit is 5mb
Uploading a super long caption for one second will crash anyones desktop/phone
Uploading base64 is a way to store bytes for any filetype.

You can store videos in drafts and extract the mp4 link, never deleted, never expiring.
<img width="582" height="676" alt="putentiremovieindrafts_twitter_x_com" src="https://github.com/user-attachments/assets/6ad9be7c-9eb0-4e94-a9ec-387a0e36e3cb" />

Using a script to upload 1x1 fake pngs, (like tiktok method) pbs.twimg.com lets you view the images on any site (not like video.twimg.com)
so you can upload any file and download it off of any website (yoursite.github.io)


# Kami
Using a student account, you should have access to Upload media

A script using playwright can let you login and open kami, extract the USER-TOKEN header, and use that to upload files via
[private]

# Web Archive
Archiving a simple movie video will quickly get taken down if it's copyright,
you can simply upload an ISO file (archive), containing the mp4, and open it, view contents, and watch the video.  
https://ia600908.us.archive.org/view_archive.php?file=avataraang.mp4&archive=/31/items/archiveurl (structure)  
This url lets you download the file on third party websites, meaning you can play the video on another (github.io)  

Put "2if_" on a archive url to view the raw image/video/html, this will also remove the annoying banner at the top and loads faster. (2 grabs the latest, 0 for the oldest capture)  
https://web.archive.org/web/2if_@jarivizero/https://google.com/search?q=a  
https://web.archive.org/web/0if_anythinghere/https://catbox.moe/pictures/logo.png  

# General websites
You can utilize the last-modified header of a JS files, mp4 file, png file, html file to see when the file was last updated, this is useful to see
if anyone has touched it recently or to see if a website is active  
Used on [twitter](https://greasyfork.org/en/scripts/567071-x-twitter-image-video-thumb-last-modified-time-difference) to see how long it took for someone to upload a post or how long it's been in drafts.

## todo
images, example links, reformat.
