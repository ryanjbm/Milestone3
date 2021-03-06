# Hidden Gems: Milestone Project 3

[Live Project](http://hiddengems-milestone3.herokuapp.com/)

<img src="static/images/responsive.png">

# Introduction
Hidden Gems is a site made so that people can join the community and share the products that they love to friends, family and strangers. The site labels products under £20 as a 'Hidden Gem' and provides people with external links to the products.

This is my third Milestone Project of four towards my Full Stack Software Development Course, throughout this project I utilised HTML, CSS, JavaScript and Python, as well as Flask, Materialize and JQuery Frameworks and MongoDB to put the whole project together.

# UX

### Goals

* To provide a platform where users are able to upload products along with the image for others to see
* To create an aesthetically pleasing and easy to navigate webpage for the user
* To use Interactive and effective features on my website
* Provide a functioning account creation service for users

### User Stories

1. I am a user wishing to show people my favourite products
1. I am a user looking for gift ideas
1. I am a user wanting to see what members of the hidden gem community recommend to buy specifically in the fitness category 
1. I am a user who wants to search for which phones people recommend on Hidden Gems
1. I am a user looking to see what experts recommend I should buy for my home office
1. I am a user wishing to create an account on Hidden Gems to recommend a product i recently found


### Design Process

1. My process began with creating a wireframe on figma, designing my site with initially a blue colour scheme in mind, I settled on a home page, login/register pages, article pages as well as community recommendations page.
1. Throughout my design process my colours used were changed to the following: <br>
  Black (Used for navigation and footer bars)<br>
  Teal (Used for highlight text and most buttons)<br>
  White (Used for navigation text and footer text)<br>
  Black  (Used for general text on the page)<br>
After some experimentation and changes throughout the design and building process these were the colours that I decided look the best, the fonts I used were the following:<br>
  Arvo <br>
  Josefin <br>
  Karla <br>
1. I made a wireframe for my project using FIGMA. I made the design aesthetically pleasing and made sure it was easy to navigate through. I first made my desktop page and then made my mobile layout. Throughout the process of building my website I made a few changes and additions based off of my experience as well as input from family and friends
1. Some of the changes I made included editing the layout of the page, customising features on the site too



# [Figma Wireframe](https://www.figma.com)
> This includes the wireframes for both desktop and mobile device layouts
<img src="static/images/figma.png">
<img src="static/images/figma1.png">
<img src="static/images/figma2.png">
<img src="static/images/figma3.png">

Throughout the process of coding my website and input from other people, a few improvements were made to the website to not only make it look more professional but also to include more useful features.


# Features

### Features throughout page
* Collapsible Navigation Bar which is stuck to the top of the page, once collapsed side nav becomes available
* When Logged in or Logged Out different options are available in the menu to click on
* Unable to visit register or login page when a user is in session, any attempt will redirect to the home page

### Nav Bar
* Collapsable Nav Bar
* Different menu options available when logged in
* Side Nav when collapsed
<img src="static/images/figma5.png">

### Hero Section
* Image carousel automatically switching every few seconds
* Overlay text sliding in from different directions after each image change
<img src="static/images/figma4.png">

### User Session
* Using MongoDB to have a user register and login feature
* Certain pages aren't available when logged in and logged out
* Unable to register an account which is already in the database

### Community Recommendation
* Users can submit their own recommendations
* All fields must be filled, validated using WTForms
* User pastes in image address
* If item is under £20, product is marked as a hidden gem, box turns yellow with star

### Contact Form
* Email js api used
* Checks all fields are filled before allowing to submit
* Page refreshes afterwards
* Functional contact form which sends email to my account, showing who sent the email

### Admin
* As admin you are able to delete any recommendations people have made
* As admin can also add new categories for products that people may want to recommend

### Security
* As passwords were being saved, I used Werkzeug to encrypt passwords to my database
* Protects users passwords from being revealed if site was to be hacked
* WTForms used to prevent people from editing frontend security and bypassing
* Backend Python used to redirect if user is logged in so cant access register or login pages and if user isn't logged in can't access profile or recommend product pages

# Technologies Used

### Languages
* HTML5
  * Base language for the project used to add content to the website
* CSS3 
  * Used to style content
* JavaScript
  * Used to add Interactive features to webpage
* Python
  * Used for Backend programming
  
  
### Technologies
* [Materialize Framework](https://materializecss.com/)
  * Used Materialize for features such as my navbar, layout, carousels, buttons, footer and forms
* [FontAwesome](https://fontawesome.com)
  * Used for social links in footer, hero image, navbar and back to top button
* [Google Fonts](https://fonts.google.com)
  * Used Arvo, Josefin and Karla
* [Google Images](https://www.google.co.uk/imghp?hl=en&tab=wi&authuser=0&ogbl)
  * Used for all of my images, each was checked to be copyright free
* [W3 Schools](https://www.w3schools.com)
  * Used for help with the code in my project, I found it very useful for my form and gallery page
* [W3C Markup Validation](https://validator.w3.org)
  * Used this to check that my HTML and CSS code were both valid throughout my project
* [Stack Overflow](https://stackoverflow.com)
  * I used this to help me with small issues I encountered when writing my code
  
  
# Testing

### Testing User Stories

1. "I am a user wishing to show people my favourite products"
  User would click on <b>Login</b> then <b>Recommend Product</b> fill out the form and press recommend product button.
3. "I am a user looking for gift ideas"
  User from the home page will click on the <b>Community Recommendations</b> tab and scroll though the products for ideas 
5. "I am a user wanting to see what members of the hidden gem community recommend to buy specifically in the fitness category"
  User will click on <b>Community Recomendations</b> tab and then in the <b>Search Bar</b> type in "Fitness", this will then only display results with fitness in.
7. "I am a user who wants to search for which phones people recommend on Hidden Gems"
  User will click on the <b>Community Recommendations</b> tab from the home page and in the <b>Search Bar</b> type in "Phones", this will then only display results related with mobile phones
9. "I am a user looking to see what experts recommend I should buy for my home office"
  From the <b>Home Page</b> the user will scroll down and select one of the articles for example the <b>Home decor</b> Article and read through what experts recommend. 
11. "I am a user wishing to create an account on Hidden Gems to recommend a product i recently found"
  User will navigate to <b>Register</b> page via navigation bar, fill in the Register form and click submit, they will then be redirected to the <b>Profile</b> page, an option will appear saying <b>Recommend Product</b> which they will click, fill in the form and press the recommend product button to submit.
  
### Manual Testing
* Test: Find the purpose of the site
* Expected outcome: To find a description on the first page of what the site does without needing to scroll.
* Result: Passed

* Test: Able to register a new account and view profile
* Expected Outcome: Be able to register with all forms functioning properly and able to login
* Result: Passed

* Test: Able to recommend product
* Expected outcome: Once logged in, able to fill out product recommendation form and successfully submit
* Result: Passed

* Test: Be able to edit recommendation
* Expected outcome: Be able to click edit button and change fields such as the name of product and submit change
* Result: Passed

* Test: Be able to delete product recommendation
* Expected outcome: Be able to click edit button on product submitted by user, click delete and confirm delete in pop up window
* Result: Passed

* Test: Unable to register without filling in all fields
* Expected outcome: When filling in field if left blank on submit message appear under field saying to not leave blank
* Result: Passed

* Test: Unable to register with unmatching password
* Expected outcome: When filling in field if passwords do not match, message flash above field saying passwords don't match and user is unable to register
* Result: Passed

* Test: Unable to login with wrong login details
* Expected outcome: Flash message above form saying wrong username and or password
* Result: Passed

### Testing Devices

My webpage was tested using Google Developer Tools to see if it's responsive. All devices were tested successfully including Iphones, Samsungs and Ipads of different screen sizes

### Validating HTML5 and CSS3 code

My code was tested on the WC3 Validation pages and passed all tests
<img src="static/images/htmlcheck.png">
<img src="static/images/csscheck.png">


### Different Browsers

I tested my page on the following browsers and found it worked on all

* Safari
* Chrome
* Firefox

### Other testing

Extensive testing by family, friends was used and no issues arose when doing so

# Deployment
This project has been pushed and deployed to the cloud application platform Heroku.

1. On Heroku create an account and log in.
1. Click new and create new app.
1. Choose a unique name for your app, select region and click on Create App
1. Go to the CLI and type $ sudo snap install heroku --classic
1. Type $ heroku login command into the terminal, type the email and the password.
1. Go back to Heroku, under Settings find Info and copy the Heroku Git URL.
1. Go to the CLI and type the command $ git remote add heroku <Heroku Git URL>
1. Create requirements.txt ($ sudo pip3 freeze --local > requirements.txt)
1. Create a Procfile ($ echo web: python app.py > Procfile)
1. Type git add ., git commit -m "Initial commit" and git push -u heroku master
1. Type $ heroku ps:scale web=1 into the terminal.
1. Go back to Heroku, under the Settings click Reveal Config Vars and set IP to 0.0.0.0 and the PORT to 5000. Set "MONGO_URI", "MONGO_DBNAME" and "API_KEY" with the corresponding values.
1. Go back into Heroku and under More click Restart all dynos
1. Click on Open App

### Deploying

I created my Milestone project using the GitPod environment and pushing it to Github after completing each section, this made sure that my project had good version control in place in case I needed to change some of the work. To create a live version of my project for people to view I did the following:


# Credits

### Content

The content of my website was written by me

### Media

Images I used were free to use but came from the following websites:

* [Google Images](https://www.google.co.uk/imghp?hl=en&tab=wi&authuser=0&ogbl)

Code snippets that I used for my read more buttons scrolling text came from the following website:

* [StackOverflow](https://stackoverflow.com)

### Acknowledgments

# Pages for information

* [Stack Overflow](https://stackoverflow.com)
* [W3schools](https://www.w3schools.com)
* [W3c](https://validator.w3.org)
* [Bootstrap](https://getbootstrap.com)

Thank you to the following for the support on issues and for offering advice on my project throughout:
* Code Institute Mentor Brian Macharia
* Code Institute Tutor
* Code Institute Slack Community
* Family and friends for constructive criticism

