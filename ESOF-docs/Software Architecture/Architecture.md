3. Software Architecture
===================



##3.1. Logical View

The **Logical View** represents all key abstractions (objects or object classes) in the system; or their packages. The main functions of this type of view are describe the organization of elements and diagrams into sections and their funcionalities, divide the software in different layers to shows it architecture and also represents the communication channels between layers.

The logical section of Django CMS is represented in a folder called cms. If we open that folder, we can see tons of folders with documents that are responsible for the CMS logic. 
The next picture is a part of the diagram that represents the object classes responsible for the base of CMS, like control the website flux and the actors using the website.

![](/ESOF-docs/images/plugin.png)

**Alias plugin** is useful for content that is present in more than one place. **Placeholder plugin** is responsible por implement the software for special model fields that DjangoCMS uses to render user-editable content in templates. That is, it’s the place where a user can add text, video or any other plugin to a webpage, using either the normal Django admin interface or the so called frontend editing. And the **CMS plugin base** it's responsible for the main plugin in general.




##3.2. Implementation View

##3.3. Process View 

##3.4. Deployment View

The **deployment view** describes the hardware components in wich software is developed. The main functions of this type of diagrams are show the hardware organization (nodes and their connections) and describe the hardware components used to unfold software. So, it's responsable to show to the developers how the components are unfolded in hardware. 

![](/ESOF-docs/images/dev.png)

Django CMS as a software that allows to create a website more easily with their new tools for editing the webpages design, we think that only exists 3 nodes: viewer PC, admin PC and Django CMS. And also, they communicate by HTTP requests. 

**NOTE:** Sometimes, the viewer PC and the admin PC can be the same, because you can be the admin of a page that you like to navigate.

##3.5. Use Case View

The **use case view** is responsible for the connection between all other 4 views (Logic, Implementation, Process and Deployment) and represents some of the actions that the actors are allowed to do in the software. The user as we mentioned before, can acess to the system as **Adminstrator** and **Viewer**. But sometimes, the user can be bought, because he can be Adminstrator of a page, and also a viewer of the same. So we have a general user (main actor) and the other two which are an inheritance of the main actor.

INSERT DIAGRAM 

##3.6. Pattern



