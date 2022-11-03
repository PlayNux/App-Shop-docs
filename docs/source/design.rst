What Design Is Not
====================
Before we get into all the things that make up playnux apps, there is a clarification that needs to be made. We need to understand what exactly design is about, but more importantly we want to smash two major myths:

**Design is not something you add on after you've completed a product.**

Whether you realize it or not, you are constantly designing anything you build. It is an intrinsic part of creating something. 
Design is not just what something looks like. It's not just the colors and fonts. 
Design is how it works. When you decide to add a button that does a thing, that is design.
You made a decision to add a button with an icon or a label and where that button went and the size and color of that button.
Decisions are designs.

**Design is not just, like, your opinion, man. **
Design is testable. One design will meet a specific goal better than another design. Consider different types of bicycles. A folding bicycle has a different set of design goals than a mountain bicycle. 
Things like weight, size, and tire tread are important factors in helping the intended user reach their goals. Because we understand that design is about solving specific problems, we must also understand that we can objectively compare the effectiveness of two designs at solving those problems.

=========================
Accessible Configuration
=========================

Providing settings can be a way to make sure an app is accessible to a wider set of users with special needs, but it can also be an easy way out of making design decisions about an app's behavior.
 Just like with problems of feature bloat, settings mean more code, more bugs, more testing, more documentation, and more complexity. 
 When considering adding options to your app, try to strike a balance of making your app more accessible without pushing design work onto your users.

=========================================
Build for the “Out of the Box” Experience
=========================================

Design with sane defaults in mind. 
playnux apps put strong emphasis on the out of the box experience.
If your app has to be configured before a user is comfortable using it, they may not take the time to configure it at all and simply use another app instead.

========================
Ask the Operating System
========================

Get as much information automatically as possible. 
Instead of asking a user for their name or their location, ask the system for this information. 
This cuts down on the amount of things a user has to do and makes your app feel more intelligent and integrated.

=================================
Is It Really About Accessibility?
=================================

Ask yourself if the configuration option you are adding is really necessary to make your app more accessible or if it makes sense to have a user make this decision. Don't ever ask users to make uninformed engineering or design decisions.

============================
When You Absolutely Have To
============================

Keep things contextual. Instead of tucking away preferences in a configuration dialog, think about displaying them in context with the objects they affect (much like how shuffle and repeat options appear near your music library).
If your app needs to be configured before it can be used (like a mail client), present this configuration inside the main window much like a . Once again, make sure this is really necessary set-up. Adding unnecessary configuration screens stops users from doing what they wanted to do when they opened your app in the first place.

======================
Minimal Documentation
======================

Most users don't want to read through help docs before they can use your app.
Instead, they expect that your app will be intuitive and simple for them to understand without assistance.

=======================
Use Understandable Copy
=======================

Avoid technical jargon and assume little-to-no technical knowledge. 
This lets your app be “self-documenting.”
Provide non-technical explanations instead of cryptic error messages.
If something goes wrong, a simplified explanation of what happened and how to fix it should be presented.
