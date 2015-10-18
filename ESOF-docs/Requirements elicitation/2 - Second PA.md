2. Requirements Elicitation
===================

 

###2.1. Issues on Django-CMS


Django-CMS by being open-source allows any outside contributor to post any issue they may find in the code or design and they are not limited to errors and bugs but can also suggest any kind of performance improvement. This type of contributions are the new requirements that outside developers think that program should have. If you are a developer, and you want to start to contribute and help to improve Django-CMS you should join the [django-cms-developers](https://groups.google.com/forum/#!forum/django-cms-developers) list and you should look for #django-cms on [freenode](http://freenode.net/) IRC network to discuss the platform development. Also, you just need to fork Django-CMS on github and send a pull request when you feel your code is good enough for inclusion.

##2.1.1. Raising an issue

In order to raise an issue Django's documentation wants firstly to raise awareness for **not posting any security issue** publicly (through IRC, GitHub, nor e-mail addresses, or any other forum or chat, etc) and they have specifically added an e-mail (security@django-cms.org) to post any security issue.

All other issues can me submitted through the other referred means and we will be focusing mainly on submitting the issue through GitHub. So you just need to fork Django-CMS on github and send a pull request when you feel your code is good enough for inclusion. Also, you need to add some unit-tests and documentation, that will help the acceptance of your piece of code by a core developer.

The core developers of Django-CMS defend that the process to raise a new issue after fork the project, is mainly hack, test, commit and test again. After that you push to your fork and make a pull request to the main project. And at any point you should discuss, because it's always useful for everyone to pass ideas around and look at things together.

##2.1.2. How to efficiently construct an issue report

To efficiently construct an issue report, you should have the code, some unit-tests to prove that works and explicit and detailed documentation. Django-CMS it's really demanding about this three things. Your issue can be automatically rejected if missing one of the three in the report. 

In order to maximize time efficiency through clarity a report should contain a clear, succinct and informative title, for example:
> “show_sub_menu displays incorrect nodes when used with soft_root” is helpful, whereas “Menus are broken” is not.

In report's description/documentation it should be included:

>- How to reproduce the problem.
>- What you expected to happen.
>- What did happen (a traceback is often helpful, if you get one).

It's really important run and write tests because a pull request that lowers the Django-CMS testing coverage will only be accepted as an exception. If it is a bug-fixing patch, the issue requester need to demostrate the bug with a test to check the fix works.
If you have the three things, your issue will be hardly rejected.

##2.1.3. Getting your issue accepted

If we browse through GitHub's issues submission history we can observe that many of the issues have labels as seen on the end of each submission title in the image below that descibe current issue state.
![Issues - Labels](/ESOF-docs/images/issues_labels.PNG)

You must be patient and see if you are asked for more information before it's accepted. It can go through some discussion and you can be able to get an approval even if the core developer wasn't optimist at the beginning. The issue can be rejected as **non-issue**, it's not actually a problem; or, **won't fix**, addressing your issue is beyond the scope of the project, or is incompatible with our other aims. 

##2.1.4. Ticket processing

As seen on the above image, tickets will get a status attributed to them, to see what stage the ticket is at. ("Status: ready for review" -- "Status: ready to be merged")
Additionally, submissions may be marked with a 'needs' label where it is specified what must be added by the contributor in order for the ticket to continue to be processed. ("needs design decision")
These will have a red background if they are critical and prevent the processing for being completed or a blue background if the need is not critical, such as:
>docs
(pull requests only) Code without docs or tests?! In django CMS? No way!

Kinds can also be used to mark and specify the point of the ticket, i.e., whether it is enhancement, bug fix, etc.
Components mark can specify which components the ticket affects. ("component: frontend")
Any other miscellaneous marks or comments may also be added. ("backport")

Django CMS ticket processing system rules:
>- one and only one status must be applied to each ticket
- a healthy ticket (blue) cannot have any critical needs (red)
- when closed, tickets must have either a healthy (blue) or dead (black) status
- a ticket with critical needs must not have non-critical needs or miscellaneous other labels
- has patch and on hold labels imply a related pull request, which must be linked-to when these labels are applied
- component, non-critical need and miscellaneous other labels should be applied as seems appropriate

When they recive the ticket, the first thing they do it's decide if it's a pull request or an issue. The acceptance means the ticket is healthy, and will have a blue label (and that means they are going somewhere).
>- ISSUE - The bar for status: accepted is high. The status can be revoked at any time, and should be when appropriate. If the issue needs a design decision, expert opinion or more info, it can’t be accepted.
- PULL REQUEST - When a pull request is accepted, it should become work in progress or ready for review or even ready to be merged, in those rare cases where a perfectly-formed and unimprovable pull request lands in our laps. As for issues, if it needs a design decision, expert opinion or more info, it can’t be accepted.

As said before, **no issue or pull request can have both a blue (accepted) and a red, grey or black label at the same time**.

Tickets can be accepted (blue label), rejected (black label) or marked as having critical needs (red label). 

###2.2. Use Case Diagram

Use Case Diagrams shows the system utility and purpose, specifies the system context and the functional requirements as in use cases. Django CMS as a content management system platform for publishing content, they have only two actores: 
>- **User**, the actor has acess to the page after register, sees the page content and can do what admin allows him to do.
- **Admin**, the actor that generates and manages the page, and gives the user permissions.

![Use Case Diagram](/ESOF-docs/images/use_case.png)
