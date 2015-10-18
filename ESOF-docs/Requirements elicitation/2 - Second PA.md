2. Requirements Elicitation
===================

 

2.1. Issues
-------

Django-CMS by being open-source allows any outside contributor to post any issue they may find in the code or design and they are not limited to errors and bugs but can also suggest any kind of performance improvement.

 2.1.1. Raising an issue
-------

In order to raise an issue Django's documentation wants firstly to raise awareness for **not posting any security issue** publicly (through IRC, GitHub, nor e-mail addresses, or any other forum or chat, etc) and they have specifically added an e-mail (security@django-cms.org) to post any security issue.

All other issues can me submitted through the other referred means and we will be focusing mainly on submitting the issue through GitHub.

 2.1.2. How to efficiently construct an issue report
=======

In order to maximize time efficiency through clarity a report should contain a clear,succinct and informative title, for example
> “show_sub_menu displays incorrect nodes when used with soft_root” is helpful, whereas “Menus are broken” is not.

In report's description it should be included

>- How to reproduce the problem.
>- What you expected to happen.
>- What did happen (a traceback is often helpful, if you get one).

 2.1.3. Getting your issue accepted
=======

If we browse through GitHub's issues submission history we can observe that many of the issues have labels as seen on the end of each submission title in the image below that descibe current issue state.
![Issues - Labels](/ESOF-docs/images/issues_labels.PNG)


 Ticket processing
=======

As seen on the above image, tickets will get a status attributed to them. ("Status: ready for review" -- "Status: ready to be merged") 

Additionally, submissions may be marked with a 'needs' label where it is specified what must be added by the contributor in order for the ticket to continue to be processed. ("needs design decision")
These will have a red background if they are critical and prevent the processing for being completed or a blue background if the need is not critical, such as:

>docs
(pull requests only) Code without docs or tests?! In django CMS? No way!

Kinds can also be used to mark and specify the point of the ticket, i.e., whether it is enhancement, bug fix, etc.

Components mark can specify which components the ticket affects. ("component: frontend")

Any other miscellaneous marks or comments may also be added ("backport")


 Django CMS ticket processing system rules
=======

>- one and only one status must be applied to each ticket
- a healthy ticket (blue) cannot have any critical needs (red)
- when closed, tickets must have either a healthy (blue) or dead (black) status
- a ticket with critical needs must not have non-critical needs or miscellaneous other labels
- has patch and on hold labels imply a related pull request, which must be linked-to when these labels are applied
-component, non-critical need and miscellaneous other labels should be applied as seems appropriate


 2.2. Use Case Diagram
=======
![Use Case Diagram](/ESOF-docs/images/use_case.png)
