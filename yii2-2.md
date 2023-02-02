# Zusatzfragen zu Yii2

-   The following diagramm shows the static structure of a Yii2 application. Fill in the re-bordered boxes with the missing terms.

    [![](https://www.yiiframework.com/doc/guide/2.0/en/images/application-structure.png)](https://www.yiiframework.com/doc/guide/2.0/en/structure-overview)

    - entry scripts: they are PHP scripts that are directly accessible by end users. They are responsible for starting a request handling cycle.
    - applications: they are globally accessible objects that manage application components and coordinate them to fulfill requests.
    - application components: they are objects registered with applications and provide various services for fulfilling requests.
    - modules: they are self-contained packages that contain complete MVC by themselves. An application can be organized in terms of multiple modules.
    - filters: they represent code that need to be invoked before and after the actual handling of each request by controllers.
    - widgets: they are objects that can be embedded in views. They may contain controller logic and can be reused in different views.
---
- Based on the given code template complete the code to implement a Yii2 RESTful Web Services controller (RWSC) The RWSC should expose the country model class via RESTful actors. You are not allowed to add additional lines to the code.

    ```php
    ???
    ```

- Based on the given Yii2 configuration template snippet, replace the three placeholder in the configuration to add  module country to your Yi2 application. You are not allowed to add additional lines to the code.

    ```php
    ???
    ```

- The following source code shows  the declaration of actionAbout that should display the about page. What must be the return value?

    ```php
    ???
    ```

- A Yii2 Controller CID belongs to module MID. What is the route format for action AID?

    ```txt
    MID/CID/AID
    ```

- What is the name of the default controller of the Yi2 console application?

    ```php
    HelpController
    ```

- Which Yi2 component is used to collect information about a user request and resolve it into a route?

    ```php
    UrlManager
    ```

- You are about to create a new Yi2 module. Which public method of the module class contains the code initializing the modules properties?

    ```php
    init()
    ```

- Cross-site request forgery is also known as?
    ```txt
    Session Riding
    ODER
    One-Click-Attack
    ```