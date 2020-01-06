# Hangersteak

Node web static files server with built in compression support.

### INSTALL
```npm i hangersteak``` or ```yarn add hangersteak```

### USAGE
Vanilla NodeJS server. Will return 404 if not found, or the file using streams and correct mime type. Supports automatic 304 last modified headers.
```javascript
const http = require('http')
const hangersteak = require('hangersteak')

const server = http.createServer((req, res) => {
  // Using default options
  hangersteak(req, res)

  // With options, default values shown
  hangersteak(req, res, { dir: '', maxAge: 3600, indexFile: 'index.html' })
})

server.listen(3000)
```
MIT licensed. Enjoy!
