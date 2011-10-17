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

Copyright (c) 2011 Ryan Parman

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

<http://opensource.org/licenses/MIT>
