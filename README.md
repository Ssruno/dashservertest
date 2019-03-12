# Testing Dash Streaming

Reference: https://hub.docker.com/r/majamee/alpine-dash-hls/

Go to: https://www.clipconverter.cc/

Download MKV 4K video of: https://www.youtube.com/watch?v=xcJtL7QggTI

Rename the file to: **sony4kvideo.mkv**

Put the "mkv" video file under the "video" directory.

Run:

	docker run -v /full/path/to/the/video/:/video majamee/alpine-dash-hls sony4kvideo.mkv


This would create an "output" directory under the "video" directory.


Then we run:

	docker run --name some-nginx -p 8080:80 -v /video/output/sony4kvideo:/usr/share/nginx/html:ro -d nginx

Then access: http://localhost:8080/

TODO: Add this player for debug: https://github.com/Dash-Industry-Forum/dash.js/