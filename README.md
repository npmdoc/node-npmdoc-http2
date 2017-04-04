# api documentation for  [http2 (v3.3.6)](https://github.com/molnarg/node-http2)  [![npm package](https://img.shields.io/npm/v/npmdoc-http2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-http2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-http2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-http2)
#### An HTTP/2 client and server implementation

[![NPM](https://nodei.co/npm/http2.png?downloads=true)](https://www.npmjs.com/package/http2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-http2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-http2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gábor Molnár",
        "email": "gabor@molnar.es",
        "url": "http://gabor.molnar.es"
    },
    "bugs": {
        "url": "https://github.com/molnarg/node-http2/issues"
    },
    "contributors": [
        {
            "name": "Nick Hurley"
        },
        {
            "name": "Mike Belshe"
        },
        {
            "name": "Yoshihiro Iwanaga"
        },
        {
            "name": "Igor Novikov"
        },
        {
            "name": "James Willcox"
        },
        {
            "name": "David Björklund"
        },
        {
            "name": "Patrick McManus"
        }
    ],
    "dependencies": {},
    "description": "An HTTP/2 client and server implementation",
    "devDependencies": {
        "bunyan": "*",
        "chai": "*",
        "docco": "*",
        "istanbul": "*",
        "mocha": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "7df06227e02b5b5a5841deea08239b3198d04bec",
        "tarball": "https://registry.npmjs.org/http2/-/http2-3.3.6.tgz"
    },
    "engines": {
        "node": ">=0.12.0"
    },
    "gitHead": "2c4c310f414d3249421340c0e2618873b07c17cb",
    "homepage": "https://github.com/molnarg/node-http2",
    "keywords": [
        "http",
        "http2",
        "client",
        "server"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "molnarg",
            "email": "gabor.molnar@sch.bme.hu"
        },
        {
            "name": "todesschaf",
            "email": "hurley@todesschaf.org"
        }
    ],
    "name": "http2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/molnarg/node-http2.git"
    },
    "scripts": {
        "doc": "docco lib/* --output doc --layout parallel --template root.jst --css doc/docco.css && docco lib/protocol/* --output doc/protocol --layout parallel --template protocol.jst --css doc/docco.css",
        "test": "istanbul test _mocha -- --reporter spec --slow 500 --timeout 15000"
    },
    "version": "3.3.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module http2](#apidoc.module.http2)
