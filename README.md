# rQRCode-image, Encode QRCodes, Render QR Code Images

## Overview

rQRCode-image is a library for encoding QR Codes, and render images using RMagick in Ruby. It has a simple interface with all the standard qrcode options. It is a fork of whomwah(Duncan Robertson's rqrcode gem).

Let's clear up some rQRCode-image stuff.

* rQRCode-image is NOT a __standalone library__ It requires RMagick and thus ImageMagick.
* It is an encoding library. You can't decode QR codes with it.
* The interface is simple and assumes you just want to encode a string into a QR code, then render an image of the QR Code
* QR code is trademarked by Denso Wave inc

## Resources

* wikipedia:: http://en.wikipedia.org/wiki/QR_Code
* Denso-Wave website:: http://www.denso-wave.com/qrcode/index-e.html
* kaywa:: http://qrcode.kaywa.com
* RMagic:: http://rmagick.rubyforge.org/
* ImageMagick:: http://http://www.imagemagick.org

## Installing

You can get the latest source from http://github.com/bluetwin/rqrcode-image

    git clone git://github.com/bluetwin/rqrcode-image.git

## Tests

To run the tests:

    $ rake
 
## Loading rQRCode-image Itself

You have installed the gem already, yeah?

    require 'rubygems'
    require 'rqrcode-image'

## Simple QRCode generation to ImageBlob

```ruby
qr = RQRCodeImage::QRCode.new( 'my string to generate', :size => 4, :level => :h )
puts qr.to_image


## Simple QRCode generation to template (RubyOnRails)

```erb
# Controller
@qr = RQRCodeImage::QRCode.new( 'my string to generate', :size => 4, :level => :h )

# View: (minimal styling added)

```
## Authors

Original rqrcode author: Duncan Robertson
Forked by(as done by many others) : Brandon Sislow

Special thanks to the following people for submitting patches to rqrcode:
* [Duncan Robertson] (https://github.com/whomwah)
* [Chris Mowforth](http://blog.99th.st)
* [Daniel Schierbeck](https://github.com/dasch)
* [Gioele Barabucci](https://github.com/gioele) 
* [Ken Collins](https://github.com/metaskills)
* [Rob la Lau](https://github.com/ohreally)
* [Tore Darell](http://tore.darell.no)
* Vladislav Gorodetskiy

## Contributing
* Fork the project
* Send a pull request
* Don't touch the .gemspec, I'll do that when I release a new version

## Copyright

MIT Licence (http://www.opensource.org/licenses/mit-license.html)
