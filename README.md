# docker_ezstream
ezstream Docker Container

Ubuntu 16.04 based ezstream media streamer. Includes lame and madplay so you can decode/rencode files.

Volumes included: "/ezstream" and "/music"

The ezstream binary is run with xml config file "/ezstream/ezstream.xml". This file does not exist in the image as it is very site specific. It is recommended to mount an external host volume onto "/ezstream" at runtime. You should also map your music repository into the container.

Example Invocation:


# docker run -v /storage/Docker/ezstream:/ezstream:ro -v /storage/Media/Music:/music:ro --name ezstream -d dashultz/ezstream
