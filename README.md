# iframe-appcache

This is a fix for the appcache package to avoid having the browser add
all the URL routes it encounters to the application cache.

For example, with the current appcache package, if the user were to
navigate to URLs such as:

```
http://example.meteor.com/x6NBA7QDPtgFrTCgq
http://example.meteor.com/qBAsGkM62aMzGwtHi
http://example.meteor.com/iYfGjoGptcJLqXxMk
```

each route encountered would be added to the application cache as a
"master" entry.

This fix uses the iframe technique described in
['Fixing' the application cache with an iframe](http://labs.ft.com/2012/11/using-an-iframe-to-stop-app-cache-storing-masters/).
