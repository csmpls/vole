idas blue
====

Idas Blue is a web application for rapid, encrypted messaging with no third parties (servers etc).

When the user hits "post," text is encrypted and stored locally as JSON. JSON files are synced direct-to-peers using BitTorrent sync, at which point it is encrypted again. Readers decrypt JSON files in the web browser, so, if you use your browser in "privacy mode," plaintext files are unlikely to be stored permanetly on the disk. 

* idas blue is a fork of [vole.cc](http://vole.cc).
* Uses the [Stanford JS Crypto library](http://crypto.stanford.edu/sjcl/), which is awesome (but go bears). 

Getting started
---------------

Read "contrib.md." For now you need to install [Bittorrent Sync](http://labs.bittorrent.com/experiments/sync.html) separately.

Following others
----------------

* Grab the **read-only** ID of the person you want to follow. A directory is in progress at [vole.cc](http://vole.cc). Why not start with Vole Team updates? Our key is RA32XLBBHXMWMECGJAJSJMMPQ3Z2ZGR7K.
* Find the Idas Blue `users` folder. Unless you changed the defaults, it will be in a directory called `idas-blue/users` in your home folder.
* Create a new folder in `idas-blue/users`, you should name it after the user that you're about to follow. For example, `idas-blue/users/voleteam`.
* In BitTorrent Sync, add this new folder as a shared folder, using the read-only key you grabbed in step 1. [Instructions](http://labs.bittorrent.com/experiments/sync/get-started.html) are available on their site and vary a little by operating system.
![OSX Screenshot](https://f.cloud.github.com/assets/453297/692312/c113737a-dc18-11e2-84e4-dee7e0507c08.png)
* You should receive notification that the folder has sync'd.
* In your browser, see the new posts appear.

Sharing your posts
------------------

Find your own user folder, for example, if you created a profile named 'Chuck':

    /home/chuck/idas-blue/users/Chuck_9674e8e8-7c7a-41e6-52ed-51a3f7969812

* In Bittorrent Sync, add this folder as a shared folder.
* In the folder options, grab the **read-only key**. Make sure the key starts with the letter 'B' that signifies it's the read-only one. You can find it by going to the advanced folder preferences. This is the key that you can share with others so they can follow your posts.
* If you want to list your key on vole.cc, make a pull request on the [website repo](https://github.com/vole/vole.github.io). Here is an [example](https://github.com/vole/vole.github.io/pull/9).

Configuration
-------------

To override the default configuration options, make a copy of `config.sample.json` and name it `config.json`.

Change the `server.listen` value to `0.0.0.0:6789` to listen for requests from any network device, instead of just the local machine.


Technology
----------

* [stanford javascript crypto library](http://crypto.stanford.edu/sjcl/)
* [bittorrent sync](http://labs.bittorrent.com/experiments/sync.html)
* [Vole](http://vole.cc)
* [Go](http://golang.org/)
* [Ember.js](http://emberjs.com/)

License
-------

all Vole code copyright (C) 2013 Vole development team

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
