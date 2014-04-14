TV5Video.ca plugin for Showtime (Unofficial)
============================

TV5Video is TV5 Canada's TV on demand (replay) website.

Showtime (https://www.lonelycoder.com/showtime ) is a great media center for Linux, Mac OS X, Raspberry Pi and the PS3.

TV5Video.ca Showtime plugin allows the integration of TV5 Canada videos into Showtime.

Most of the content is in french, seems to be accessible from outside Canada, and is encoded in 640x360 only :-(

Git: https://github.com/anthonydahanne/showtime-plugin-tv5video.ca

## Release notes

1.0 - First release

-  allows you to browse shows (Emissions), then select one and choose your episode

## Screenshots

![Screenshot](https://raw.github.com/anthonydahanne/showtime-plugin-tv5video.ca/master/screenshots/tv5video.ca-homescreen.png "home")
![Screenshot](https://raw.github.com/anthonydahanne/showtime-plugin-tv5video.ca/master/screenshots/tv5video.ca-listofshows.png "list of shows")
![Screenshot](https://raw.github.com/anthonydahanne/showtime-plugin-tv5video.ca/master/screenshots/tv5video.ca-listofepisodes.png "list of episodes")

## License notes

(c) 2014 Anthony Dahanne [anthony.dahanne@gmail.com](mailto:anthony.dahanne@gmail.com) ; http://blog.dahanne.net


TV5Video.ca Showtime plugin is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

TV5Video.ca Showtime plugin is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with TV5Video.ca Showtime plugin.  If not, see http://www.gnu.org/licenses/.

## Installing

TV5Video.ca Showtime plugin, is available directly from the Showtime plugin repository. Just install it from there (the puzzle piece in showtime homepage right top corner).

TV5Video.ca Showtime plugin, *needs* Showtime version >= 4.3.167

- Official versions: https://showtimemediacenter.com/plugins/showtime

## Infos and special thanks

Examples of few TV5Video.ca useful urls to list shows :
-  http://m.video.tv5.ca/api/json/application/genres
-  http://m.video.tv5.ca/api/json/application/nouveautes
-  http://m.video.tv5.ca/api/json/application/a_z

And then getting a specific show information is as easy as :
 
    POST /api/json/tools/loadSerieEmissions HTTP/1.1
    Content-Length: 82
    Content-Type: application/x-www-form-urlencoded
    Host: m.video.tv5.ca
    Connection: Keep-Alive
    parameters=%7B%22id%22%3A%22623%22%2C%22pagesize%22%3A%2216%22%2C%22page%22%3A1%7D

THe last line being decoded to :

    parameters={"id":"623","pagesize":"16","page":1}


-  Thanks to Andreas Öman (https://www.lonelycoder.com/ , author of Showtime) for this great media center
-  I took inspiration on my previous work on https://github.com/anthonydahanne/showtime-plugin-tou.tv
