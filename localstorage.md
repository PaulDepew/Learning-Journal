## What is Local Storage?


Cookies are included with every HTTP request
Cookies are naturally unencripted
Cookies are limited to about 4kb of data

What we want:
1. A lot of Storage
2. On the Client Side
3. That persis beyond page refresh
4. And isn't transmitted to the server

DOM Storage
    - A way for webpages to store named key/value pairs locally in the client browser

### Check for HTML5 Storage

```js
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```

#### You can also use Modernizr

```js 
if (Modernizr.localstorage) {
//   window.localStorage is available!
} else {
//   no native support for HTML5 storage :(
//   maybe try dojox.storage or a third-party solution
} 
```

HTML Storage is based on Key/Value pairs, you store data based on the named key, then retrieve it with the key. 
    - The data type can be any but it is stored as a string

You will need to use parseInt() and parseFloat() to coerce the strings into the data types

#### getItem() gets an item

```js 
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
```

#### setItem() sets an item

#### removeItem() removes the item

#### key() gets the total number of values in a storage area and iterates through all by index

Add an event listener to a 'storage' action

 #### SQL 

```js 
openDatabase('documents', '1.0', 'Local document storage', 5*1024*1024, function (db) {
  db.changeVersion('', '1.0', function (t) {
    t.executeSql('CREATE TABLE docids (id, name)');
  }, error);
});
```