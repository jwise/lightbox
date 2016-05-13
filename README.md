# lightbox: A tiny little web album generator.

Periodically, I find the urge to put photos up on the web of things that
I've done or places that I've been.  This repository is the evolution of a
ball-of-wax shell script, and its accompanying pieces of web detritus that
go with it.

## Included in this package...

You'll find included here:

* one `GEN`, which is the master driver that turns a bunch of photos into an index.html;
* one `retina.js`, a modified derivative of https://github.com/imulus/retinajs (MIT License; Copyright (c) 2013-2016 Axial, LLC, Ben Atkin, and other contributors);
* one `lightbox.css`, a chunk of CSS that gives the album its distinctive look;
* and one sample pair of `header.html` and `footer.html`, which are simply templates that are glued on the top and bottom of every file.

## Usage instructions

The approximate state of the art right now is to do something like:

* Clone this repository.
* Create a directory called 'scale' inside.
* Modify `header.html` and `footer.html` to your needs.
* Drop all your photos in the directory with this script and the other supporting files.
* Ensure that their file timestamps are the timestamp order you want (`jhead -ft *` helps here).
* Create description and surrounding files, as desired:
  * `.desc` files are one-liners that describe a single image.
  * `.post` files get inserted immediately after an image (good for section dividers).
  * `.pre` files go right above an image, in a `photopre` class.  So use `<div class="words">` surrounding text that you want to go before an image if you have a longer-form description.
* Invoke `GEN`.
* Tweak all of your surrounding files, and continue to invoke `GEN`.  Already scaled images will be reused.
