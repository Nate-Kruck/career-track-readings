# Class 07 Readings (Sept. 21tst)

# Using Express Routing

- Routing refers to how an app's endpoints respont to client requests.

  - Example
    1. app.get(handles GET requests)
    1. app.post(handles POST requests)
    1. app.all(handles all HTTP methods)
    1. app.use(specifiy middleware as the callback)

### Route Methods

- Derived from one of the HTTP methods, and is attached to an instance of the express class.

```js
// GET method route
app.get("/", function (req, res) {
  res.send("GET request to the homepage");
});

// POST method route
app.post("/", function (req, res) {
  res.send("POST request to the homepage");
});
```

### Route Paths

- If you need to use the dollar character ($) in a path string, enclose it escaped within ([ and ]). For example, the path string for requests at “/data/$book”, would be “/data/([\$])book”.

### Route Parameters

- Route parameters are named URL segments that are used to capture the values specified at their position in the URL.

---

# SuperTest

- install with command:

  ```md
  npm install supertest --save-dev
  ```

- You may use any superagent methods, including .write(), .pipe() etc and perform assertions in the .end() callback for lower-level needs.

- .expect(status[, fn])

  Assert response status code.

- .expect(status, body[, fn])

  Assert response status code and body.

- .expect(body[, fn])

  Assert response body text with a string, regular expression, or parsed body object.

- .expect(field, value[, fn])

  Assert header field value with a string or regular expression.

- .expect(function(res) {})

  Pass a custom assertion function. It'll be given the response object to check. If the check fails, throw an error.

# Using Express Middleware

- Express is a routing and middleware web framework that has minimal functionality of its own.

- Middleware functions are functions that have access to the request object(req), the response object(res) and the next middleware function in the applications request-response cycle. The next middleware function is commonly denoted by a variable named text.

- Middle ware functions can execute code, make changes to the req/res objects, end the req/res cycle and call the next middleware function in the stack.

- If the current middleware function does not end the req/res cycle, it must call next() to pass control to the next middleware function. Else it will be left hanging.

# Express Middleware

```
//This function call is very important. It tells that more processing is
//required for the current request and is in the next middleware

function/route handler.
next();
```

# Express Middleware List

<table>
    <thead>
        <tr>
            <th>Middleware module</th>
            <th>Description</th>
            <th>Replaces built-in function (Express 3)</th>
        </tr>
    </thead>
<tbody>
        <tr>
            <td><a href="/resources/middleware/body-parser.html">body-parser</a></td>
            <td>Parse HTTP request body. See also: <a href="https://github.com/raynos/body">body</a>, <a href="https://github.com/visionmedia/co-body">co-body</a>, and <a href="https://github.com/stream-utils/raw-body">raw-body</a>.</td>
            <td>express.bodyParser</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/compression.html">compression</a></td>
            <td>Compress HTTP responses.</td>
            <td>express.compress</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/connect-rid.html">connect-rid</a></td>
            <td>Generate unique request ID.</td>
            <td>NA</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/cookie-parser.html">cookie-parser</a></td>
            <td>Parse cookie header and populate <code>req.cookies</code>. See also <a href="https://github.com/jed/cookies">cookies</a> and <a href="https://github.com/jed/keygrip">keygrip</a>.</td>
            <td>express.cookieParser</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/cookie-session.html">cookie-session</a></td>
            <td>Establish cookie-based sessions.</td>
            <td>express.cookieSession</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/cors.html">cors</a></td>
            <td>Enable cross-origin resource sharing (CORS) with various options.</td>
            <td>NA</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/csurf.html">csurf</a></td>
            <td>Protect from CSRF exploits.</td>
            <td>express.csrf</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/errorhandler.html">errorhandler</a></td>
            <td>Development error-handling/debugging.</td>
            <td>express.errorHandler</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/method-override.html">method-override</a></td>
            <td>Override HTTP methods using header.</td>
            <td>express.methodOverride</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/morgan.html">morgan</a></td>
            <td>HTTP request logger.</td>
            <td>express.logger</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/multer.html">multer</a></td>
            <td>Handle multi-part form data.</td>
            <td>express.bodyParser</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/response-time.html">response-time</a></td>
            <td>Record HTTP response time.</td>
            <td>express.responseTime</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/serve-favicon.html">serve-favicon</a></td>
            <td>Serve a favicon.</td>
            <td>express.favicon</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/serve-index.html">serve-index</a></td>
            <td>Serve directory listing for a given path.</td>
            <td>express.directory</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/serve-static.html">serve-static</a></td>
            <td>Serve static files.</td>
            <td>express.static</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/session.html">session</a></td>
            <td>Establish server-based sessions (development only).</td>
            <td>express.session</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/timeout.html">timeout</a></td>
            <td>Set a timeout period for HTTP request processing.</td>
            <td>express.timeout</td>
        </tr>
        <tr>
            <td><a href="/resources/middleware/vhost.html">vhost</a></td>
            <td>Create virtual domains.</td>
            <td>express.vhost</td>
        </tr>
    </tbody>
</table>
