# Browsers
---

## What exactly are browsers?

The main function of a **browser** is to present the desired web resource by retrieving it from the server and displaying it in the browser window. The resource is usually an [[Introduction to HTML|HTML]] document, but it can also be a [[PDF]] file, an image or another type of content. The location of the resource is specified by the user using a [[URI]] (*Uniform Resource Identifier*).

The way in which the browser interprets and displays [[Introduction to HTML|HTML]] files is defined in the [[Introduction to HTML|HTML]] and [[Introduction to CSS|CSS]] specifications. These specifications are adhered to by the *World Wide Web Consortium W3C*, the standardization organization for the web. For years, browsers only complied with part of the specifications and developed their own extensions. This led to serious compatibility problems for web authors. Today, most browsers more or less comply with the specifications.

Browser user interfaces have a lot in common. Common user interface elements include:

- Address bar for inserting a [[URI]]
- Back and forward buttons
- Bookmark options
- Refresh and stop buttons to refresh or stop loading current documents
- Home page button that takes you to the home page
- Strangely enough, the user interface of a browser is not defined in any formal specification. It is merely a result of best practices that have evolved over the years and through mutual imitation.

>Five popular **browsers** are currently used on desktop computers: *Chrome, Internet Explorer, Firefox, Safari and Opera*. The main browsers on mobile devices are the *Android browser, iPhone, Opera and Chrome*. All browsers, with the exception of the *Opera* browser, are based on [[WebKit]]. 


---


## The high-level-structure of a browser 

### The main components of the browser include:

1. **User interface**: This includes the address bar, the "Back" and "Next" buttons, the bookmark menu, etc. All areas of the browser display except the window in which the requested page is displayed.
2. **Browser engine**: Marshals actions between the user interface and the rendering module.
3. [[#The Rendering-Module]]: responsible for displaying requested content If the requested content is [[Introduction to HTML|HTML]], for example, the [[#The Rendering-Module|rendering module]] parses [[Introduction to HTML]] and [[Introduction to CSS|CSS]] and displays the parsed content on the screen.
4. [[Network]]: For network calls such as [[HTTP]] requests with different implementations for different platforms behind a platform-independent interface.
5. **UI back-end**: Used to draw basic widgets such as combo boxes and windows. This back-end provides a generic interface that is not platform-specific. Below this, user interface methods of the operating system are used.
6. [[Introduction to JavaScript]] **interpreter**: Used to parse and execute [[Introduction to JavaScript]] code.
7. **Data storage**: This is a persistence level. The browser must store all types of data, such as cookies, locally. Browsers also support storage mechanisms such as *localStorage, IndexedDB, WebSQL and FileSystem*.


![[Browser Components.png]]

>In browsers such as *Chrome*, multiple instances of the [[#The Rendering-Module|rendering module]] are executed: one per tab. Each tab is executed in a separate process.


---


## The User Interface

This component allows end-users to interact with all visual elements available on the web page. The visual elements include the *address bar, home button, next button,* and all other elements that fetch and display the web page requested by the end-user.


---


## The Browser Engine

It is a core component of every web browser. The **browser engine** functions as an intermediary or a bridge between the [[#The User Interface|user interface]] and the [[#The Rendering Engine|rendering engine]]. It queries and handles the [[#The Rendering Engine|rendering engine]] as per the inputs received from the [[#The User Interface|user interface]].

The performance and features of a **browser engine** can greatly impact the user experience of a web browser. A fast and efficient **browser engine** can help web pages load quickly and smoothly, while a slower or less capable engine may struggle to render complex pages or provide a smooth browsing experience.


---


## The Rendering Engine

As the name suggests, this component is responsible for rendering a specific web page requested by the user on their screen. It interprets [[Introduction to HTML|HTML]] and [[XML]] documents along with images that are styled or formatted using [[Introduction to CSS|CSS]], and a final layout is generated, which is displayed on the user interface.

**Note**: Every browser has its own unique **rendering engine**. **Rendering engines** might also differ for different browser versions. The list below mentions [[#The Browser Engine|browser engines]] used by a few common browsers:

1. Google Chrome and Opera v.15+: **Blink**
2. Internet Explorer: **Trident**
3. Mozilla Firefox: **Gecko**
4. Chrome for iOS and Safari: [[WebKit]]


---


## Networking

This component is responsible for managing network calls using standard protocols like [[HTTP]] or [[FTP]]. It also looks after security issues associated with internet connection.


---


## [[Introduction to JavaScript|JavaScript]] Interpreter

As the name suggests, it is responsible for parsing and executing the [[Introduction to JavaScript|JavaScript]] code embedded in a website. Once the interpreted results are generated, they are forwarded to the rendering engine for display on the [[#The User Interface|user interface]].


---


## UI Backend 

This component uses the [[#The User Interface|user interface]] methods of the underlying operating system. It is mainly used for drawing basic widgets (windows and combo boxes).


---


## Data Storage / Persistence

It is a persistent layer. A web browser needs to store various types of data locally, for example, [[Cookies]]. As a result, Browsers must be compatible with data storage mechanisms such as *WebSQL*, *IndexedDB*, *FileSystem* etc.





###### External Links:
---
[Funktionsweise von Browsern](https://web.dev/articles/howbrowserswork?hl=de)
[How Browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
[Understanding the Role of Rendering Engine in Browsers](https://www.browserstack.com/guide/browser-rendering-engine)

---

#Browsers #Web-Browsers #Browser-Components #Browser-Engine #Rendering-Engine #User-Interface #Networks #Networking #JavaScript #JavaScript-Interpreter #UI-Backend #HTML #CSS #WebKit #Blink #Trident #Gecko #Browser-Performance #Browser-Compatibility 