1.  [function <span class="apidocSignatureSpan">http2.</span>Agent (options)](#apidoc.element.http2.Agent)
1.  [function <span class="apidocSignatureSpan">http2.</span>ClientRequest ()](#apidoc.element.http2.ClientRequest)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingMessage (stream)](#apidoc.element.http2.IncomingMessage)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingRequest (stream)](#apidoc.element.http2.IncomingRequest)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingResponse (stream)](#apidoc.element.http2.IncomingResponse)
1.  [function <span class="apidocSignatureSpan">http2.</span>OutgoingMessage ()](#apidoc.element.http2.OutgoingMessage)
1.  [function <span class="apidocSignatureSpan">http2.</span>OutgoingRequest ()](#apidoc.element.http2.OutgoingRequest)
1.  [function <span class="apidocSignatureSpan">http2.</span>OutgoingResponse (stream)](#apidoc.element.http2.OutgoingResponse)
1.  [function <span class="apidocSignatureSpan">http2.</span>Server (options)](#apidoc.element.http2.Server)
1.  [function <span class="apidocSignatureSpan">http2.</span>ServerResponse (stream)](#apidoc.element.http2.ServerResponse)
1.  [function <span class="apidocSignatureSpan">http2.</span>createServer (options, requestListener)](#apidoc.element.http2.createServer)
1.  [function <span class="apidocSignatureSpan">http2.</span>get (options, callback)](#apidoc.element.http2.get)
1.  [function <span class="apidocSignatureSpan">http2.</span>protocol.Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint)
1.  [function <span class="apidocSignatureSpan">http2.</span>request (options, callback)](#apidoc.element.http2.request)
1.  object <span class="apidocSignatureSpan">http2.</span>Agent.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>ClientRequest.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>IncomingMessage.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>IncomingRequest.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>IncomingResponse.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>OutgoingMessage.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>OutgoingResponse.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>STATUS_CODES
1.  object <span class="apidocSignatureSpan">http2.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>globalAgent
1.  object <span class="apidocSignatureSpan">http2.</span>http
1.  object <span class="apidocSignatureSpan">http2.</span>https
1.  object <span class="apidocSignatureSpan">http2.</span>protocol
1.  object <span class="apidocSignatureSpan">http2.</span>protocol.Endpoint.prototype
1.  object <span class="apidocSignatureSpan">http2.</span>raw
1.  object <span class="apidocSignatureSpan">http2.</span>serializers

#### [module http2.Agent](#apidoc.module.http2.Agent)
1.  [function <span class="apidocSignatureSpan">http2.</span>Agent (options)](#apidoc.element.http2.Agent.Agent)

#### [module http2.Agent.prototype](#apidoc.module.http2.Agent.prototype)
1.  [function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>destroy (error)](#apidoc.element.http2.Agent.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>get (options, callback)](#apidoc.element.http2.Agent.prototype.get)
1.  [function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>request (options, callback)](#apidoc.element.http2.Agent.prototype.request)

#### [module http2.ClientRequest](#apidoc.module.http2.ClientRequest)
1.  [function <span class="apidocSignatureSpan">http2.</span>ClientRequest ()](#apidoc.element.http2.ClientRequest.ClientRequest)

#### [module http2.ClientRequest.prototype](#apidoc.module.http2.ClientRequest.prototype)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_fallback (request)](#apidoc.element.http2.ClientRequest.prototype._fallback)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_onPromise (stream, headers)](#apidoc.element.http2.ClientRequest.prototype._onPromise)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_start (stream, options)](#apidoc.element.http2.ClientRequest.prototype._start)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>abort ()](#apidoc.element.http2.ClientRequest.prototype.abort)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>on (event, listener)](#apidoc.element.http2.ClientRequest.prototype.on)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setNoDelay (noDelay)](#apidoc.element.http2.ClientRequest.prototype.setNoDelay)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setPriority (priority)](#apidoc.element.http2.ClientRequest.prototype.setPriority)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setSocketKeepAlive (enable, initialDelay)](#apidoc.element.http2.ClientRequest.prototype.setSocketKeepAlive)
1.  [function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setTimeout (timeout, callback)](#apidoc.element.http2.ClientRequest.prototype.setTimeout)

#### [module http2.IncomingMessage](#apidoc.module.http2.IncomingMessage)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingMessage (stream)](#apidoc.element.http2.IncomingMessage.IncomingMessage)

#### [module http2.IncomingMessage.prototype](#apidoc.module.http2.IncomingMessage.prototype)
1.  [function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_checkSpecialHeader (key, value)](#apidoc.element.http2.IncomingMessage.prototype._checkSpecialHeader)
1.  [function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_onEnd ()](#apidoc.element.http2.IncomingMessage.prototype._onEnd)
1.  [function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingMessage.prototype._onHeaders)
1.  [function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_validateHeaders (headers)](#apidoc.element.http2.IncomingMessage.prototype._validateHeaders)
1.  [function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>setTimeout ()](#apidoc.element.http2.IncomingMessage.prototype.setTimeout)

#### [module http2.IncomingRequest](#apidoc.module.http2.IncomingRequest)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingRequest (stream)](#apidoc.element.http2.IncomingRequest.IncomingRequest)

#### [module http2.IncomingRequest.prototype](#apidoc.module.http2.IncomingRequest.prototype)
1.  [function <span class="apidocSignatureSpan">http2.IncomingRequest.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingRequest.prototype._onHeaders)

#### [module http2.IncomingResponse](#apidoc.module.http2.IncomingResponse)
1.  [function <span class="apidocSignatureSpan">http2.</span>IncomingResponse (stream)](#apidoc.element.http2.IncomingResponse.IncomingResponse)

#### [module http2.IncomingResponse.prototype](#apidoc.module.http2.IncomingResponse.prototype)
1.  [function <span class="apidocSignatureSpan">http2.IncomingResponse.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingResponse.prototype._onHeaders)

#### [module http2.OutgoingMessage](#apidoc.module.http2.OutgoingMessage)
1.  [function <span class="apidocSignatureSpan">http2.</span>OutgoingMessage ()](#apidoc.element.http2.OutgoingMessage.OutgoingMessage)

#### [module http2.OutgoingMessage.prototype](#apidoc.module.http2.OutgoingMessage.prototype)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_checkSpecialHeader (key, value)](#apidoc.element.http2.OutgoingMessage.prototype._checkSpecialHeader)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_finish ()](#apidoc.element.http2.OutgoingMessage.prototype._finish)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_write (chunk, encoding, callback)](#apidoc.element.http2.OutgoingMessage.prototype._write)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>addTrailers (trailers)](#apidoc.element.http2.OutgoingMessage.prototype.addTrailers)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>getHeader (name)](#apidoc.element.http2.OutgoingMessage.prototype.getHeader)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>removeHeader (name)](#apidoc.element.http2.OutgoingMessage.prototype.removeHeader)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>setHeader (name, value)](#apidoc.element.http2.OutgoingMessage.prototype.setHeader)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>setTimeout ()](#apidoc.element.http2.OutgoingMessage.prototype.setTimeout)

#### [module http2.OutgoingResponse](#apidoc.module.http2.OutgoingResponse)
1.  [function <span class="apidocSignatureSpan">http2.</span>OutgoingResponse (stream)](#apidoc.element.http2.OutgoingResponse.OutgoingResponse)

#### [module http2.OutgoingResponse.prototype](#apidoc.module.http2.OutgoingResponse.prototype)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_implicitHeader ()](#apidoc.element.http2.OutgoingResponse.prototype._implicitHeader)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_implicitHeaders ()](#apidoc.element.http2.OutgoingResponse.prototype._implicitHeaders)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_onRequestHeaders (headers)](#apidoc.element.http2.OutgoingResponse.prototype._onRequestHeaders)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>altsvc (host, port, protocolID, maxAge, origin)](#apidoc.element.http2.OutgoingResponse.prototype.altsvc)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>end ()](#apidoc.element.http2.OutgoingResponse.prototype.end)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>on (event, listener)](#apidoc.element.http2.OutgoingResponse.prototype.on)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>push (options)](#apidoc.element.http2.OutgoingResponse.prototype.push)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>write ()](#apidoc.element.http2.OutgoingResponse.prototype.write)
1.  [function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>writeHead (statusCode, reasonPhrase, headers)](#apidoc.element.http2.OutgoingResponse.prototype.writeHead)

#### [module http2.Server](#apidoc.module.http2.Server)
1.  [function <span class="apidocSignatureSpan">http2.</span>Server (options)](#apidoc.element.http2.Server.Server)

#### [module http2.Server.prototype](#apidoc.module.http2.Server.prototype)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>_fallback (socket)](#apidoc.element.http2.Server.prototype._fallback)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>_start (socket)](#apidoc.element.http2.Server.prototype._start)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>addContext (hostname, credentials)](#apidoc.element.http2.Server.prototype.addContext)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>address ()](#apidoc.element.http2.Server.prototype.address)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>close (callback)](#apidoc.element.http2.Server.prototype.close)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>listen (port, hostname)](#apidoc.element.http2.Server.prototype.listen)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>on (event, listener)](#apidoc.element.http2.Server.prototype.on)
1.  [function <span class="apidocSignatureSpan">http2.Server.prototype.</span>setTimeout (timeout, callback)](#apidoc.element.http2.Server.prototype.setTimeout)

#### [module http2.http](#apidoc.module.http2.http)
1.  [function <span class="apidocSignatureSpan">http2.http.</span>createServer ()](#apidoc.element.http2.http.createServer)
1.  [function <span class="apidocSignatureSpan">http2.http.</span>get ()](#apidoc.element.http2.http.get)
1.  [function <span class="apidocSignatureSpan">http2.http.</span>request ()](#apidoc.element.http2.http.request)

#### [module http2.https](#apidoc.module.http2.https)
1.  [function <span class="apidocSignatureSpan">http2.https.</span>createServer (options, requestListener)](#apidoc.element.http2.https.createServer)
1.  [function <span class="apidocSignatureSpan">http2.https.</span>get (options, callback)](#apidoc.element.http2.https.get)
1.  [function <span class="apidocSignatureSpan">http2.https.</span>request (options, callback)](#apidoc.element.http2.https.request)

#### [module http2.protocol](#apidoc.module.http2.protocol)
1.  [function <span class="apidocSignatureSpan">http2.protocol.</span>Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint)
1.  object <span class="apidocSignatureSpan">http2.protocol.</span>serializers
1.  string <span class="apidocSignatureSpan">http2.protocol.</span>VERSION

#### [module http2.protocol.Endpoint](#apidoc.module.http2.protocol.Endpoint)
1.  [function <span class="apidocSignatureSpan">http2.protocol.</span>Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint.Endpoint)

#### [module http2.protocol.Endpoint.prototype](#apidoc.module.http2.protocol.Endpoint.prototype)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_error (component, error)](#apidoc.element.http2.protocol.Endpoint.prototype._error)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeDataFlow (role, settings, filters)](#apidoc.element.http2.protocol.Endpoint.prototype._initializeDataFlow)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeErrorHandling ()](#apidoc.element.http2.protocol.Endpoint.prototype._initializeErrorHandling)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeManagement ()](#apidoc.element.http2.protocol.Endpoint.prototype._initializeManagement)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_read ()](#apidoc.element.http2.protocol.Endpoint.prototype._read)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_readPrelude ()](#apidoc.element.http2.protocol.Endpoint.prototype._readPrelude)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_write (chunk, encoding, done)](#apidoc.element.http2.protocol.Endpoint.prototype._write)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_writePrelude ()](#apidoc.element.http2.protocol.Endpoint.prototype._writePrelude)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>close (error)](#apidoc.element.http2.protocol.Endpoint.prototype.close)
1.  [function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>createStream ()](#apidoc.element.http2.protocol.Endpoint.prototype.createStream)

#### [module http2.raw](#apidoc.module.http2.raw)
1.  [function <span class="apidocSignatureSpan">http2.raw.</span>createServer (options, requestListener)](#apidoc.element.http2.raw.createServer)
1.  [function <span class="apidocSignatureSpan">http2.raw.</span>get (options, callback)](#apidoc.element.http2.raw.get)
1.  [function <span class="apidocSignatureSpan">http2.raw.</span>request (options, callback)](#apidoc.element.http2.raw.request)

#### [module http2.serializers](#apidoc.module.http2.serializers)
1.  [function <span class="apidocSignatureSpan">http2.serializers.</span>data (data)](#apidoc.element.http2.serializers.data)
1.  [function <span class="apidocSignatureSpan">http2.serializers.</span>e (endpoint)](#apidoc.element.http2.serializers.e)
1.  [function <span class="apidocSignatureSpan">http2.serializers.</span>frame (frame)](#apidoc.element.http2.serializers.frame)
1.  [function <span class="apidocSignatureSpan">http2.serializers.</span>s (stream)](#apidoc.element.http2.serializers.s)



# <a name="apidoc.module.http2"></a>[module http2](#apidoc.module.http2)

#### <a name="apidoc.element.http2.Agent"></a>[function <span class="apidocSignatureSpan">http2.</span>Agent (options)](#apidoc.element.http2.Agent)
- description and source-code
```javascript
function Agent(options) {
  EventEmitter.call(this);
  this.setMaxListeners(0);

  options = util._extend({}, options);

  this._settings = options.settings;
  this._log = (options.log || defaultLogger).child({ component: 'http' });
  this.endpoints = {};

  // * Using an own HTTPS agent, because the global agent does not look at 'NPN/ALPNProtocols' when
  //   generating the key identifying the connection, so we may get useless non-negotiated TLS
  //   channels even if we ask for a negotiated one. This agent will contain only negotiated
  //   channels.
  options.ALPNProtocols = supportedProtocols;
  options.NPNProtocols = supportedProtocols;
  this._httpsAgent = new https.Agent(options);

  this.sockets = this._httpsAgent.sockets;
  this.requests = this._httpsAgent.requests;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest"></a>[function <span class="apidocSignatureSpan">http2.</span>ClientRequest ()](#apidoc.element.http2.ClientRequest)
- description and source-code
```javascript
function OutgoingRequest() {
  OutgoingMessage.call(this);

  this._log = undefined;

  this.stream = undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingMessage"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingMessage (stream)](#apidoc.element.http2.IncomingMessage)
- description and source-code
```javascript
function IncomingMessage(stream) {
  // * This is basically a read-only wrapper for the [Stream](protocol/stream.html) class.
  PassThrough.call(this);
  stream.pipe(this);
  this.socket = this.stream = stream;

  this._log = stream._log.child({ component: 'http' });

  // * HTTP/2.0 does not define a way to carry the version identifier that is included in the
  //   HTTP/1.1 request/status line. Version is always 2.0.
  this.httpVersion = '2.0';
  this.httpVersionMajor = 2;
  this.httpVersionMinor = 0;

  // * 'this.headers' will store the regular headers (and none of the special colon headers)
  this.headers = {};
  this.trailers = undefined;
  this._lastHeadersSeen = undefined;

  // * Other metadata is filled in when the headers arrive.
  stream.once('headers', this._onHeaders.bind(this));
  stream.once('end', this._onEnd.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingRequest"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingRequest (stream)](#apidoc.element.http2.IncomingRequest)
- description and source-code
```javascript
function IncomingRequest(stream) {
  IncomingMessage.call(this, stream);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingResponse"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingResponse (stream)](#apidoc.element.http2.IncomingResponse)
- description and source-code
```javascript
function IncomingResponse(stream) {
  IncomingMessage.call(this, stream);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage"></a>[function <span class="apidocSignatureSpan">http2.</span>OutgoingMessage ()](#apidoc.element.http2.OutgoingMessage)
- description and source-code
```javascript
function OutgoingMessage() {
  // * This is basically a read-only wrapper for the [Stream](protocol/stream.html) class.
  Writable.call(this);

  this._headers = {};
  this._trailers = undefined;
  this.headersSent = false;
  this.finished = false;

  this.on('finish', this._finish);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingRequest"></a>[function <span class="apidocSignatureSpan">http2.</span>OutgoingRequest ()](#apidoc.element.http2.OutgoingRequest)
- description and source-code
```javascript
function OutgoingRequest() {
  OutgoingMessage.call(this);

  this._log = undefined;

  this.stream = undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse"></a>[function <span class="apidocSignatureSpan">http2.</span>OutgoingResponse (stream)](#apidoc.element.http2.OutgoingResponse)
- description and source-code
```javascript
function OutgoingResponse(stream) {
  OutgoingMessage.call(this);

  this._log = stream._log.child({ component: 'http' });

  this.stream = stream;
  this.statusCode = 200;
  this.sendDate = true;

  this.stream.once('headers', this._onRequestHeaders.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server"></a>[function <span class="apidocSignatureSpan">http2.</span>Server (options)](#apidoc.element.http2.Server)
- description and source-code
```javascript
function Server(options) {
  options = util._extend({}, options);

  this._log = (options.log || defaultLogger).child({ component: 'http' });
  this._settings = options.settings;

  var start = this._start.bind(this);
  var fallback = this._fallback.bind(this);

  // HTTP2 over TLS (using NPN or ALPN)
  if ((options.key && options.cert) || options.pfx) {
    this._log.info('Creating HTTP/2 server over TLS');
    this._mode = 'tls';
    options.ALPNProtocols = supportedProtocols;
    options.NPNProtocols = supportedProtocols;
    options.ciphers = options.ciphers || cipherSuites;
    options.honorCipherOrder = (options.honorCipherOrder != false);
    this._server = https.createServer(options);
    this._originalSocketListeners = this._server.listeners('secureConnection');
    this._server.removeAllListeners('secureConnection');
    this._server.on('secureConnection', function(socket) {
      var negotiatedProtocol = socket.alpnProtocol || socket.npnProtocol;
      // It's true that the client MUST use SNI, but if it doesn't, we don't care, don't fall back to HTTP/1,
      // since if the ALPN negotiation is otherwise successful, the client thinks we speak HTTP/2 but we don't.
      if (negotiatedProtocol === protocol.VERSION) {
        start(socket);
      } else {
        fallback(socket);
      }
    });
    this._server.on('request', this.emit.bind(this, 'request'));

    forwardEvent('error', this._server, this);
    forwardEvent('listening', this._server, this);
  }

  // HTTP2 over plain TCP
  else if (options.plain) {
    this._log.info('Creating HTTP/2 server over plain TCP');
    this._mode = 'plain';
    this._server = net.createServer(start);
  }

  // HTTP/2 with HTTP/1.1 upgrade
  else {
    this._log.error('Trying to create HTTP/2 server with Upgrade from HTTP/1.1');
    throw new Error('HTTP1.1 -> HTTP2 upgrade is not yet supported. Please provide TLS keys.');
  }

  this._server.on('close', this.emit.bind(this, 'close'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ServerResponse"></a>[function <span class="apidocSignatureSpan">http2.</span>ServerResponse (stream)](#apidoc.element.http2.ServerResponse)
- description and source-code
```javascript
function OutgoingResponse(stream) {
  OutgoingMessage.call(this);

  this._log = stream._log.child({ component: 'http' });

  this.stream = stream;
  this.statusCode = 200;
  this.sendDate = true;

  this.stream.once('headers', this._onRequestHeaders.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.createServer"></a>[function <span class="apidocSignatureSpan">http2.</span>createServer (options, requestListener)](#apidoc.element.http2.createServer)
- description and source-code
```javascript
function createServerTLS(options, requestListener) {
  if (typeof options === 'function') {
    throw new Error('options are required!');
  }
  if (!options.pfx && !(options.key && options.cert)) {
    throw new Error('options.pfx or options.key and options.cert are required!');
  }
  options.plain = false;

  var server = new Server(options);

  if (requestListener) {
    server.on('request', requestListener);
  }

  return server;
}
```
- example usage
```shell
...

'''javascript
var options = {
  key: fs.readFileSync('./example/localhost.key'),
  cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
...
```

#### <a name="apidoc.element.http2.get"></a>[function <span class="apidocSignatureSpan">http2.</span>get (options, callback)](#apidoc.element.http2.get)
- description and source-code
```javascript
function getTLS(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = false;
  if (options.protocol && options.protocol !== "https:") {
    throw new Error('This interface only supports https-schemed URLs');
  }
  if (options.agent && typeof(options.agent.get) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.get(agentOptions, callback);
  }
  return exports.globalAgent.get(options, callback);
}
```
- example usage
```shell
...
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
  response.pipe(process.stdout);
});
'''

### Simple static file server ###

An simple static file server serving up content from its own directory is available in the 'example'
...
```

#### <a name="apidoc.element.http2.protocol.Endpoint"></a>[function <span class="apidocSignatureSpan">http2.</span>protocol.Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint)
- description and source-code
```javascript
function Endpoint(log, role, settings, filters) {
  Duplex.call(this);

  // * Initializing logging infrastructure
  this._log = log.child({ component: 'endpoint', e: this });

  // * First part of the handshake process: sending and receiving the client connection header
  //   prelude.
  assert((role === 'CLIENT') || role === 'SERVER');
  if (role === 'CLIENT') {
    this._writePrelude();
  } else {
    this._readPrelude();
  }

  // * Initialization of component. This includes the second part of the handshake process:
  //   sending the first SETTINGS frame. This is done by the connection class right after
  //   initialization.
  this._initializeDataFlow(role, settings, filters || {});

  // * Initialization of management code.
  this._initializeManagement();

  // * Initializing error handling.
  this._initializeErrorHandling();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.request"></a>[function <span class="apidocSignatureSpan">http2.</span>request (options, callback)](#apidoc.element.http2.request)
- description and source-code
```javascript
function requestTLS(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = false;
  if (options.protocol && options.protocol !== "https:") {
    throw new Error('This interface only supports https-schemed URLs');
  }
  if (options.agent && typeof(options.agent.request) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.request(agentOptions, callback);
  }
  return exports.globalAgent.request(options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.Agent"></a>[module http2.Agent](#apidoc.module.http2.Agent)

#### <a name="apidoc.element.http2.Agent.Agent"></a>[function <span class="apidocSignatureSpan">http2.</span>Agent (options)](#apidoc.element.http2.Agent.Agent)
- description and source-code
```javascript
function Agent(options) {
  EventEmitter.call(this);
  this.setMaxListeners(0);

  options = util._extend({}, options);

  this._settings = options.settings;
  this._log = (options.log || defaultLogger).child({ component: 'http' });
  this.endpoints = {};

  // * Using an own HTTPS agent, because the global agent does not look at 'NPN/ALPNProtocols' when
  //   generating the key identifying the connection, so we may get useless non-negotiated TLS
  //   channels even if we ask for a negotiated one. This agent will contain only negotiated
  //   channels.
  options.ALPNProtocols = supportedProtocols;
  options.NPNProtocols = supportedProtocols;
  this._httpsAgent = new https.Agent(options);

  this.sockets = this._httpsAgent.sockets;
  this.requests = this._httpsAgent.requests;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.Agent.prototype"></a>[module http2.Agent.prototype](#apidoc.module.http2.Agent.prototype)

#### <a name="apidoc.element.http2.Agent.prototype.destroy"></a>[function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>destroy (error)](#apidoc.element.http2.Agent.prototype.destroy)
- description and source-code
```javascript
destroy = function (error) {
  if (this._httpsAgent) {
    this._httpsAgent.destroy();
  }
  for (var key in this.endpoints) {
    this.endpoints[key].close(error);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Agent.prototype.get"></a>[function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>get (options, callback)](#apidoc.element.http2.Agent.prototype.get)
- description and source-code
```javascript
function get(options, callback) {
  var request = this.request(options, callback);
  request.end();
  return request;
}
```
- example usage
```shell
...
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
  response.pipe(process.stdout);
});
'''

### Simple static file server ###

An simple static file server serving up content from its own directory is available in the 'example'
...
```

#### <a name="apidoc.element.http2.Agent.prototype.request"></a>[function <span class="apidocSignatureSpan">http2.Agent.prototype.</span>request (options, callback)](#apidoc.element.http2.Agent.prototype.request)
- description and source-code
```javascript
function request(options, callback) {
  if (typeof options === 'string') {
    options = url.parse(options);
  } else {
    options = util._extend({}, options);
  }

  options.method = (options.method || 'GET').toUpperCase();
  options.protocol = options.protocol || 'https:';
  options.host = options.hostname || options.host || 'localhost';
  options.port = options.port || 443;
  options.path = options.path || '/';

  if (!options.plain && options.protocol === 'http:') {
    this._log.error('Trying to negotiate client request with Upgrade from HTTP/1.1');
    this.emit('error', new Error('HTTP1.1 -> HTTP2 upgrade is not yet supported.'));
  }

  var request = new OutgoingRequest(this._log);

  if (callback) {
    request.on('response', callback);
  }

  var key = [
    !!options.plain,
    options.host,
    options.port
  ].join(':');
  var self = this;

  // * There's an existing HTTP/2 connection to this host
  if (key in this.endpoints) {
    var endpoint = this.endpoints[key];
    request._start(endpoint.createStream(), options);
  }

  // * HTTP/2 over plain TCP
  else if (options.plain) {
    endpoint = new Endpoint(this._log, 'CLIENT', this._settings);
    endpoint.socket = net.connect({
      host: options.host,
      port: options.port,
      localAddress: options.localAddress
    });

    endpoint.socket.on('error', function (error) {
      self._log.error('Socket error: ' + error.toString());
      request.emit('error', error);
    });

    endpoint.on('error', function(error){
      self._log.error('Connection error: ' + error.toString());
      request.emit('error', error);
    });

    this.endpoints[key] = endpoint;
    endpoint.pipe(endpoint.socket).pipe(endpoint);
    request._start(endpoint.createStream(), options);
  }

  // * HTTP/2 over TLS negotiated using NPN or ALPN, or fallback to HTTPS1
  else {
    var started = false;
    var createAgent = hasAgentOptions(options);
    options.ALPNProtocols = supportedProtocols;
    options.NPNProtocols = supportedProtocols;
    options.servername = options.host; // Server Name Indication
    options.ciphers = options.ciphers || cipherSuites;
    if (createAgent) {
      options.agent = new https.Agent(options);
    } else if (options.agent == null) {
      options.agent = this._httpsAgent;
    }
    var httpsRequest = https.request(options);

    httpsRequest.on('error', function (error) {
      self._log.error('Socket error: ' + error.toString());
      self.removeAllListeners(key);
      request.emit('error', error);
    });

    httpsRequest.on('socket', function(socket) {
      var negotiatedProtocol = socket.alpnProtocol || socket.npnProtocol;
      if (negotiatedProtocol != null) { // null in >=0.11.0, undefined in <0.11.0
        negotiated();
      } else {
        socket.on('secureConnect', negotiated);
      }
    });

    function negotiated() {
      var endpoint;
      var negotiatedProtocol = httpsRequest.socket.alpnProtocol || httpsRequest.socket.npnProtocol;
      if (negotiatedProtocol === protocol.VERSION) {
        httpsRequest.socket.emit('agentRemove');
        unbundleSocket(httpsRequest.socket);
        endpoint = new Endpoint(self._log, 'CLIENT', self._settings);
        endpoint.socket = httpsRequest.socket;
        endpoint.pipe(endpoint.socket).pipe(endpoint);
      }
      if (started) {
        // ** In the meantime, an other connection was made to the same host...
        if (endpoint) {
          // *** and it turned out to be HTTP2 and the request was multiplexed on that one, so we should close this one
          endpoint.close();
        }
        // *** otherwise, the fallback to HTTPS1 is already done.
      } else {
        if (endpoint) {
          self._log.info({ e: endpoint, server: options.host + ':' + options.port },
                         'New outgoing HTTP/2 connection');
          self.endpoints[key] = endpoint;
          self.emit(key, endpoint);
        } else {
          self.emit(key, undefined);
        }
      }
    }

    this.once(key, function(endpoint) {
      started = true;
      if (endpoint) { ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.ClientRequest"></a>[module http2.ClientRequest](#apidoc.module.http2.ClientRequest)

#### <a name="apidoc.element.http2.ClientRequest.ClientRequest"></a>[function <span class="apidocSignatureSpan">http2.</span>ClientRequest ()](#apidoc.element.http2.ClientRequest.ClientRequest)
- description and source-code
```javascript
function OutgoingRequest() {
  OutgoingMessage.call(this);

  this._log = undefined;

  this.stream = undefined;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.ClientRequest.prototype"></a>[module http2.ClientRequest.prototype](#apidoc.module.http2.ClientRequest.prototype)

#### <a name="apidoc.element.http2.ClientRequest.prototype._fallback"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_fallback (request)](#apidoc.element.http2.ClientRequest.prototype._fallback)
- description and source-code
```javascript
function _fallback(request) {
  request.on('response', this.emit.bind(this, 'response'));
  this.stream = this.request = request;
  this.emit('socket', this.socket);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype._onPromise"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_onPromise (stream, headers)](#apidoc.element.http2.ClientRequest.prototype._onPromise)
- description and source-code
```javascript
function _onPromise(stream, headers) {
  this._log.info({ push_stream: stream.id }, 'Receiving push promise');

  var promise = new IncomingPromise(stream, headers);

  if (this.listeners('push').length > 0) {
    this.emit('push', promise);
  } else {
    promise.cancel();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype._start"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>_start (stream, options)](#apidoc.element.http2.ClientRequest.prototype._start)
- description and source-code
```javascript
function _start(stream, options) {
  this.stream = stream;
  this.options = options;

  this._log = stream._log.child({ component: 'http' });

  for (var key in options.headers) {
    this.setHeader(key, options.headers[key]);
  }
  var headers = this._headers;
  delete headers.host;

  if (options.auth) {
    headers.authorization = 'Basic ' + new Buffer(options.auth).toString('base64');
  }

  headers[':scheme'] = options.protocol.slice(0, -1);
  headers[':method'] = options.method;
  headers[':authority'] = options.host;
  headers[':path'] = options.path;

  this._log.info({ scheme: headers[':scheme'], method: headers[':method'],
                   authority: headers[':authority'], path: headers[':path'],
                   headers: (options.headers || {}) }, 'Sending request');
  this.stream.headers(headers);
  this.headersSent = true;

  this.emit('socket', this.stream);
  var response = new IncomingResponse(this.stream);
  response.req = this;
  response.once('ready', this.emit.bind(this, 'response', response));

  this.stream.on('promise', this._onPromise.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.abort"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>abort ()](#apidoc.element.http2.ClientRequest.prototype.abort)
- description and source-code
```javascript
function abort() {
  if (this.request) {
    this.request.abort();
  } else if (this.stream) {
    this.stream.reset('CANCEL');
  } else {
    this.on('socket', this.abort.bind(this));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.on"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>on (event, listener)](#apidoc.element.http2.ClientRequest.prototype.on)
- description and source-code
```javascript
function on(event, listener) {
  if (this.request && (event === 'upgrade')) {
    this.request.on(event, listener && listener.bind(this));
  } else {
    OutgoingMessage.prototype.on.call(this, event, listener);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.setNoDelay"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setNoDelay (noDelay)](#apidoc.element.http2.ClientRequest.prototype.setNoDelay)
- description and source-code
```javascript
function setNoDelay(noDelay) {
  if (this.request) {
    this.request.setNoDelay(noDelay);
  } else if (!this.stream) {
    this.on('socket', this.setNoDelay.bind(this, noDelay));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.setPriority"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setPriority (priority)](#apidoc.element.http2.ClientRequest.prototype.setPriority)
- description and source-code
```javascript
function setPriority(priority) {
  if (this.stream) {
    this.stream.priority(priority);
  } else {
    this.once('socket', this.setPriority.bind(this, priority));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.setSocketKeepAlive"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setSocketKeepAlive (enable, initialDelay)](#apidoc.element.http2.ClientRequest.prototype.setSocketKeepAlive)
- description and source-code
```javascript
function setSocketKeepAlive(enable, initialDelay) {
  if (this.request) {
    this.request.setSocketKeepAlive(enable, initialDelay);
  } else if (!this.stream) {
    this.on('socket', this.setSocketKeepAlive.bind(this, enable, initialDelay));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.ClientRequest.prototype.setTimeout"></a>[function <span class="apidocSignatureSpan">http2.ClientRequest.prototype.</span>setTimeout (timeout, callback)](#apidoc.element.http2.ClientRequest.prototype.setTimeout)
- description and source-code
```javascript
function setTimeout(timeout, callback) {
  if (this.request) {
    this.request.setTimeout(timeout, callback);
  } else if (!this.stream) {
    this.on('socket', this.setTimeout.bind(this, timeout, callback));
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingMessage"></a>[module http2.IncomingMessage](#apidoc.module.http2.IncomingMessage)

#### <a name="apidoc.element.http2.IncomingMessage.IncomingMessage"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingMessage (stream)](#apidoc.element.http2.IncomingMessage.IncomingMessage)
- description and source-code
```javascript
function IncomingMessage(stream) {
  // * This is basically a read-only wrapper for the [Stream](protocol/stream.html) class.
  PassThrough.call(this);
  stream.pipe(this);
  this.socket = this.stream = stream;

  this._log = stream._log.child({ component: 'http' });

  // * HTTP/2.0 does not define a way to carry the version identifier that is included in the
  //   HTTP/1.1 request/status line. Version is always 2.0.
  this.httpVersion = '2.0';
  this.httpVersionMajor = 2;
  this.httpVersionMinor = 0;

  // * 'this.headers' will store the regular headers (and none of the special colon headers)
  this.headers = {};
  this.trailers = undefined;
  this._lastHeadersSeen = undefined;

  // * Other metadata is filled in when the headers arrive.
  stream.once('headers', this._onHeaders.bind(this));
  stream.once('end', this._onEnd.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingMessage.prototype"></a>[module http2.IncomingMessage.prototype](#apidoc.module.http2.IncomingMessage.prototype)

#### <a name="apidoc.element.http2.IncomingMessage.prototype._checkSpecialHeader"></a>[function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_checkSpecialHeader (key, value)](#apidoc.element.http2.IncomingMessage.prototype._checkSpecialHeader)
- description and source-code
```javascript
function _checkSpecialHeader(key, value) {
  if ((typeof value !== 'string') || (value.length === 0)) {
    this._log.error({ key: key, value: value }, 'Invalid or missing special header field');
    this.stream.reset('PROTOCOL_ERROR');
  }

  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingMessage.prototype._onEnd"></a>[function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_onEnd ()](#apidoc.element.http2.IncomingMessage.prototype._onEnd)
- description and source-code
```javascript
function _onEnd() {
  this.trailers = this._lastHeadersSeen;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingMessage.prototype._onHeaders"></a>[function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingMessage.prototype._onHeaders)
- description and source-code
```javascript
function _onHeaders(headers) {
  // * Detects malformed headers
  this._validateHeaders(headers);

  // * Store the _regular_ headers in 'this.headers'
  for (var name in headers) {
    if (name[0] !== ':') {
      if (name === 'set-cookie' && !Array.isArray(headers[name])) {
        this.headers[name] = [headers[name]];
      } else {
        this.headers[name] = headers[name];
      }
    }
  }

  // * The last header block, if it's not the first, will represent the trailers
  var self = this;
  this.stream.on('headers', function(headers) {
    self._lastHeadersSeen = headers;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingMessage.prototype._validateHeaders"></a>[function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>_validateHeaders (headers)](#apidoc.element.http2.IncomingMessage.prototype._validateHeaders)
- description and source-code
```javascript
function _validateHeaders(headers) {
  // * An HTTP/2.0 request or response MUST NOT include any of the following header fields:
  //   Connection, Host, Keep-Alive, Proxy-Connection, Transfer-Encoding, and Upgrade. A server
  //   MUST treat the presence of any of these header fields as a stream error of type
  //   PROTOCOL_ERROR.
  //  If the TE header is present, it's only valid value is 'trailers'
  for (var i = 0; i < deprecatedHeaders.length; i++) {
    var key = deprecatedHeaders[i];
    if (key in headers || (key === 'te' && headers[key] !== 'trailers')) {
      this._log.error({ key: key, value: headers[key] }, 'Deprecated header found');
      this.stream.reset('PROTOCOL_ERROR');
      return;
    }
  }

  for (var headerName in headers) {
    // * Empty header name field is malformed
    if (headerName.length <= 1) {
      this.stream.reset('PROTOCOL_ERROR');
      return;
    }
    // * A request or response containing uppercase header name field names MUST be
    //   treated as malformed (Section 8.1.3.5). Implementations that detect malformed
    //   requests or responses need to ensure that the stream ends.
    if(/[A-Z]/.test(headerName)) {
      this.stream.reset('PROTOCOL_ERROR');
      return;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.IncomingMessage.prototype.setTimeout"></a>[function <span class="apidocSignatureSpan">http2.IncomingMessage.prototype.</span>setTimeout ()](#apidoc.element.http2.IncomingMessage.prototype.setTimeout)
- description and source-code
```javascript
function noop() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingRequest"></a>[module http2.IncomingRequest](#apidoc.module.http2.IncomingRequest)

#### <a name="apidoc.element.http2.IncomingRequest.IncomingRequest"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingRequest (stream)](#apidoc.element.http2.IncomingRequest.IncomingRequest)
- description and source-code
```javascript
function IncomingRequest(stream) {
  IncomingMessage.call(this, stream);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingRequest.prototype"></a>[module http2.IncomingRequest.prototype](#apidoc.module.http2.IncomingRequest.prototype)

#### <a name="apidoc.element.http2.IncomingRequest.prototype._onHeaders"></a>[function <span class="apidocSignatureSpan">http2.IncomingRequest.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingRequest.prototype._onHeaders)
- description and source-code
```javascript
function _onHeaders(headers) {
  // * The ":method" header field includes the HTTP method
  // * The ":scheme" header field includes the scheme portion of the target URI
  // * The ":authority" header field includes the authority portion of the target URI
  // * The ":path" header field includes the path and query parts of the target URI.
  //   This field MUST NOT be empty; URIs that do not contain a path component MUST include a value
  //   of '/', unless the request is an OPTIONS request for '*', in which case the ":path" header
  //   field MUST include '*'.
  // * All HTTP/2.0 requests MUST include exactly one valid value for all of these header fields. A
  //   server MUST treat the absence of any of these header fields, presence of multiple values, or
  //   an invalid value as a stream error of type PROTOCOL_ERROR.
  this.method = this._checkSpecialHeader(':method'   , headers[':method']);
  this.scheme = this._checkSpecialHeader(':scheme'   , headers[':scheme']);
  this.host   = this._checkSpecialHeader(':authority', headers[':authority']  );
  this.url    = this._checkSpecialHeader(':path'     , headers[':path']  );
  if (!this.method || !this.scheme || !this.host || !this.url) {
    // This is invalid, and we've sent a RST_STREAM, so don't continue processing
    return;
  }

  // * Host header is included in the headers object for backwards compatibility.
  this.headers.host = this.host;

  // * Handling regular headers.
  IncomingMessage.prototype._onHeaders.call(this, headers);

  // * Signaling that the headers arrived.
  this._log.info({ method: this.method, scheme: this.scheme, host: this.host,
                   path: this.url, headers: this.headers }, 'Incoming request');
  this.emit('ready');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingResponse"></a>[module http2.IncomingResponse](#apidoc.module.http2.IncomingResponse)

#### <a name="apidoc.element.http2.IncomingResponse.IncomingResponse"></a>[function <span class="apidocSignatureSpan">http2.</span>IncomingResponse (stream)](#apidoc.element.http2.IncomingResponse.IncomingResponse)
- description and source-code
```javascript
function IncomingResponse(stream) {
  IncomingMessage.call(this, stream);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.IncomingResponse.prototype"></a>[module http2.IncomingResponse.prototype](#apidoc.module.http2.IncomingResponse.prototype)

#### <a name="apidoc.element.http2.IncomingResponse.prototype._onHeaders"></a>[function <span class="apidocSignatureSpan">http2.IncomingResponse.prototype.</span>_onHeaders (headers)](#apidoc.element.http2.IncomingResponse.prototype._onHeaders)
- description and source-code
```javascript
function _onHeaders(headers) {
  // * A single ":status" header field is defined that carries the HTTP status code field. This
  //   header field MUST be included in all responses.
  // * A client MUST treat the absence of the ":status" header field, the presence of multiple
  //   values, or an invalid value as a stream error of type PROTOCOL_ERROR.
  //   Note: currently, we do not enforce it strictly: we accept any format, and parse it as int
  // * HTTP/2.0 does not define a way to carry the reason phrase that is included in an HTTP/1.1
  //   status line.
  this.statusCode = parseInt(this._checkSpecialHeader(':status', headers[':status']));

  // * Handling regular headers.
  IncomingMessage.prototype._onHeaders.call(this, headers);

  // * Signaling that the headers arrived.
  this._log.info({ status: this.statusCode, headers: this.headers}, 'Incoming response');
  this.emit('ready');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.OutgoingMessage"></a>[module http2.OutgoingMessage](#apidoc.module.http2.OutgoingMessage)

#### <a name="apidoc.element.http2.OutgoingMessage.OutgoingMessage"></a>[function <span class="apidocSignatureSpan">http2.</span>OutgoingMessage ()](#apidoc.element.http2.OutgoingMessage.OutgoingMessage)
- description and source-code
```javascript
function OutgoingMessage() {
  // * This is basically a read-only wrapper for the [Stream](protocol/stream.html) class.
  Writable.call(this);

  this._headers = {};
  this._trailers = undefined;
  this.headersSent = false;
  this.finished = false;

  this.on('finish', this._finish);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.OutgoingMessage.prototype"></a>[module http2.OutgoingMessage.prototype](#apidoc.module.http2.OutgoingMessage.prototype)

#### <a name="apidoc.element.http2.OutgoingMessage.prototype._checkSpecialHeader"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_checkSpecialHeader (key, value)](#apidoc.element.http2.OutgoingMessage.prototype._checkSpecialHeader)
- description and source-code
```javascript
function _checkSpecialHeader(key, value) {
  if ((typeof value !== 'string') || (value.length === 0)) {
    this._log.error({ key: key, value: value }, 'Invalid or missing special header field');
    this.stream.reset('PROTOCOL_ERROR');
  }

  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype._finish"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_finish ()](#apidoc.element.http2.OutgoingMessage.prototype._finish)
- description and source-code
```javascript
function _finish() {
  if (this.stream) {
    if (this._trailers) {
      if (this.request) {
        this.request.addTrailers(this._trailers);
      } else {
        this.stream.headers(this._trailers);
      }
    }
    this.finished = true;
    this.stream.end();
  } else {
    this.once('socket', this._finish.bind(this));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype._write"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>_write (chunk, encoding, callback)](#apidoc.element.http2.OutgoingMessage.prototype._write)
- description and source-code
```javascript
function _write(chunk, encoding, callback) {
  if (this.stream) {
    this.stream.write(chunk, encoding, callback);
  } else {
    this.once('socket', this._write.bind(this, chunk, encoding, callback));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype.addTrailers"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>addTrailers (trailers)](#apidoc.element.http2.OutgoingMessage.prototype.addTrailers)
- description and source-code
```javascript
function addTrailers(trailers) {
  this._trailers = trailers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype.getHeader"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>getHeader (name)](#apidoc.element.http2.OutgoingMessage.prototype.getHeader)
- description and source-code
```javascript
function getHeader(name) {
  return this._headers[name.toLowerCase()];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype.removeHeader"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>removeHeader (name)](#apidoc.element.http2.OutgoingMessage.prototype.removeHeader)
- description and source-code
```javascript
function removeHeader(name) {
  if (this.headersSent) {
    return this.emit('error', new Error('Can\'t remove headers after they are sent.'));
  } else {
    delete this._headers[name.toLowerCase()];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype.setHeader"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>setHeader (name, value)](#apidoc.element.http2.OutgoingMessage.prototype.setHeader)
- description and source-code
```javascript
function setHeader(name, value) {
  if (this.headersSent) {
    return this.emit('error', new Error('Can\'t set headers after they are sent.'));
  } else {
    name = name.toLowerCase();
    if (deprecatedHeaders.indexOf(name) !== -1) {
      return this.emit('error', new Error('Cannot set deprecated header: ' + name));
    }
    this._headers[name] = value;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingMessage.prototype.setTimeout"></a>[function <span class="apidocSignatureSpan">http2.OutgoingMessage.prototype.</span>setTimeout ()](#apidoc.element.http2.OutgoingMessage.prototype.setTimeout)
- description and source-code
```javascript
function noop() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.OutgoingResponse"></a>[module http2.OutgoingResponse](#apidoc.module.http2.OutgoingResponse)

#### <a name="apidoc.element.http2.OutgoingResponse.OutgoingResponse"></a>[function <span class="apidocSignatureSpan">http2.</span>OutgoingResponse (stream)](#apidoc.element.http2.OutgoingResponse.OutgoingResponse)
- description and source-code
```javascript
function OutgoingResponse(stream) {
  OutgoingMessage.call(this);

  this._log = stream._log.child({ component: 'http' });

  this.stream = stream;
  this.statusCode = 200;
  this.sendDate = true;

  this.stream.once('headers', this._onRequestHeaders.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.OutgoingResponse.prototype"></a>[module http2.OutgoingResponse.prototype](#apidoc.module.http2.OutgoingResponse.prototype)

#### <a name="apidoc.element.http2.OutgoingResponse.prototype._implicitHeader"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_implicitHeader ()](#apidoc.element.http2.OutgoingResponse.prototype._implicitHeader)
- description and source-code
```javascript
_implicitHeader = function () {
  this._implicitHeaders();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype._implicitHeaders"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_implicitHeaders ()](#apidoc.element.http2.OutgoingResponse.prototype._implicitHeaders)
- description and source-code
```javascript
function _implicitHeaders() {
  if (!this.headersSent) {
    this.writeHead(this.statusCode);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype._onRequestHeaders"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>_onRequestHeaders (headers)](#apidoc.element.http2.OutgoingResponse.prototype._onRequestHeaders)
- description and source-code
```javascript
function _onRequestHeaders(headers) {
  this._requestHeaders = headers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.altsvc"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>altsvc (host, port, protocolID, maxAge, origin)](#apidoc.element.http2.OutgoingResponse.prototype.altsvc)
- description and source-code
```javascript
function altsvc(host, port, protocolID, maxAge, origin) {
    if (origin === undefined) {
        origin = "";
    }
    this.stream.altsvc(host, port, protocolID, maxAge, origin);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.end"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>end ()](#apidoc.element.http2.OutgoingResponse.prototype.end)
- description and source-code
```javascript
function end() {
  this.finshed = true;
  this._implicitHeaders();
  return OutgoingMessage.prototype.end.apply(this, arguments);
}
```
- example usage
```shell
...
'''javascript
var options = {
  key: fs.readFileSync('./example/localhost.key'),
  cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
...
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.on"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>on (event, listener)](#apidoc.element.http2.OutgoingResponse.prototype.on)
- description and source-code
```javascript
function on(event, listener) {
  if (this.request && (event === 'timeout')) {
    this.request.on(event, listener && listener.bind(this));
  } else {
    OutgoingMessage.prototype.on.call(this, event, listener);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.push"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>push (options)](#apidoc.element.http2.OutgoingResponse.prototype.push)
- description and source-code
```javascript
function push(options) {
  if (typeof options === 'string') {
    options = url.parse(options);
  }

  if (!options.path) {
    throw new Error(''path' option is mandatory.');
  }

  var promise = util._extend({
    ':method': (options.method || 'GET').toUpperCase(),
    ':scheme': (options.protocol && options.protocol.slice(0, -1)) || this._requestHeaders[':scheme'],
    ':authority': options.hostname || options.host || this._requestHeaders[':authority'],
    ':path': options.path
  }, options.headers);

  this._log.info({ method: promise[':method'], scheme: promise[':scheme'],
                   authority: promise[':authority'], path: promise[':path'],
                   headers: options.headers }, 'Promising push stream');

  var pushStream = this.stream.promise(promise);

  return new OutgoingResponse(pushStream);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.write"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>write ()](#apidoc.element.http2.OutgoingResponse.prototype.write)
- description and source-code
```javascript
function write() {
  this._implicitHeaders();
  return OutgoingMessage.prototype.write.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.OutgoingResponse.prototype.writeHead"></a>[function <span class="apidocSignatureSpan">http2.OutgoingResponse.prototype.</span>writeHead (statusCode, reasonPhrase, headers)](#apidoc.element.http2.OutgoingResponse.prototype.writeHead)
- description and source-code
```javascript
function writeHead(statusCode, reasonPhrase, headers) {
  if (this.headersSent) {
    return;
  }

  if (typeof reasonPhrase === 'string') {
    this._log.warn('Reason phrase argument was present but ignored by the writeHead method');
  } else {
    headers = reasonPhrase;
  }

  for (var name in headers) {
    this.setHeader(name, headers[name]);
  }
  headers = this._headers;

  if (this.sendDate && !('date' in this._headers)) {
    headers.date = (new Date()).toUTCString();
  }

  this._log.info({ status: statusCode, headers: this._headers }, 'Sending server response');

  headers[':status'] = this.statusCode = statusCode;

  this.stream.headers(headers);
  this.headersSent = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.Server"></a>[module http2.Server](#apidoc.module.http2.Server)

#### <a name="apidoc.element.http2.Server.Server"></a>[function <span class="apidocSignatureSpan">http2.</span>Server (options)](#apidoc.element.http2.Server.Server)
- description and source-code
```javascript
function Server(options) {
  options = util._extend({}, options);

  this._log = (options.log || defaultLogger).child({ component: 'http' });
  this._settings = options.settings;

  var start = this._start.bind(this);
  var fallback = this._fallback.bind(this);

  // HTTP2 over TLS (using NPN or ALPN)
  if ((options.key && options.cert) || options.pfx) {
    this._log.info('Creating HTTP/2 server over TLS');
    this._mode = 'tls';
    options.ALPNProtocols = supportedProtocols;
    options.NPNProtocols = supportedProtocols;
    options.ciphers = options.ciphers || cipherSuites;
    options.honorCipherOrder = (options.honorCipherOrder != false);
    this._server = https.createServer(options);
    this._originalSocketListeners = this._server.listeners('secureConnection');
    this._server.removeAllListeners('secureConnection');
    this._server.on('secureConnection', function(socket) {
      var negotiatedProtocol = socket.alpnProtocol || socket.npnProtocol;
      // It's true that the client MUST use SNI, but if it doesn't, we don't care, don't fall back to HTTP/1,
      // since if the ALPN negotiation is otherwise successful, the client thinks we speak HTTP/2 but we don't.
      if (negotiatedProtocol === protocol.VERSION) {
        start(socket);
      } else {
        fallback(socket);
      }
    });
    this._server.on('request', this.emit.bind(this, 'request'));

    forwardEvent('error', this._server, this);
    forwardEvent('listening', this._server, this);
  }

  // HTTP2 over plain TCP
  else if (options.plain) {
    this._log.info('Creating HTTP/2 server over plain TCP');
    this._mode = 'plain';
    this._server = net.createServer(start);
  }

  // HTTP/2 with HTTP/1.1 upgrade
  else {
    this._log.error('Trying to create HTTP/2 server with Upgrade from HTTP/1.1');
    throw new Error('HTTP1.1 -> HTTP2 upgrade is not yet supported. Please provide TLS keys.');
  }

  this._server.on('close', this.emit.bind(this, 'close'));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.Server.prototype"></a>[module http2.Server.prototype](#apidoc.module.http2.Server.prototype)

#### <a name="apidoc.element.http2.Server.prototype._fallback"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>_fallback (socket)](#apidoc.element.http2.Server.prototype._fallback)
- description and source-code
```javascript
function _fallback(socket) {
  var negotiatedProtocol = socket.alpnProtocol || socket.npnProtocol;

  this._log.info({ client: socket.remoteAddress + ':' + socket.remotePort,
                   protocol: negotiatedProtocol,
                   SNI: socket.servername
                 }, 'Falling back to simple HTTPS');

  for (var i = 0; i < this._originalSocketListeners.length; i++) {
    this._originalSocketListeners[i].call(this._server, socket);
  }

  this.emit('connection', socket);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype._start"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>_start (socket)](#apidoc.element.http2.Server.prototype._start)
- description and source-code
```javascript
function _start(socket) {
  var endpoint = new Endpoint(this._log, 'SERVER', this._settings);

  this._log.info({ e: endpoint,
                   client: socket.remoteAddress + ':' + socket.remotePort,
                   SNI: socket.servername
                 }, 'New incoming HTTP/2 connection');

  endpoint.pipe(socket).pipe(endpoint);

  var self = this;
  endpoint.on('stream', function _onStream(stream) {
    var response = new OutgoingResponse(stream);
    var request = new IncomingRequest(stream);

    // Some conformance to Node.js Https specs allows to distinguish clients:
    request.remoteAddress = socket.remoteAddress;
    request.remotePort = socket.remotePort;
    request.connection = request.socket = response.socket = socket;

    request.once('ready', self.emit.bind(self, 'request', request, response));
  });

  endpoint.on('error', this.emit.bind(this, 'clientError'));
  socket.on('error', this.emit.bind(this, 'clientError'));

  this.emit('connection', socket, endpoint);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype.addContext"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>addContext (hostname, credentials)](#apidoc.element.http2.Server.prototype.addContext)
- description and source-code
```javascript
function addContext(hostname, credentials) {
  if (this._mode === 'tls') {
    this._server.addContext(hostname, credentials);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype.address"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>address ()](#apidoc.element.http2.Server.prototype.address)
- description and source-code
```javascript
function address() {
  return this._server.address()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype.close"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>close (callback)](#apidoc.element.http2.Server.prototype.close)
- description and source-code
```javascript
function close(callback) {
  this._log.info('Closing server');
  this._server.close(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype.listen"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>listen (port, hostname)](#apidoc.element.http2.Server.prototype.listen)
- description and source-code
```javascript
function listen(port, hostname) {
  this._log.info({ on: ((typeof hostname === 'string') ? (hostname + ':' + port) : port) },
                 'Listening for incoming connections');
  this._server.listen.apply(this._server, arguments);

  return this._server;
}
```
- example usage
```shell
...
var options = {
key: fs.readFileSync('./example/localhost.key'),
cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
response.pipe(process.stdout);
...
```

#### <a name="apidoc.element.http2.Server.prototype.on"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>on (event, listener)](#apidoc.element.http2.Server.prototype.on)
- description and source-code
```javascript
function on(event, listener) {
  if ((event === 'upgrade') || (event === 'timeout')) {
    return this._server.on(event, listener && listener.bind(this));
  } else {
    return EventEmitter.prototype.on.call(this, event, listener);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.Server.prototype.setTimeout"></a>[function <span class="apidocSignatureSpan">http2.Server.prototype.</span>setTimeout (timeout, callback)](#apidoc.element.http2.Server.prototype.setTimeout)
- description and source-code
```javascript
function setTimeout(timeout, callback) {
  if (this._mode === 'tls') {
    this._server.setTimeout(timeout, callback);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.http"></a>[module http2.http](#apidoc.module.http2.http)

#### <a name="apidoc.element.http2.http.createServer"></a>[function <span class="apidocSignatureSpan">http2.http.</span>createServer ()](#apidoc.element.http2.http.createServer)
- description and source-code
```javascript
function notImplemented() {
    throw new Error('HTTP UPGRADE is not implemented!');
}
```
- example usage
```shell
...

'''javascript
var options = {
  key: fs.readFileSync('./example/localhost.key'),
  cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
...
```

#### <a name="apidoc.element.http2.http.get"></a>[function <span class="apidocSignatureSpan">http2.http.</span>get ()](#apidoc.element.http2.http.get)
- description and source-code
```javascript
function notImplemented() {
    throw new Error('HTTP UPGRADE is not implemented!');
}
```
- example usage
```shell
...
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
  response.pipe(process.stdout);
});
'''

### Simple static file server ###

An simple static file server serving up content from its own directory is available in the 'example'
...
```

#### <a name="apidoc.element.http2.http.request"></a>[function <span class="apidocSignatureSpan">http2.http.</span>request ()](#apidoc.element.http2.http.request)
- description and source-code
```javascript
function notImplemented() {
    throw new Error('HTTP UPGRADE is not implemented!');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.https"></a>[module http2.https](#apidoc.module.http2.https)

#### <a name="apidoc.element.http2.https.createServer"></a>[function <span class="apidocSignatureSpan">http2.https.</span>createServer (options, requestListener)](#apidoc.element.http2.https.createServer)
- description and source-code
```javascript
function createServerTLS(options, requestListener) {
  if (typeof options === 'function') {
    throw new Error('options are required!');
  }
  if (!options.pfx && !(options.key && options.cert)) {
    throw new Error('options.pfx or options.key and options.cert are required!');
  }
  options.plain = false;

  var server = new Server(options);

  if (requestListener) {
    server.on('request', requestListener);
  }

  return server;
}
```
- example usage
```shell
...

'''javascript
var options = {
  key: fs.readFileSync('./example/localhost.key'),
  cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
...
```

#### <a name="apidoc.element.http2.https.get"></a>[function <span class="apidocSignatureSpan">http2.https.</span>get (options, callback)](#apidoc.element.http2.https.get)
- description and source-code
```javascript
function getTLS(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = false;
  if (options.protocol && options.protocol !== "https:") {
    throw new Error('This interface only supports https-schemed URLs');
  }
  if (options.agent && typeof(options.agent.get) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.get(agentOptions, callback);
  }
  return exports.globalAgent.get(options, callback);
}
```
- example usage
```shell
...
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
  response.pipe(process.stdout);
});
'''

### Simple static file server ###

An simple static file server serving up content from its own directory is available in the 'example'
...
```

#### <a name="apidoc.element.http2.https.request"></a>[function <span class="apidocSignatureSpan">http2.https.</span>request (options, callback)](#apidoc.element.http2.https.request)
- description and source-code
```javascript
function requestTLS(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = false;
  if (options.protocol && options.protocol !== "https:") {
    throw new Error('This interface only supports https-schemed URLs');
  }
  if (options.agent && typeof(options.agent.request) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.request(agentOptions, callback);
  }
  return exports.globalAgent.request(options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.protocol"></a>[module http2.protocol](#apidoc.module.http2.protocol)

#### <a name="apidoc.element.http2.protocol.Endpoint"></a>[function <span class="apidocSignatureSpan">http2.protocol.</span>Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint)
- description and source-code
```javascript
function Endpoint(log, role, settings, filters) {
  Duplex.call(this);

  // * Initializing logging infrastructure
  this._log = log.child({ component: 'endpoint', e: this });

  // * First part of the handshake process: sending and receiving the client connection header
  //   prelude.
  assert((role === 'CLIENT') || role === 'SERVER');
  if (role === 'CLIENT') {
    this._writePrelude();
  } else {
    this._readPrelude();
  }

  // * Initialization of component. This includes the second part of the handshake process:
  //   sending the first SETTINGS frame. This is done by the connection class right after
  //   initialization.
  this._initializeDataFlow(role, settings, filters || {});

  // * Initialization of management code.
  this._initializeManagement();

  // * Initializing error handling.
  this._initializeErrorHandling();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.protocol.Endpoint"></a>[module http2.protocol.Endpoint](#apidoc.module.http2.protocol.Endpoint)

#### <a name="apidoc.element.http2.protocol.Endpoint.Endpoint"></a>[function <span class="apidocSignatureSpan">http2.protocol.</span>Endpoint (log, role, settings, filters)](#apidoc.element.http2.protocol.Endpoint.Endpoint)
- description and source-code
```javascript
function Endpoint(log, role, settings, filters) {
  Duplex.call(this);

  // * Initializing logging infrastructure
  this._log = log.child({ component: 'endpoint', e: this });

  // * First part of the handshake process: sending and receiving the client connection header
  //   prelude.
  assert((role === 'CLIENT') || role === 'SERVER');
  if (role === 'CLIENT') {
    this._writePrelude();
  } else {
    this._readPrelude();
  }

  // * Initialization of component. This includes the second part of the handshake process:
  //   sending the first SETTINGS frame. This is done by the connection class right after
  //   initialization.
  this._initializeDataFlow(role, settings, filters || {});

  // * Initialization of management code.
  this._initializeManagement();

  // * Initializing error handling.
  this._initializeErrorHandling();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.protocol.Endpoint.prototype"></a>[module http2.protocol.Endpoint.prototype](#apidoc.module.http2.protocol.Endpoint.prototype)

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._error"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_error (component, error)](#apidoc.element.http2.protocol.Endpoint.prototype._error)
- description and source-code
```javascript
function _error(component, error) {
  this._log.fatal({ source: component, message: error }, 'Fatal error, closing connection');
  this.close(error);
  setImmediate(this.emit.bind(this, 'error', error));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._initializeDataFlow"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeDataFlow (role, settings, filters)](#apidoc.element.http2.protocol.Endpoint.prototype._initializeDataFlow)
- description and source-code
```javascript
function _initializeDataFlow(role, settings, filters) {
  var firstStreamId, compressorRole, decompressorRole;
  if (role === 'CLIENT') {
    firstStreamId = 1;
    compressorRole = 'REQUEST';
    decompressorRole = 'RESPONSE';
  } else {
    firstStreamId = 2;
    compressorRole = 'RESPONSE';
    decompressorRole = 'REQUEST';
  }

  this._serializer   = new Serializer(this._log);
  this._deserializer = new Deserializer(this._log);
  this._compressor   = new Compressor(this._log, compressorRole);
  this._decompressor = new Decompressor(this._log, decompressorRole);
  this._connection   = new Connection(this._log, firstStreamId, settings);

  pipeAndFilter(this._connection, this._compressor, filters.beforeCompression);
  pipeAndFilter(this._compressor, this._serializer, filters.beforeSerialization);
  pipeAndFilter(this._deserializer, this._decompressor, filters.afterDeserialization);
  pipeAndFilter(this._decompressor, this._connection, filters.afterDecompression);

  this._connection.on('ACKNOWLEDGED_SETTINGS_HEADER_TABLE_SIZE',
                      this._decompressor.setTableSizeLimit.bind(this._decompressor));
  this._connection.on('RECEIVING_SETTINGS_HEADER_TABLE_SIZE',
                      this._compressor.setTableSizeLimit.bind(this._compressor));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._initializeErrorHandling"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeErrorHandling ()](#apidoc.element.http2.protocol.Endpoint.prototype._initializeErrorHandling)
- description and source-code
```javascript
function _initializeErrorHandling() {
  this._serializer.on('error', this._error.bind(this, 'serializer'));
  this._deserializer.on('error', this._error.bind(this, 'deserializer'));
  this._compressor.on('error', this._error.bind(this, 'compressor'));
  this._decompressor.on('error', this._error.bind(this, 'decompressor'));
  this._connection.on('error', this._error.bind(this, 'connection'));

  this._connection.on('peerError', this.emit.bind(this, 'peerError'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._initializeManagement"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_initializeManagement ()](#apidoc.element.http2.protocol.Endpoint.prototype._initializeManagement)
- description and source-code
```javascript
function _initializeManagement() {
  this._connection.on('stream', this.emit.bind(this, 'stream'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._read"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_read ()](#apidoc.element.http2.protocol.Endpoint.prototype._read)
- description and source-code
```javascript
function _read() {
  this._readableState.sync = true;
  var moreNeeded = noread, chunk;
  while (moreNeeded && (chunk = this._serializer.read())) {
    moreNeeded = this.push(chunk);
  }
  if (moreNeeded === noread) {
    this._serializer.once('readable', this._read.bind(this));
  }
  this._readableState.sync = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._readPrelude"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_readPrelude ()](#apidoc.element.http2.protocol.Endpoint.prototype._readPrelude)
- description and source-code
```javascript
function _readPrelude() {
  // * progress in the header is tracker using a 'cursor'
  var cursor = 0;

  // * '_write' is temporarily replaced by the comparator function
  this._write = function _temporalWrite(chunk, encoding, done) {
    // * which compares the stored header with the current 'chunk' byte by byte and emits the
    //   'error' event if there's a byte that doesn't match
    var offset = cursor;
    while(cursor < CLIENT_PRELUDE.length && (cursor - offset) < chunk.length) {
      if (CLIENT_PRELUDE[cursor] !== chunk[cursor - offset]) {
        this._log.fatal({ cursor: cursor, offset: offset, chunk: chunk },
                        'Client connection header prelude does not match.');
        this._error('handshake', 'PROTOCOL_ERROR');
        return;
      }
      cursor += 1;
    }

    // * if the whole header is over, and there were no error then restore the original '_write'
    //   and call it with the remaining part of the current chunk
    if (cursor === CLIENT_PRELUDE.length) {
      this._log.debug('Successfully received the client connection header prelude.');
      delete this._write;
      chunk = chunk.slice(cursor - offset);
      this._write(chunk, encoding, done);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._write"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_write (chunk, encoding, done)](#apidoc.element.http2.protocol.Endpoint.prototype._write)
- description and source-code
```javascript
function _write(chunk, encoding, done) {
  this._deserializer.write(chunk, encoding, done);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype._writePrelude"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>_writePrelude ()](#apidoc.element.http2.protocol.Endpoint.prototype._writePrelude)
- description and source-code
```javascript
function _writePrelude() {
  this._log.debug('Sending the client connection header prelude.');
  this.push(CLIENT_PRELUDE);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype.close"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>close (error)](#apidoc.element.http2.protocol.Endpoint.prototype.close)
- description and source-code
```javascript
function close(error) {
  this._connection.close(error);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.protocol.Endpoint.prototype.createStream"></a>[function <span class="apidocSignatureSpan">http2.protocol.Endpoint.prototype.</span>createStream ()](#apidoc.element.http2.protocol.Endpoint.prototype.createStream)
- description and source-code
```javascript
function createStream() {
  return this._connection.createStream();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.raw"></a>[module http2.raw](#apidoc.module.http2.raw)

#### <a name="apidoc.element.http2.raw.createServer"></a>[function <span class="apidocSignatureSpan">http2.raw.</span>createServer (options, requestListener)](#apidoc.element.http2.raw.createServer)
- description and source-code
```javascript
function createServerRaw(options, requestListener) {
  if (typeof options === 'function') {
    requestListener = options;
    options = {};
  }

  if (options.pfx || (options.key && options.cert)) {
    throw new Error('options.pfx, options.key, and options.cert are nonsensical!');
  }

  options.plain = true;
  var server = new Server(options);

  if (requestListener) {
    server.on('request', requestListener);
  }

  return server;
}
```
- example usage
```shell
...

'''javascript
var options = {
  key: fs.readFileSync('./example/localhost.key'),
  cert: fs.readFileSync('./example/localhost.crt')
};

require('http2').createServer(options, function(request, response) {
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
...
```

#### <a name="apidoc.element.http2.raw.get"></a>[function <span class="apidocSignatureSpan">http2.raw.</span>get (options, callback)](#apidoc.element.http2.raw.get)
- description and source-code
```javascript
function getRaw(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = true;
  if (options.protocol && options.protocol !== "http:") {
    throw new Error('This interface only supports http-schemed URLs');
  }
  if (options.agent && typeof(options.agent.get) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.get(agentOptions, callback);
  }
  return exports.globalAgent.get(options, callback);
}
```
- example usage
```shell
...
  response.end('Hello world!');
}).listen(8080);
'''

### Using as a client ###

'''javascript
require('http2').get('https://localhost:8080/', function(response) {
  response.pipe(process.stdout);
});
'''

### Simple static file server ###

An simple static file server serving up content from its own directory is available in the 'example'
...
```

#### <a name="apidoc.element.http2.raw.request"></a>[function <span class="apidocSignatureSpan">http2.raw.</span>request (options, callback)](#apidoc.element.http2.raw.request)
- description and source-code
```javascript
function requestRaw(options, callback) {
  if (typeof options === "string") {
    options = url.parse(options);
  }
  options.plain = true;
  if (options.protocol && options.protocol !== "http:") {
    throw new Error('This interface only supports http-schemed URLs');
  }
  if (options.agent && typeof(options.agent.request) === 'function') {
    var agentOptions = util._extend({}, options);
    delete agentOptions.agent;
    return options.agent.request(agentOptions, callback);
  }
  return exports.globalAgent.request(options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.http2.serializers"></a>[module http2.serializers](#apidoc.module.http2.serializers)

#### <a name="apidoc.element.http2.serializers.data"></a>[function <span class="apidocSignatureSpan">http2.serializers.</span>data (data)](#apidoc.element.http2.serializers.data)
- description and source-code
```javascript
data = function (data) {
  return data.toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.serializers.e"></a>[function <span class="apidocSignatureSpan">http2.serializers.</span>e (endpoint)](#apidoc.element.http2.serializers.e)
- description and source-code
```javascript
e = function (endpoint) {
  if (!('id' in endpoint)) {
    endpoint.id = nextId;
    nextId += 1;
  }
  return endpoint.id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.serializers.frame"></a>[function <span class="apidocSignatureSpan">http2.serializers.</span>frame (frame)](#apidoc.element.http2.serializers.frame)
- description and source-code
```javascript
frame = function (frame) {
  if (!frame) {
    return null;
  }

  if ('id' in frame) {
    return frame.id;
  }

  frame.id = frameCounter;
  frameCounter += 1;

  var logEntry = { id: frame.id };
  genericAttributes.concat(typeSpecificAttributes[frame.type]).forEach(function(name) {
    logEntry[name] = frame[name];
  });

  if (frame.data instanceof Buffer) {
    if (logEntry.data.length > 50) {
      logEntry.data = frame.data.slice(0, 47).toString('hex') + '...';
    } else {
      logEntry.data = frame.data.toString('hex');
    }

    if (!('length' in logEntry)) {
      logEntry.length = frame.data.length;
    }
  }

  if (frame.promised_stream instanceof Object) {
    logEntry.promised_stream = 'stream-' + frame.promised_stream.id;
  }

  logEntry.flags = Object.keys(frame.flags || {}).filter(function(name) {
    return frame.flags[name] === true;
  });

  return logEntry;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.http2.serializers.s"></a>[function <span class="apidocSignatureSpan">http2.serializers.</span>s (stream)](#apidoc.element.http2.serializers.s)
- description and source-code
```javascript
s = function (stream) {
  if (!('_id' in stream)) {
    stream._id = nextId;
    nextId += 1;
  }
  return stream._id;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
