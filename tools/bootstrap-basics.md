# Bootstrap Basics
## Quick summary
Bootstrap is a CSS and Javscript framework to rapidly construct responsive and visually appealing front-end design for web applications. Bootstrap makes it easy to do anything from css dropdown lists to javascript modals and provides you with a fluid and responsive grid system to help you with positioning your buttons, your text etc (mostly) exactly where you want it. Instead of spending many hours creating css stylesheets and javascript code, you can use bootstrap's pre-defined grid system or components such as buttons, modals, dropdown menus, navigation menus etc. However, this only works if you are okay with Bootstrap's many assumptions about what you want your site layout and components to look like.

## Understanding the Grid System

The grid system is both the biggest strength and weakness of using bootstrap. It can take a while to get it fully figured out, but once you do, it is very powerful in getting your website looking exactly the way you want it to.

The basic premise is this:
1. There are an unlimited amount of rows and each row has exactly 12 grids of equal size.
2. You can put your content anywhere you want on this grid but you cannot customize this grid to your exact specifications -- if it doesn't work for you, too bad! (however, in most cases, the grid system is perfect for any kind of web app that doesnt have to have a heavily customized front-end)

## Examples of bootstrap-built websites
1. http://crumbs.am
2. http://timelyapp.com
3. http://surfacediary.net
4. http://foundmyanimal.com
5. http://dgbrt.fr

## Watch out for these common issues!:

1. Customizing the grid system - make sure you use offset properly and nesting properly. For instance if you use col-md-8 and you nest a col-md-6 in that, then in reality the col-md-6 is a col-md-4 (ie it is half of the col-md-8 since because of the rules of nesting bootstrap is looking at col-md-8 as an entirely new grid row in a sense).

2. Making sure you override properly - if you want to override bootstrap css you ahve to go into the bootstrap css file and manually override or you can put it at the END of the file or if you are using the gem you have to put it in the application.css to override the bootstrap css for all pages or put it in the specific page's css file to override just that page and keep the boostrap css for the rest of the pages.

3. When you use a template make sure you put everything in the right folder and include all the images in the template and make sure the template is calling the images properly otherwise it just won't look as good as the live demo did when you downloaded the template

4. Make sure you have the 'less' gem installed otherwise it wont compile bootstrap properly (unless you use the manual installation method)

5. When you use the bootstrap javascript make sure you understand how it is interacting with your rails app

## Other 'gotchas'

- ### Centering
Think you might want to customize the Bootstrap grid system a bit more to your specific needs - maybe change the 12 grid system to a 14 grid system because you don't feel like doing so much nesting for each of your elements? Well too bad, because you can't - you just have to twist the bootstrap grid system to your needs using multiple nesting of columns, no matter how confusing and time-consuming it can be, to both write and read the code. If you feel yourself wanting to customize your website beyond bootstrap's capabilities a lot, you might want to take a look at the ZURB Foundation framework instead.

- ### Syntax
Another 'gotcha' you need to look out for are syntax errors. Bootstrap does have many difficult to remember names for its components so feel free to always look up each component on the bootstrap site and make sure you have the spelling and syntax correct. For instance, offsetting columns has a somewhat difficult syntax...if you wanted to have a 6 grid container offset by 3 grids from the left, you would write: col-md-6.col-offset-md-3.

- ### Bootstrap templates
Be very careful when installing bootstrap templates! You need to make sure you download **all** the code, pictures, stylesheets, and javascript code and put it in the right files in the assets folder. You should also understand how the template interacts with and changes the bootstrap code so you can troubleshoot errors properly. 

- ### Installation
Make sure you install the official and constantly updated 'bootstrap' gem (in which case you would also need the 'less' gem) or if you prefer sass, you can install 'bootstrap-sass' gem (which would require the 'sass-rails' gem). 
    
    For beginners, it is ***highly recommended*** that you do the manual install instead (download the Bootstrap files from http://getbootstrap.com and copy and paste the bootstrap files into the proper folders in your assets folder (either the stylesheets folder or the javascript folder) - this way you can look through the bootstrap code and fully understand and troubleshoot any errors that come up.


##Tips
- Make sure you understand the grid system (cannot reiterate this point enough!)
- Look through the official 'getbootstrap' site first and see all the components and designs that are available to you
- Look through some template websites as well as some sample bootstrap using websites to see what your finished product might look like

##Bootstrap vs Foundation

Another popular web framework that you might be considering is the Foundation framework by ZURB. Here are the main differences between the two frameworks:

In essence: Bootstrap is heavily opinionated especially about the layout of your site (with its grid system) and was created with web developers in mind, while Foundation is unopinionated and was created with web designers in mind.	

1) Bootstrap makes a lot of assumptions about what you are trying to do with your front-end (with its grid system and with its heavily pre-defined CSS and Javascript components) - this can be a good thing if you agree with their assumptions because it significantly cuts down on the amount of time you need to implement your ideas yourself if someone has already built the skeeleton for you. Of course, if you want a different grid system, have a different set of assumptions or just want your website to look crazy and unlike anything else on the web you are SOL - you can probably use bootstrap and mess around with the grid system but it entirely defeats the purpose of bootstrap if you spend most of your time pulling your hair out figuring out how to circumvent their grid system so it fits into your design ideas.

2) ZURB Foundation design is just not as nice out of the box as it is for bootstrap. Foundation was purposefully designed this way, as it is for designers who want to heavily customize their site. Since the initial design for Foundation is such a blank slate, designers have more creative control over how the site design turns out.

##Resources

1. http://www.sitepoint.com/twitter-bootstrap-tutorial-handling-complex-designs/
	- provides a good quick setup guide
2. https://github.com/twbs/bootstrap
	- bootstrap gem site
3. **http://www.getbootstrap.com**
	- the official bootstrap site...go here first if you want to look something up
4. http://hollsk.co.uk/posts/view/why-i-switched-to-susy
	- some problems you might have with bootstrap
5. http://www.bootstrapswatch.com
	- a good list of bootstrap themes (Again be careful to use these as prescribed or they won't end up looking as good as the live demo!)
6. http://expo.getbootstrap.com
	- examples of cool site and apps built using bootstrap as the front-end!