# Mimetypes

Creates a JSON document containing a thorough list of file extensions => mime types as provided by the
[Apache httpd project](http://httpd.apache.org).


## How to use

### Step 1

Download the latest copy of the Apache `mime-types` file into the same directory as the `generate` script.

```bash
cd mimetypes &&
wget --no-check-certificate https://svn.apache.org/repos/asf/httpd/httpd/branches/2.4.x/docs/conf/mime.types
```

### Step 1.5 (optional)

Update the provided `customize.json` document with any additional mimetypes to define, or any that you would like to
override.

### Step 2

Run the `generate` script.

```bash
./generate
```

In the end, a `mimetypes.json` document will be generated. This JSON document can be easily parsed into a
map/dictionary/associative array by pretty much every programming language with little effort.

It also generates a backing PHP class if you want to use the data in PHP-land.

## Installation
### Install source from GitHub
To install the source code:

```bash
git clone git://github.com/skyzyx/mimetypes.git
```

And use it in your scripts:

```php
$mimetypes = json_decode('/path/to/mimetypes/mimetypes.json');
$type = $mimetypes['html'];
#=> text/html

// ...or...

use Skyzyx\Components\Mimetypes\Mimetypes;
$type = Mimetypes::getInstance()->fromExtension('html');
#=> text/html
```


### Install with Composer
If you're using [Composer](http://getcomposer.org) to manage dependencies, you can add the mimetypes with it.

```json
{
    "require": {
        "skyzyx/mimetypes": ">=1.0"
    }
}
```


## See Also...
For a similar-yet-different approach (including reverse-lookups from `mimetypes => extensions`), check out
[dflydev-apache-mime-types](https://github.com/dflydev/dflydev-apache-mime-types).


## License & Copyright
Copyright (c) 2010-2013 [Ryan Parman](http://ryanparman.com). Licensed for use under the terms of the
[MIT license](http://www.opensource.org/licenses/mit-license.php). See the
[list of contributors](https://github.com/skyzyx/mimetypes/contributors) for more author information.
