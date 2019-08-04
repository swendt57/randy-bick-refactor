## Randy Bick Photography

This is a refactor of randybick.com which was originally designed for larger screens only. I have been friends with Randy for many 
years and have worked with him to create at least three major versions of this website with numerous adjustments in between. 

It was time for a responsive design and that's what I chose for my first milestone project. You can view the existing site at 
www.randybick.com along with this new design that is temporarily deployed at www.randybick.com/new.

### UX
Randy is approaching retirement, so he has been winding down his business the last few years along with the level of detail 
on his website. Due to his upcoming retirement, and since this is a redesign of an existing website, only a few user stories were created. 

User Stories:
* User wants to view examples of Randy's work.
* User wants to be able to easily contact Randy.
* User wants to understand Randy's personality to assure he would be compatible with them.

I created some mock-ups in Balsamiq Mockup 3 and these can be downloaded from my GitHub site at 
https://github.com/swendt57/randy-bick-refactor/tree/master/support_documents/mock-ups

### Features

**The site includes the following:**

* A **Home** page that displays a few of Randy's images and links to a photo gallery of eclectic images.
* An **About Randy** page that gives a brief highlight of Randy's accomplishments and his photographic process.
* A **Fine Art** gallery that displays some of Randy's more recent Cincinnati, Ohio and Covington, Kentucky "city-scapes."
* A **Corporate Photography** page that provides examples of some of the corporate work Randy has done.
* A **Portraits** page that highlight two different possible photographic packages, a single collage, or an album.
* A **Family Portraits** page that has galleries showing the albums for two different families.
* A **Contact Us** form that allows the user to submit questions to Randy.

**Possible future work:**

* Expand the Fine Art section with some other examples beyond city-scapes.
* Add in pricing. He used to have very specific pricing, but removed it a while back. He may put some general pricing 
estimates back in at some point.

### Technologies used

* Bootstrap 4
  * https://getbootstrap.com/docs/4.0/getting-started/introduction/
  * Responsive, mobile-first, framework
* Google Fonts
  * https://fonts.google.com/
  * Free, open-source, fonts
* Font Awesome
  * https://fontawesome.com
  * Icons and such
* Juicebox Pro
  * https://www.juicebox.net/
  * Purchased module for Randy's site
  * HTML5 responsive image gallery tool
* W3Schools
  * https://www.w3schools.com
  * Image overlay hover effect information 
* AWS Cloud9
  * https://aws.amazon.com/education
  * Online IDE
* IntelliJ IDEA
  * https://www.jetbrains.com/idea/
  * Java integrated development environment
  * My preferred IDE
* GitHub
  * https://github.com/swendt57
  * Code repository
* Stack Overflow
  * https://stackoverflow.com/
  * Community of developers
* Adobe Flash
  * https://www.adobe.com
  * Used for creating the animation of Randy's signature
  
#### Server Side Includes
I prefer to use Server Side Includes (SSI) as much as possible to avoid having to maintain the same code in multiple files
such as headers, and footers. However, GitHub pages does not support traditional SSI so I have implemented a
JavaScript version for now that works with both nGitHub and the WideWorks server. The w3-include-html="header.html"> div attribute is designed for this purpose.
  
### Testing

Since this is a basic website and not an application, testing was limited to testing all links and galleries on: 
* Chrome version 75.0.3770.100 browser including:
  * Galaxy S5 simulator
  * iPhone 6/7/8 simulator
  * iPad simulator
  *iPad Pro simulator
* Firefox 67.0.4 browser including:
  * Galaxy S9/S9+ simulator
  * iPhone X/XS simulator
  * Kindle Fire HDX simulator
* Edge 42.17134.1.0 browser
* Galaxy S7 phone with:
  * Chrome mobile version 75.0.3770.100
  * Firefox for Android version 67.0.3
  
 #### Problems discovered during testing
 * Overlay hover effect used on Corporate, Portraits, and Families did not line up for all screen sizes
   * The overlay effect required fixed positioning which turned out to be quite challenging with a responsive design.
   & My solution was to use a combination of Bootstrap tables along with Bootstrap div containers to provide a consistent structure
   for the absolute positioning required but still responsive to different screen sizes.
* The Juicebox galleries malfunctioned in multiple ways. 
  * Apple small screen devices tended to cut off the upper half of the galleries. The solution was to upgrade Juicebox to 
  the current version.
  * Then expanded collapsible nav bar was hidden beneath the galleries. Using developer tools, I discovered that the galleries 
  had an extremely high z-index, some I gave the nav an even higher value.
  * Inconsistent behavior on smaller screen sizes. The presentations vary somewhat from phone OS to phone OS. However, they 
  work on all tested phones.

### Deployment
 I have deployed the code using GitHub pages at https://swendt57.github.io/randy-bick-refactor as well as below a subfolder
 on Randy's current website. I use FTP to transfer the files to the wideworks.com, Randy's website host.
 
 #### Deployment steps
* Log into FTP client
  * ftp://randybick.com 
  * u: ask me
  * p: ask me
* Back up existing site on server, just in case 
  * Create an "old" folder at the root level.
  * Copy/move all the entire website to this folder.
* Choose the correct header file and rename to header.html
  * header-github is intended for GitHub Pages
  * header-server is intended for the WideWorks server.
* Copy the entire new site to the server.
* Test, test, test!!

### Credits

**In addition to the above, thanks go to:**

* https://hackerthemes.com/bootstrap-cheatsheet/
* Raaf003 on Stack Overflow for his JavaScript SSI-like "Include" function
* Jose Rui Santos on Stack Overflow for a reasonable "footer at the bottom of the screen" solution
* Michael B on Stack Overflow for his Grid Layout solution for allstate.html

Content written by Randy Bick and Steve Wendt

All images &copy; 2003-2019 by Randy Bick