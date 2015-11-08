3. Software Architecture
===================

Software Architecture is important to define and construct a solution for needed features and what the system needs to behave on a certain way. Usually, software engineerings do that answer the questions: "What we want to do?" and "How we want to do that?". And, normally, they find an architecture that adapts to the product.

So, they define how the system will be divide in modules and how they will connect with each other, and with other frameworks or even hardware. But to have and efficient architecture designed they have to get in mind some concepts as security, safety, perfomance, maintainability, availability and portability.

The model used to find what they want to know about the architecture system is the 4+1 model, that corporates logical view, implementation view, deployment view, process view and use case view that relates the other 4.

##3.1. Logical View

The **Logical View** represents all key abstractions (objects or object classes) in the system; or their packages. The main functions of this type of view are describe the organization of elements and diagrams into sections and their funcionalities, divide the software in different layers to shows it architecture and also represents the communication channels between layers.

The logical section of Django CMS is represented in a folder called cms. If we open that folder, we can see tons of folders with documents that are responsible for the CMS logic. 
The next picture is a part of the diagram that represents the object classes responsible for the base of CMS, like control the website flux and the actors using the website.

![](/ESOF-docs/images/plugin.png)

**Alias plugin** is useful for content that is present in more than one place. **Placeholder plugin** is responsible por implement the software for special model fields that DjangoCMS uses to render user-editable content in templates. That is, it’s the place where a user can add text, video or any other plugin to a webpage, using either the normal Django admin interface or the so called frontend editing. And the **CMS plugin base** it's responsible for the main plugin in general.

After plugin section, we have the toolbar section where we have the tools to edit the front-end page.

![](/ESOF-docs/images/toolbar.png)

The main class is the **CMS toolbar** that has 3 toolbars associated: **Page toolbar**, **Placeholder toolbar** and **Basic toolbar**. All bring to the main toolbar, some personalized features to edit de front-end webpage.

After the base plugins and toolbars we have some classes that are also important to make funcionalites possible. One is the **Plugin Context** that allows modify all plugin’s context before rendering.

![](/ESOF-docs/images/plugincontext.png)

To make the connection with the views, we have **CMSAttachMenu** and **CMSMenu**.

![](/ESOF-docs/images/menu.png)

Next, we have the class responsible for the CMS configuration (**CMSConfig**), **NavExtender** responsible to modify de nav and **SoftRootCutter** class that represents the page that is the root of a significant new section on your site.

![](/ESOF-docs/images/mod.png)

**CMSPluginBaseMetaclass** has the base for plugins. And **AppRegexURLResolver** it's responsible for the routes configuration.

![](/ESOF-docs/images/models.png)

Next, we have a bunch of classes. **Apphook** is responsible for attach a Django CMS application to a page. **Toolbar** attach a toolbar to the Django CMS application. **CMSApp** makes the configuration of all application. **PluginMenuItem** allows you to choose and personalize the plugins that you want to use. **PluginPool** make the attach between app and plugins. 

![](/ESOF-docs/images/object.png)


To manage the software, Django CMS created some exceptions and warning to make more clear to actors they're impraticable/wrong usage of the framework.
   
    > - Expections:
    
![](/ESOF-docs/images/exception2.png)
    
    > - Warnings:
    
![](/ESOF-docs/images/warning.png)

**NOTE:** We opt to just represent the packages and their connections in some sections because they had to much functions what turned the class extensive. 

##3.2. Implementation View

##3.3. Process View 

##3.4. Deployment View

The **deployment view** describes the hardware components in wich software is developed. The main functions of this type of diagrams are show the hardware organization (nodes and their connections) and describe the hardware components used to unfold software. So, it's responsable to show to the developers how the components are unfolded in hardware. 

![](/ESOF-docs/images/dev.png)

Django CMS as a software that allows to create a website more easily with their new tools for editing the webpages design, we think that only exists 3 nodes: viewer PC, admin PC and Django CMS. And also, they communicate by HTTP requests. 

**NOTE:** Sometimes, the viewer PC and the admin PC can be the same, because you can be the admin of a page that you like to navigate.

##3.5. Use Case View

The **use case view** is responsible for the connection between all other 4 views (Logic, Implementation, Process and Deployment) and represents some of the actions that the actors are allowed to do in the software. The user as we mentioned before, can acess to the system as **Adminstrator** and **Viewer**. But sometimes, the user can be bought, because he can be Adminstrator of a page, and also a viewer of the same. So we have a general user (main actor) and the other two which are an inheritance of the main actor.

![](/ESOF-docs/images/use_case_2.png)

As we can see, a viewer can make what the administrator if they're the same. 

##3.6. Architectural Pattern

**Is Django CMS an MVC Framework?**
The answer is both **yes** and **no**. The MVC patthern advocates the decoupling of the presentation layer from the application logic. For instance, while designing an online game website API, you might present a game's high scores table as an HTML, XML, or comma-separated (CSV) file. However, its underlying model class would be designed independent of how the data would be finally presented.

MVC is very rigid about what models, views, and controllers do. However, Django CMS takes a much more pratical view to web applications. Due to the nature of the HTTP protocol, each request for a web page is independent of any other request. Django's framework is designed like a pipeline to process each request and prepare a responde. 

Django CMS call this the **Model-Template-View** (MTV) architecture. There is separation of concerns between the database interfacing classes (Model), request-processing classes (View), and a templating language for the final presentation (Template).

**If you compare this to MVC**, we have Model equals to Django CMS Model, View equals to Django CMS template and Controller is the framework itself that processes and incoming HTTP request and routes it to the correct view function.




