# Mimetypes

Creates a JSON document containing a thorough list of file extensions => mime types as provided by the [Apache httpd project](http://httpd.apache.org).


## How to use

### Step one

Download the latest copy of the Apache `mime-types` file into the same directory as the `generate` script.

	cd mimetypes &&
	wget --no-check-certificate https://svn.apache.org/repos/asf/httpd/httpd/branches/2.0.x/docs/conf/mime.types

### Step one-and-a-half (optional)

Update the provided `customize.json` document with any additional mimetypes to define, or any that you would like to override.

### Step two

Run the `generate` script.

	./generate

In the end, a `mimetypes.json` document will be generated. This JSON document can be easily parsed into a map/dictionary/associative array by pretty much every programming language with little effort.


## License & Copyright
Copyright (c) 2010-2012 [Ryan Parman](http://ryanparman.com). Licensed for use under the terms of the [MIT license](http://www.opensource.org/licenses/mit-license.php).
