<h3 id='app-del'>Application::del</h3>
<h4 class='variant'>void del(const char* path, Router::Middleware* middleware);</h4>
<h4 class='variant'>void del(Router::Middleware* middleware);</h4>

Routes HTTP DELETE requests to the specified path with the specified Middleware function. If no path is specified the matching is done based on the HTTP verb.

For more information, see the [routing guide](/guide/routing.html).

##### Example
```arduino
void deleteSomething(Request &req, Response &res) {
  res.sendStatus(204);
}

app.del("/delete", &deleteSomething);
```
