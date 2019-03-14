# Testing Dash Streaming

Reference: https://hub.docker.com/r/majamee/alpine-dash-hls/

Go to: https://www.clipconverter.cc/

Download MKV 4K video of: https://www.youtube.com/watch?v=xcJtL7QggTI

Rename the file to: **sony4kvideo.mkv**

We clone this project, and then we put the "mkv" video file under the "video" directory.

On the root directory of this project we run:

	docker run -v /full/path/to/the/video/:/video majamee/alpine-dash-hls sony4kvideo.mkv

This would create an "output" directory under the "video" directory.

Then we run:

	docker-compose up

Our generated DASH video is in our "server" here: http://localhost:8080/playlist.mpd

To test it, we need to access to this URL: http://localhost:3000/dash.js/samples/dash-if-reference-player/ and put there the URL of the above video. We can also use the default video provided by dash.js


Reference: 
- https://github.com/Dash-Industry-Forum/dash.js/
- https://hub.docker.com/r/majamee/alpine-dash-hls
- https://isrv.pw/html5-live-streaming-with-mpeg-dash
- https://github.com/arut/nginx-rtmp-module

Useful commands to clean everything:

	docker rm $(docker ps -a -q)
	docker image rm $(docker image ls -a -q)



