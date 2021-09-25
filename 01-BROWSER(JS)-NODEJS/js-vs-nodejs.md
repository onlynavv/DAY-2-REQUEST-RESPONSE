## Difference between Browser JS (console) and Node JS

## Browser JS

1. Javascript is used on the client side
2. In browser we most of the time interact with the DOM or other Web Platform API's, we have document object and window objects provided by the browser, window is a predefined global object that has functions and attributes that has to deal with the window that has to be rendered/drawn
3. Browser provides document object, which is alsa a global object, which helps the html file to get render
4. Browser doesn't have _'require'_ predefined. We might need to include it in our app for asynchronous file loading, moduling is not mandatory in browsers, we use _'import'_
5. _'location'_ is another browser api/predefined object that has all the information about the url which we have loaded

## Node JS

1. Nodejs is used on the server side
2. In node we dont have window object, because it doesn't have a window to render/draw anything
3. In node we dont have document object, because it has nothing to render on a page
4. In node _'require'_ object is predefined, which is used to include modules in our app, in Node everything is module, we need to keep the code inside the module
5. _'location'_ object is related to a particular url, that means it is page specific, no node doen't have this
