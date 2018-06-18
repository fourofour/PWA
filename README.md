# PWA
Working around Progressive Web Apps

# Steps

- import sample template for ui
- build a sample manifest
- working around manifest ( manipulations and learning specifics )


# Up coming
- description
- dir
- display
- icons
- lang
- name
- orientation
- prefer_related_applications
- related_applications
- scope
- short_name
- start_url
- theme_color


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

``<link rel="manifest" href="/manifest.json">``

Next step ? go a head and create a that file in that path :)

#### What are the properties of Manifest ?
* **background_color**
    
    According to [developer.google.com](https://developers.google.com/web/fundamentals/web-app-manifest#background-color) :
    > The **background_color** property is used on the splash screen when the application is first launched.
    
    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#background_color) :
    > Defines the expected **background color** for the website. This value repeats what is already available in the site’s CSS, but can be used by browsers to draw the background color of a shortcut when the manifest is available before the stylesheet has loaded. This creates a smooth transition between launching the web application and loading the site's content.
    
    ``"background_color": "red"``


* **description**


* **dir**    


* **display**


* **icons**


* **lang**


* **name**


* **orientation**


* **prefer_related_applications**


* **related_applications**


* **scope**


* **short_name**

    According to [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/Manifest#short_name) :
    > Provides a short human-readable name for the application. This is intended for when there is insufficient space to display the full name of the web application, like device homescreens.
    
    ``"short_name": "I/O 2017"``
    

* **start_url**


* **theme_color**
