## README

**Contributors:** Maya Minier

<p align = "center"> **_The Eat List_** </p>

**Project Summary:** This product aims to deliver a streamlined and simple way of categorizing your favourite restaurants into a visually appealing, minimalistic online database! It's often difficult to keep track of restaurants, especially because there's so much to know about them - where are they? What kind of food do they serve? How much do they cost? What do _you_ feel like eating today? This product aims to not only condense that information into one convenient location (because, let's face it, your mind is not as reliable as you'd think, and when you _just_ can't quite remember the name of that really good restaurant, The Eat List is here to save the day), but also to allow you to only look for and see the information that you feel is important. Don't care about the price? Don't show it! The Eat List is the restaurant hit list that you've never realized you needed until now. Whether you're a mother trying to feed your children, a boyfriend looking to take your girlfriend out on a date, an elderly couple trying to revisit that restaurant you fell in love in 30 years ago, or just a hungry kid, this app caters to anyone and everyone.


**MVP Features:** 
The basic necessity for this MVP was the ability to display a list of restaurants with several characteristics available (i.e. location or type of food), along with a function to add more restaurants to the list. That said, the ability to add more restaurants through the GUI had a bug that I couldn't quite fix, and I gave up on it after a good 45 minutes of researching (as it was working on the previous rails app that I had made as practice).
Here are the main features of the MVP:
* A main display screen for the restaurants.
  * Displays the restaurants in table form, with the pertinent information labeled at the top.
  * I chose not to include the ability to filter or choose certain characteristics/labels as I felt that it was not as central to the functionality of my MVP. 
* A data base in which to store the restaurant information (I used sqlite3).
* A GUI function to add new restaurants to the list. **broken**
  * While this is still buggy/broken, they can be added through the rails console or through the seed db file. 
* A GUI function to edit/destroy existing restaurants in the list.


**Functionality and Instructions:**
This product allows you to create a database of restaurants, in which each restaurant's name, type of food, and location can be stored. You can then edit/remove elements and add new elements to your database. It also allows your list of restaurants and their associated information to be displayed on a web GUI. 

In order to install and run this rails app on your device, follow these steps:
1. Clone the git repository to your preferred local directory as follows:
  * Open Terminal.
  * Navigate to your desired directory using cd.
  * On the Github Repository, click on "Clone or download" and copy the link that shows up.
  * Navigate back to your terminal, and type ```git clone <link you just copied>```. 
2. Ensure that you have Rails installed on your computer (if not, see [How to Install Rails](http://installrails.com/ "Rails Guide"))
3. On Terminal, navigate into the directory that you just cloned, and run ```rails server``` or ```rails s``` for short.
4. On any browser of your choice, go to the URL: ```localhost:3000```. 
5. Be sure to quit out of the rails server using ```CTRL^ C``` before making changes to the code. 

Unfortunately, since the creating restaurants GUI is currently broken on the prototyped website, any additions will have to be made directly through the code or through the terminal. This can be done in two ways:
1. Through Terminal:
  1. Once you are located in the app directory, run ```rails console```.
  2. Inside the console, create a Restaurant using the following template: ```Restaurant.create(name: '<restaurant name>', cuisine: '<type of food', location: '<location>')```
  3. Run quit to exit the console, and relaunch your local server using ```rails s```. 

2. Through the Code:
  1. Navigate to ```/app-folder/db/migrate/seeds.rb``` and in this file, create a new Restaurant object using the following template: ```Restaurant.create!(name: '<restaurant name>', cuisine: '<type of food', location: '<location>')```.
  2. Run ```rake db:root``` in Terminal.
  3. Relaunch your local server using ```rails s```. 


**Key Issues and Resolutions:**
A major issue that I faced was that I fell ill over the weekend, and so this greatly limited the amount of time and mental energy that I had available to myself, and so this bled into all of the other issues listed below. 
* A main issue that I faced was creating users and associating them with information (so that particular lists could be tied to particular users). Ultimately, I decided that this was too costly of an endeavour and not completely necessary in order for this app to function as an MVP, and so I cut it from my project. I had a half-completed prototype of a different system (using Bookmarks) that partly succeeded (see [here](https://github.com/minierm97/CS121-creativerails)), but I decided to scrap it because it was taking too much time and wasn't central to the product.

**Known Bugs:**
* Another issue that I faced was clearly the inability to create the restaurants through the online GUI. I researched the error and repeated my steps with a separate app to see if it happened again (which it did not), so I'm not entirely sure what part of the code I may have damaged in order to cause that bug, but since I couldn't find a workaround but didn't want to scrap all of my work by then, I instead looked up alternative methods to add objects (i.e. through the console and through the code). While this option is definitely not optimal as it fails to display the GUI's efficiency to the customer, it serves the intended purpose of simply adding a restaurant element to the database, and so given the time constraints, it seemed like the only possible way of including that central feature.


**References:**

* [Bookmarks Tutorial](http://12devs.co.uk/articles/writing-a-web-application-with-ruby-on-rails/)
* [Codecademy Ruby Guide](https://www.codecademy.com/tracks/ruby)
* [Codecademy Ruby on Rails Guide](https://www.codecademy.com/courses/learn-rails)
* [Learn Enough CSS and HTML Guides](https://www.learnenough.com)
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Ruby on Rails Tutorial](https://www.railstutorial.org/book/beginning)
* [Zero to Sixty Rails](https://code.tutsplus.com/tutorials/zero-to-sixty-creating-and-deploying-a-rails-app-in-under-an-hour--net-8252)
