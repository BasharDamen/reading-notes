# LOCAL STORAGE FOR WEB APPLICATIONS

Web storage, sometimes known as DOM storage (Document Object Model storage), provides web apps with methods and protocols for storing client-side data. Web storage supports persistent data storage, similar to cookies but with a greatly enhanced capacity and no information stored in the HTTP request header. There are two main web storage types: local storage and session storage, behaving similarly to persistent cookies and session cookies respectively. Web Storage is standardized by the World Wide Web Consortium (W3C) and WHATWG. All major browsers support it.  

![storage](https://love2dev.com/img/dm_tapeuqaeiw77-1200x630.jpg)

## Features  

Web storage differs from cookies in some key ways.  

**Purpose**  

Cookies are intended for communication with servers; they are automatically added to all requests and can be accessed by both the server and client-side. Web storage falls exclusively under the purview of client-side scripting. Web storage data is not automatically transmitted to the server in every HTTP request, and a web server can't directly write to Web storage. However, either of these effects can be achieved with explicit client-side scripts, allowing for fine-tuning the server's desired interaction.  

**Storage size**  

Cookies are restricted to 4 kilobytes. Web storage provides far greater storage capacity:
* Opera 10.50+ allows 5 MB.
* Safari 8 allows 5 MB.
* Firefox 34 allows 10 MB (formerly 5 MB per origin in 2007).
* Google Chrome allows 10 MB per origin.
* Internet Explorer allows 10 MB per storage area.  

**Local and session storage**  

Web storage offers two different storage areas—local storage and session storage—which differ in scope and lifetime. Data placed in local storage is per origin—the combination of protocol, host name, and port number as defined in the same-origin policy. The data is available to all scripts loaded from pages from the same origin that previously stored the data and persists after the browser is closed. As such, Web storage does not suffer from cookie Weak Integrity and Weak Confidentiality issues, described in RFC 6265 sections 8.5 and 8.6. Session storage is both per-origin and per-instance (per-window or per-tab) and is limited to the lifetime of the instance. Session storage is intended to allow separate instances of the same web app to run in different windows without interfering with each other, a use case that's not well supported by cookies.  

**Interface and data model**  


Web storage provides a better programmatic interface than cookies because it exposes an associative array data model where the keys and values are both strings. An additional API for accessing structured data is being considered by the W3C Web Applications Working Group.  

---

## Usage  

Browsers that support web storage have the global objects *sessionStorage* and localStorage declared at the window level. The following JavaScript code can be used on these browsers to trigger web storage behavior:  

```
// Store value on browser for duration of the session
sessionStorage.setItem('key', 'value');

// Retrieve value (gets deleted when browser is closed and re-opened) ...
alert(sessionStorage.getItem('key'));

// Store value on the browser beyond the duration of the session
localStorage.setItem('key', 'value');

// Retrieve value (persists even after closing and re-opening the browser)
alert(localStorage.getItem('key'));
```

Only strings can be stored via the Storage API. Attempting to store a different data type will result in an automatic conversion into a string in most browsers. Conversion into JSON, however, allows for effective storage of JavaScript objects.  

```
// Store an object instead of a string
localStorage.setItem('key', {name: 'value'});
alert(typeof localStorage.getItem('key')); // string

// Store an integer instead of a string
localStorage.setItem('key', 1);
alert(typeof localStorage.getItem('key')); // string

// Store an object using JSON
localStorage.setItem('key', JSON.stringify({name: 'value'}));
alert(JSON.parse(localStorage.getItem('key')).name); // value
```

## Nomenclature  

The W3C draft is titled "Web Storage". "DOM storage" has also been a commonly used name, though it is becoming less so; for example the "DOM Storage" web articles of the Mozilla and Microsoft developer sites have been replaced with "Web Storage" articles.

The "DOM" in DOM storage does not literally refer to the Document Object Model. According to the W3C, "The term DOM is used to refer to the API set made available to scripts in Web applications, and does not necessarily imply the existence of an actual Document object..."  

## Web storage management  

Storage of web storage objects is enabled by default in current versions of all supporting web browsers, with browser vendors providing ways for users to natively enable or disable web storage, or clear the web storage "cache". Similar controls over web storage are also available through 3rd party browser extensions. Each browser stores Web storage objects differently:

* Firefox saves Web storage objects in a SQLite file called webappsstore.sqlite in the user's profile folder.
* Google Chrome records Web storage data in a SQLite file in the user's profile. The subfolder containing this file is "\AppData\Local\Google\Chrome\User Data\Default\Local Storage" on Windows, and "~/Library/Application Support/Google/Chrome/Default/Local Storage" on macOS.
* Opera's Web storage is located in either "\AppData\Roaming\Opera\Opera\sessions\autosave.win" or "\AppData\Local\Opera\Opera\pstorage\" depending upon Opera's version.  

![storages](https://learninfinity.info/wp-content/uploads/2017/05/Utilizing-browser-local-storage-for-client-site-script-in-any-web-application.jpg)