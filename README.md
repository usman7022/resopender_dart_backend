A tiny lightning fast server-side framework for dart.
## Getting Started
```dart
import 'package:responder/responder.dart';

var app = Responder();
var port = 3000;

void main() {
  app.get('/a{dynamic}/route', (req, res) {
    res.headers({
      "Content-type": "text/plain",
      "x-foo": "bar",
    });
    res.send("Hello, World! ${req.params.dynamic}");
  });
  
  app.listen(port, (iport, server) => print("Listening on $iport"));
}
```
### `.options`
### `.get(route, Function(Request, Response))`
### `.post`
### `.put`
### `.delete`
### `.head`
### `.options`
### `.patch`
## `Request`
#### `.id`
#### `.params`
#### `.headers`
#### `.hostname`
#### `.method`
#### `.url`
#### `.body`
#### `.query`
#### `.is404`
## `Response`
#### `.code`
#### `.header(name, value)`
#### `.headers(Map<Name, Value>)`
#### `.getHeaders()`
#### `.type(type)`
#### `.hasHeader(headerName)`
#### `.removeHeader(headerName)`
#### `.redirect(code, dest)`
#### `.send(data)`
#### `.sent`
#   r e s o p e n d e r _ d a r t _ b a c k e n d  
 