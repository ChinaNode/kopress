kopress
=======

TJ's new framework [Koa](https://github.com/koajs/koa) is a prettry awesome thing, enable us
write asynchronous code in a more enjoyable way. But koa is more like Connect, only have the
basic HTTP methods and function. And TJ [has no plan](https://github.com/koajs/koa/issues/239#issuecomment-37491315)
for a express like framework. So we create the Kopress.

Kopress is based on koa, and more like express. It provide complete server function
 such as router, template, logger, session and so on. Kopress's target is
  `same function as express, used like express, no callback`.

## Current status
kopress now is just a application generator just like [express generator](https://github.com/expressjs/generator).
it is a command line tool which can generate a basic kopress application. A kopress application is koa plus serveral
most common used http middleware. In the future we will proceed a lot deep develop to reach our target.

Koa now is just 0.5, and the middlewares are not mature, Kopress will keep update for koa and better middleware.

## Install
```
$ npm install -g kopress-generator
```

## Quick Start
```bash
$ kopress /tmp/appname
$ cd /tmp/appname && npm install
$ node app.js
```
Now you can visit the service at http://localhost:3000

`note`: because co and koa require node version higher than 0.11.9, so is kopress, or you can use [gnode](https://github.com/TooTallNate/gnode)

## How to use

## Included middleware

Here is the middleware table compare to Express 4.0

| Kopress | Express 4.0 |
|:---:|:---:|
| koa-body | body-parser |
| koa-compress | compression |
| - | cookie-session |
| koa-logger | morgan |
| - | cookie-parser |
| session | express-session |
| koa-favi | static-favicon |
| koa-response | response-time |
| koa-error | errorhandler |
| koa-method-override | method-override |
| - | connect-timeout |
| koa-vhost | vhost |
| csrf | csurf |

Kopress also use these middlewares:

- [koa-router](https://github.com/alexmingoia/koa-router) as default router middleware
- [koa-views](https://github.com/queckezz/koa-views) provide almost any template engine support
- [koa-qs](https://github.com/koajs/qs) parse querystring

## TODO

* cookie & session
* bodyParser
* provide same api to express

## Related project
* [koan](https://github.com/soygul/koan) KOAN Stack (Koa, Angular, Node, Mongo, WebSockets) for real-time full-stack JavaScript web development.
* [co-express](https://github.com/mciparelli/co-express) is a interesting module, that enables generators to be used as middlewares.
* [api-boilerplate](https://github.com/koajs/api-boilerplate) is a koa api service develop boilerplate.
* [okey](https://github.com/dead-horse/okey) a high layer framework base on koa

## Resource

* [koa](https://github.com/koajs/koa)
* [koa site](http://koajs.com/)
* [koa middleware](https://github.com/koajs/koa/wiki)
* [co](https://github.com/visionmedia/co)
* [co compatible module](https://github.com/visionmedia/co/wiki)
* [express generator](https://github.com/expressjs/generator)


## Open source
Kopress is a open source project, pull request are welcome.

## License
(The MIT License)

Copyright (c) 2014 Pana &lt;pana.wang@outlook.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
