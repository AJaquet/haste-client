# Haste Client

haste-client is a simple client for uploading data to haste.  Usage is very simple, all you do it pipe data in STDIN:

`cat file | haste`

And once the file makes it to the server, it will print the URL to STDOUT.

This can be really really cool in combination with `pbcopy`, like:

`cat file | haste | pbcopy`

after which the contents of `file` will be accessible at a URL which has been copied to your pasteboard.

## Changing the location of your haste server

By default, haste is expected to be running on `http://localhost:7777`, which I'm sure no one is doing.  You can change this by setting the value of ENV['HASTE_SERVER'] to the URL of your haste server.  You can use `alias` to make easy shortcuts if you commonly use a few hastes intermingled with each other.  To do that, you'd put something like

alias work_haste="HASTE_SERVER=http://something.com haste"

After which you can use `work_haste` to send hastes there.

## Author

John Crepezzi <john.crepezzi@gmail.com>

## License

(The MIT License)

Copyright © 2011 John Crepezzi

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE
