Electron DevTools Installer
---------------------------

[![Build Status](https://travis-ci.org/GPMDP/electron-devtools-installer.svg?branch=master)](https://travis-ci.org/GPMDP/electron-devtools-installer)

This is an easy way to install DevTool extensions into Electron.  You shouldn't
have to mess around with downloading the extension, finding the right folder and
then configuring the path for everyone's machines.

All you have to do now is

```js
import installExtension from 'electron-devtools-installer';

// This is the extension ID of React Dev Tools
const extensionID = 'fmkadmapgofadopljbjfkapdkoienihi';

installExtension(extensionID)
    .then((name) => console.log(`Added Extension:  ${name}`))
    .catch((err) => console.log('An error occurred: ', err));
```

## How does it work?

Well, you know those steps over in the [Electron Docs](https://github.com/electron/electron/blob/master/docs/tutorial/devtools-extension.md)
that involve downloading, copying, checking paths, Etc.

This does all of that for you, it downloads the chrome extension directly from
the Chrome WebStore.  Then it extracts it to your applications `userData` directory
before loading it into Electron.


License
-------

The MIT License (MIT)

Copyright (c) 2016 Samuel Attard

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
