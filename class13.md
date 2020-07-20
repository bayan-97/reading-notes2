# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS 

![](http://diveinto.html5doctor.com/i/aoc-p.png)

Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful.

## A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5

In the beginning, there was only Internet Explorer. Or at least, that’s what Microsoft wanted the world to think. To that end, as part of the First Great Browser Wars, Microsoft invented a great many things and included them in their browser-to-end-all-browser-wars, Internet Explorer. One of these things was called DHTML Behaviors, and one of these behaviors was called userData.

As you survey these solutions, a pattern emerges: all of them are either specific to a single browser, or reliant on a third-party 

plugin. Despite heroic efforts to paper over the differences (in dojox.storage), they all expose radically different interfaces, have 

different storage limitations, and present different user experiences. So this is the problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

## INTRODUCING HTML5 STORAGE

t’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or 

what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at 

providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.


check for HTML5 Storage

`function supports_html5_storage() {`
 ` try {`
   ` return 'localStorage' in window && window``['localStorage'] !== null;`
  `} catch (e) {`
    `return false;`
`  }`
`}`

Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

## USING HTML5 STORAGE
HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

`if (Modernizr.localstorage) {`
 ` // window.localStorage is available!`
`} else {`
 ` // no native support for HTML5 storage :(`
  `// maybe try dojox.storage or a third-party ``solution`
`}`

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll 

need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of 

this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

`if (window.addEventListener) {`
 ` window.addEventListener("storage", ``handle_storage, false);`
`} else {`
 ` window.attachEvent("onstorage", `handle_storage);`
`};`

## HTML5 STORAGE IN ACTION

*Let’s see HTML5 Storage in action. Recall the*
 *Halma game we constructed in the canvas 
 *chapter. *There’s a small problem with the **game: if you close the browser window *mid-game, you’ll lose your progress. But with 

HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.



## BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS

**While the past is littered with hacks and** **workarounds, the present condition of HTML5** 
*Storage is surprisingly rosy. A new API has* *been standardized and implemented across all* 

*major browsers, platforms, and devices. As a*
*web developer, that’s just not something you* *see every day, is it? But there is more to* *life than “5 megabytes of named key/value* *pairs,” and the future of persistent local*
*storage is… how shall I put it… well, there*
*are competing visions.*
One vision is an acronym that you probably know already: SQL. In 2007, Google launched Gears, an open source cross-browser plugin which included an embedded database based on SQLite. This early prototype later influenced the creation of the Web SQL Database specification. Web SQL Database (formerly known as “WebDB”) provides a thin wrapper around a SQL database, allowing you to do things like this from JavaScript:

actual working code in 4 browsers

`document storage', 5*1024*1024, function (db) {`
  `db.changeVersion('', '1.0', function (t) {`
   ` t.executeSql('CREATE TABLE docids (id, ``name)');`
  `}, error);`
`});`


The Indexed Database API exposes what’s called an object store. An object store shares many concepts with a SQL database. There are 

“databases” with “records,” and each record has a set number of “fields.” Each field has a specific datatype, which is defined when the database is created. You can select a subset of records, then enumerate them with a “cursor.” Changes to the object store are handled within “transactions.”

If you’ve done any SQL database programming, these terms probably sound familiar. The primary difference is that the object store 
has no structured query language. You don’t construct a statement like "SELECT * from USERS where ACTIVE = 'Y'". Instead, you use 

methods provided by the object store to open a cursor on the database named “USERS,” enumerate through the records, filter out records for inactive users, and use accessor methods to get the values of each field in the remaining records. An early walk-through of IndexedDB is a good tutorial of how IndexedDB works, giving side-by-side comparisons of IndexedDB and Web SQL Database.

At time of writing, IndexedDB has only been implemented in a beta version of Firefox 4. (By contrast, Mozilla has stated that they 

will never implement Web SQL Database.) Google has stated that they are considering IndexedDB support for Chromium and Google Chrome. And even Microsoft has said that IndexedDB “is a great solution for the web.”

So what can you, as a web developer, do with IndexedDB? At the moment, virtually nothing beyond some technology demos. A year from now? Maybe something. Check the “Further Reading” section for links to some good tutorials to get you started.