# PWA
Working around Progressive Web Apps

# Steps

- import sample template for ui
- build a sample manifest
- working around manifest ( manipulations and learning specifics )


# Up coming
- all manifest properties test result to find the fittest info for each one


# So far we learned

## Progressive Web Apps has three parts
- Manifest
- Service workers
- Application shell architecture

### Manifest

According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest) :
> The web app **manifest** is a simple JSON file that tells the browser about your web application and how it should behave when 'installed' on the users mobile device or desktop

According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest) :
> The web app **manifest** provides information about an application (such as its name, author, icon, and description) in a JSON text file. The manifest informs details for websites installed on the homescreen of a device, providing users with quicker access and a richer experience

#### How to use it ?

Add the following code to the Head section of your document

```
<link rel="manifest" href="/manifest.json">
```

Next step ? go a head and create a that file in that path :)

#### What are the properties of Manifest ?
* **background_color**
    
    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#background-color) :
    > The **background_color** property is used on the splash screen when the application is first launched.
    
    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#background_color) :
    > Defines the expected **background color** for the website. This value repeats what is already available in the site’s CSS, but can be used by browsers to draw the background color of a shortcut when the manifest is available before the stylesheet has loaded. This creates a smooth transition between launching the web application and loading the site's content.
    
    ```
    "background_color": "red"
    ```


* **description**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#description) :
    > Provides a general description of what the pinned website does.
    
    ```
    "description": "The app that helps you find the best food in town!"
    ```


* **dir**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#dir) :
    > Specifies the primary text direction for the name, short_name, and description members. Together with the lang member, it helps the correct display of right-to-left languages.
    
    ```
    "dir": "rtl",
    "lang": "fa",
    "short_name": "سلام!"
    ```

* **display**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#display) :
    > You can customize what browser UI is shown when your app is launched. For example, you can hide the address bar and browser chrome. Or games may want to go completely full screen.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#display) :
    > Defines the developers’ preferred display mode for the website.
    
    ```
    "display": "standalone"
    ```


* **icons**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#icons) :
    > When a user adds your site to their home screen, you can define a set of icons for the browser to use. These icons are used in places like the home screen, app launcher, task switcher, splash screen, etc.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#icons) :
    > Specifies an array of image files that can serve as application icons, depending on context. For example, they can be used to represent the web application amongst a list of other applications, or to integrate the web application with an OS's task switcher and/or system preferences.
    
    ```
    "icons": [
        {
          "src": "icon/lowres.webp",
          "sizes": "48x48",
          "type": "image/webp"
        },
        {
          "src": "icon/lowres",
          "sizes": "48x48"
        },
        {
          "src": "icon/hd_hi.ico",
          "sizes": "72x72 96x96 128x128 256x256"
        },
        {
          "src": "icon/hd_hi.svg",
          "sizes": "72x72"
        }
      ]      
    ```


* **lang**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#lang) :
    > Specifies the primary language for the values in the name and short_name members. This value is a string containing a single language tag.
    
    ```
    "lang": "en-US"
    ```


* **name**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#name) :
    > You must provide at least the short_name or name property. If both are provided, short_name is used on the user's home screen, launcher, or other places where space may be limited. name is used on the app install prompt.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#name) :
    > Provides a human-readable name for the site when displayed to the user. For example, among a list of other applications or as a label for an icon.
    
    ```
    "name": "Google Maps"
    ```


* **orientation**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#orientation) :
    > You can enforce a specific orientation, which is advantageous for apps that work in only one orientation, such as games. Use this selectively. Users prefer selecting the orientatio

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#orientation) :
    > Defines the default orientation for all the website's top level browsing contexts.
    
    ```
    "orientation": "portrait-primary"
    ```


* **prefer_related_applications**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#prefer_related_applications) :
    > Specifies a boolean value that hints for the user agent to indicate to the user that the specified native applications (see below) are recommended over the website. This should only be used if the related native apps really do offer something that the website can't.
    
    ```
    "prefer_related_applications": false
    ```


* **related_applications**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#related_applications) :
    > An array of native applications that are installable by, or accessible to, the underlying platform — for example, a native Android application obtainable through the Google Play Store. Such applications are intended to be alternatives to the website that provides similar/equivalent functionality — like the native app version of the website.
    
    ```
    "related_applications": [
      {
        "platform": "play",
        "url": "https://play.google.com/store/apps/details?id=com.example.app1",
        "id": "com.example.app1"
      }, {
        "platform": "itunes",
        "url": "https://itunes.apple.com/app/example-app1/id123456789"
      }
    ]
    ```


* **scope**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#scope) :
    > The scope defines the set of URLs that the browser considers within your app, and is used to decide when you’ve left your app, and should be bounced back out to a browser tab. The scope controls the url structure that encompasses all the entry and exit points in your web app. Your start_url must reside within the scope.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#scope) :
    > Defines the navigation scope of this website's context. This restricts what web pages can be viewed while the manifest is applied. If the user navigates outside the scope, it returns to a normal web page inside a browser tab/window.
    
    ```
    "scope": "/myapp/"
    ```


* **short_name**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#name) :
    > You must provide at least the short_name or name property. If both are provided, short_name is used on the user's home screen, launcher, or other places where space may be limited.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#short_name) :
    > Provides a short human-readable name for the application. This is intended for when there is insufficient space to display the full name of the web application, like device homescreens.
    
    ```
    "short_name": "I/O 2017"
    ```
    

* **start_url**
    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#start-url) :
    > The start_url tells the browser where your application should start when it is launched, and prevents the app from starting on whatever page the user was on when they added your app to their home screen.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#start_url) :
    > The URL that loads when a user launches the application (e.g. when added to home screen), typically the index. Note that this has to be a relative URL, relative to the manifest url.
    
    ```
    "start_url": "/pwa-examples/a2hs/index.html"
    ```


* **theme_color**

    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#theme-color) :
    > The theme_color sets the color of the tool bar, and in the task switcher.

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#theme_color) :
    > Defines the default theme color for an application. This sometimes affects how the OS displays the site (e.g., on Android's task switcher, the theme color surrounds the site).  
    
    ```
    "theme_color": "aliceblue"
    ```

