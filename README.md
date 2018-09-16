[![Build Status](https://travis-ci.org/90t/book-club.svg?branch=master)](https://travis-ci.org/90t/book-club)

# CodeNote flasks micro services

The inspiration for this project came from studying python since 2016 before I attended IT & Maintenance in CoCC , this python class was of a night time in CoCC,
- Since then moving on to SoloLearn on my phone ,then Code institute with SoloLearn agian & then syllabus1_LMS1 & syllabus2_LMS2(cloud9)
- At this stage I was really looking forward to building something real in web development with the flask framework I had heard so much about
- Flasks Micro services was what I was really interested in , I was setting out to incorporate & learn microservices to speed up, improve, & build a website
- that could match the mern stack , the mean stack, django , this however is a long term goal as I am very pleased on how far I was able to push the development of this website
- I wanted to see if I could develop a messaging system without having to leave the flask eco system
- I also wanted to explore Flask-SQLAlchemy, the orm which allows a dev to programme a database
- Another key driver behind this project was idea of building a fullstack application with flask & cloud9, this was of course a challenge


## UX
 
The style of this website is very minimil, with a small bit of inline styling, this was down to the fact I wanted to focus on fuctionalty
- The nav bar is white to match the rest of the page , this is my attempt to bring the website together, with the hover of the links coming from
- the defualt styles from FlaskBootStrap, I also restyled the color of the navbar links , this had a massive effect on such a plain interface
- Changing the mail notification icon was also a massive changer in the over all aesthetics of my application
- When arriving on CodeNote you will be met with a sign in page where the user has the option of signing into the application
- or registering a new account, the user also has the option of email recovery & a remember me checkbox, since this is the first page the user will see,
- Once the user has logged in, the user will be greeted with a message with there user name that they had just signed with
- The main CodeNote/posts/forum/ page is accessible through the navbar with the link CodeNote,
- The users mail, logout , profile , & search engine are also availible on this page  


- Once on this page the user has the abitly to go home to his own posts/notes page or the user can go staright to his profile page or
- straight to his own mail page, 
- This page the main page , is also the page with all the users ,here the user can select another user & view there profile
- When hovering over a user name a popup box will appear with details about the user such as There user name , there most recent Post/CodeNote, & 
- the last time there were seen aswell as the date & year
- Also in this pop up box users can observe how many followers a user has & how many there are following
- The pop up box is also interactive, a user can select a user name & be transported to there profile page or a users profile page 
- They can also follow or unfollow a user by accessing there profile page , but the user can not follow themselves
- The users profile page is also the page where other coders/users can private message another coder/user
- 
- The home page is the page where users can leave a Note/Post & then this Note/Post will show up on the CodeNotes page, & there own home page
- 
- This application can come in very handy indeed , if 2 developers were working on a project ,
- they could very easliy communicate with one another through the use of the mailing system 
- with little to no distraction
- More devs on the note page or more team members could also join in & solve problems about there code & advise on going forward
- Where this application also would come in very handy is in a small business, or family business,
- This would give the all the team members access the communication to one another completly free of charge
- where this application can also be used is in a in house restaurnat communication system
 



###### Flask on cloud 9 venv setup python3
- The setup for this project was similer Django but with slight variations 
- First I created a blank instance with an ubuntu server on cloud 9
- Then I ran the command sudo pip install virtualenv, this installed the virtualenv that comes bundled with the ubuntu server
- Next I created my venv with virtualenv -p python3 env <<<-----name of virtual enviroment
- My next task was to activate the virtualenv with  clivenoonan:~/workspace $ source env/bin/activate
- Since I had the majority of my project already built on a different ubuntu cloud workspace server, I copy & pasted my requirements.txt file into my new project
- Next I ran the command pip freeze  -r requirements.txt
- Also pip install --upgrade -r requirements.txt, this updated & synced my packages to my project folder
- Finally I started my development folder, with the command env/bin/flask run --host=0.0.0.0 --port=8080
- After settting my env vars in heroku , when evr I neede to workon my project after I set the vars , I would have to run export FLASK_APP=blog.py
- If I wanted to workon my project with debug mode on I would run the command  export FLASK_DEBUG=1 <<---ON
- To turn debug off for deployment I would run the command export FLASK_DEBUG=0 <<-- OFF
- To run my local debug built in email server I would run the command python -m smtpd -n -c DebuggingServer localhost:8025 in a new terminal, with my bash
- terminal also running



## Features

## BluePrints 
- blueprints are a brillant feature to the flask framework, a good example of this is this project , I fully indented to build my project with a
- blueprint structure , for large aplliactions, even tho this is only a meduim to a small appllication, blueprints had a masssive effect on the organisation
- of my project
- In Order to acheieve this I created a main / auth/ errors BluePrints inside of my app folder
- I then registered my BluePrints in my __init__ package files
- This is similer to Django each BluePrint is like there own app 

## Enviroment Variables
- In Order to automate my env vars I configured a .env file , this technique is used by many frameworks such node.js, Django
- I also needed to install the install the dot.env with the pip package manager with the command pip install python-dotenv
- To connect my python package with the alias of dot.env in my config.py file I created this alias in my config class
- Next I needed to craete my.env file this is where I stored my SECRET_KEY, MAIL_SERVER, MAIL_PORT, MS_TRANSLATOR_KEY, variables
- while my aplication was running I saved my .env file , this process imports my varibles from me to my appliaction


## The Requirements.txt file
- To keep my packages up to date & in sync with my 3 repos GitHub/Heroku/Local
- I adopted the requirements.txt techniuqe , I updated & synced my poackge requirments with the pip package manager with the command pip install
- pip freeze > requirements.txt this essentially dumped all my projects dependencies to my requirements.txt, Heroku will heavily depend on this file in the
- deployment stages of my project
- When future up dates to my project are nessacary , I can then reproduce my project with just my requirements.txt file , aswell another developer


### Web Forms & Flask-WTF
- To work & set up my forms I had to have venv activated & I had intitiatd the project with my FLASK_APP=blog.py
- & ran my server 
- this was the only I could get cloud 9 to run the server
- A core component of my application is webforms, I accomplished this with Falsk web forms & the Flask-WTF exstention package which I installed with pip
- the python package manager, while my venv was active with the command pip inatll flask-wtf


### Database & Migrations 

- To create my database I used the python eco system to my advantage
- I used SQLAlchemy, I again installed this database python package with the pip package manager
- SQLAlchemy is a ORM  a object relational mapper, this package will act as the client to work with my python code 
- I needed another package to migrate my database during production, I needed a database migration framework
- for this I installed flask migrate with the pip package manager
- SQLAlchemy is not a database it is a mapper , so I also needed a database, for this task I chose sqlite for the devlopment database
- To create my database with SQLAlchemy I needed to configer my project to my os base line under system in my config.py 
- I then needed to create my models
- This led me to my migration workflow, to migrate my database during production of my project I needed to create a database repository
- to update my schema 
- To work with my database I needed to initiiaise my repository with the command flask db init
- This created an automatic migration folder into my project on cloud9 
- to create my first migration I used to command flask db migrate -m "just like git commit messsage ", just like git a message can be included in your migration
- for the changes in my project models to take effect to my database, I needed to run a upgrade command,
- flask db upgrade became a part of my migration workflow, this command automatically generated a sqlite.db database in my project,
- I then worked with the commands 

#### Migrate Workflow
## git add .
## git commit -m "Trying to flush out posts problem"
## git push origin master
## flask db migrate
## flask db upgrade
## flask db downgrade
## flask db current 
## flask db history 

- to manage & observe my database
- to populate my tables in my database I worked in the python interactive shell , I enterd this shell with the command
- python
- I also used flask shell , this eliminated the need to import my instance into my python shell everytime I wanted too manage my database I entered this
- flask shell with the command flask shell

### End Of Database & Migrations 



### User Logins & Avatars 
- I built my user subsystem with password hashing , by storing them in password hashs

### Followers & Error Handling

### Ajax Magic

### Moment.js

### Email Support , Dates & Times & Flask-Babel 

### Full-Text Search

### Notifications & Messages
- The notifications & messages feature was one of the main 2 features I wanted to implement in this project,
- This was down to there dynamic nature
- I also wanted to discover how to achieve this while staying inside the flask eco system
- My first task was to add a new model in my projects models.py file to create the database tables which inturn would work with my messaging system
- I also updated my user models model class 
- Next was my forms.py
- Next up was my routes.py , I created a new route that would accept & recieve messages using the GET & POST method
- I aslo created my jinja if statements in my user templates, to reflect if a user is viewing a profile that is not there own they will see the send private
- link , if there are on there own profile they will !not see the send private message link
- I also updated my templates to reflect my messaging system with html messaging templates
- I then added a new message method in my route.py 
- In order to have emphasis on the mail link in my navbar which is present on all pages, aswell as the drop down on mobile navigation
- I needed to include my my jinja if statements in my base.html to define that if the message count is 0 there is nothing dispalyed
- My mail badge will appear only when there is unread message 
- In order to make my badge more dynamic I need to use js by using a jquery fuction that searches for an element that repesents the badge
- when jquery finds the element the css method is applied by changing the visisbilty of the badge to visible when there is a message &
- not viisble when there is !not a message
- Next was to create my notification models , I used the payload_json for this operation
- because of this addition I also added a new model field to my main models.py to reflect my changes

 

### Features Left to Implement

- Another feature idea

font-family: "Source Sans Pro",Helvetica,sans-serif

    color: #666;
    style="color:#666;" "font-family: "Source Sans Pro",Helvetica,sans-serif;"


sET ENVIROMENT VARIBLE
## heroku config:set LOG_TO_STDOUT=1
## Created postgresql-graceful-71515 as DATABASE_URL
## 
## 
## Compile Languages
## 
## 
## 
## 
## SET HEROKU ENVIROMENT VARIBLE
## heroku config:set FLASK_APP=blog.py
## Setting FLASk_APP and restarting ⬢ book-of-hue... done, v5
## FLASK_APP: blog.py
## 
## 
## PUSH TO HEROKU WORKFLOW
## no changes added to commit (use "git add" and/or "git commit -a")
## (env) clivenoonan:~/workspace (master) $ git add .
## (env) clivenoonan:~/workspace (master) $ git commit -m "First push to heroku"
## [master 9f10d8c] First push to heroku
## 
## 
## https://my-book-of-hue.herokuapp.com/ | https://git.heroku.com/my-book-of-hue.git
##
## HEROKU UPDATE WORKFLOW
## 
## 
## heroku login
## 
## git add .
##
## git commit -m ""
##
## git push heroku master
##
- 


- 



## Technologies Used

- [Flask](https://docs.djangoproject.com/)
    - The project uses Django 2 for rapid web development, clean design & a pragmatic approach

- [Cloud9](https://https://c9.io/)
    - The project uses Cloud9 to Write/Code & format syntax in various languages.

- [Heroku](https://https://www.heroku.com/)
    - The project uses **Heroku** as an app deployment hosting platform for my application 
    
    
- [TravisCI](https://travis-ci.org/)
    - The project uses **https://travis-ci.org/** for continues testing intergration, test passsing on git repo

- [Git&GitHub](https://github.com/)
    - The project uses **https://github.com/** to version control the development project
    

- [CSS3](https://https://www.w3schools.com/)
    - The project uses **CSS3** to to Style the elements & Responsive WebDesign.
    
- [Js](https://https://https://www.w3schools.com/)
    - The project uses **Js** to add interactivity & to interact with stripe.
        
   
- [LightHouseChromeExstention](https://chrome.google.com/webstore/detail/lighthouse)
    - The project uses **LightHouseChromeExstention** to test seo data & accsseibitly & best practices
    
- [validator.w3](https://validator.w3.org/)
    - The project uses **validator.w3** to test seo data & accsseibitly & best practices
    
- [jigsaw.w3](https://jigsaw.w3g/)
    - The project uses **jigsaw.w3** to test validation of CSS3
    -also to test seo data & accessibility & best practices

## Micro Services

- [FlaskBootStrap](https://https://getbootstrap.com/)
- The project uses **BootStrap4** to assist the Developer with a built in css library79376504
- aswell as reusable components

- [Flask-Babel](https://https://https://www.w3schools.com/)
- I used flask babel to add support for date & time formatting
- 
- [Flask-Login](https://https://getbootstrap.com/)
- I used Flask-Login for user session management which  handeled my authentication system
- 
- [Flask-Mail](https://https://getbootstrap.com/)
- I used Flask-Mail to provide a simple interface to set up SMTP with your Flask application
- and to send messages from my views from inside my flask application
- 
- [Flask-Moment](https://https://getbootstrap.com/)
- I used Flask-Moment Formatting of dates and times in Flask templates using moment.js.
- 
- [Flask-SQLAlchemy](https://https://getbootstrap.com/)
- I used Flask-SQLAlchemy as my ORM manager to work with my database
- 
- [Flask-WTF](https://https://getbootstrap.com/)
- I used Flask-WTF to work with my forms
- 
- [guess-language-spirit](https://https://getbootstrap.com/)
- The project uses **BootStrap4** to assist the Developer with a built in css library
- 
- [WTForms](https://https://getbootstrap.com/)
- I used WTForms to validate my forms



## Testing


##### I ran all my files through a validation test using
##### Passing 100%
- [W3C](https://validator.w3.org/) for HTML.
- [W3C](https://jigsaw.w3.org/css-validator/) for CSS.
- [JS Hint](http://jshint.com/) for JavaScript.
- [TravisCI](https://travis-ci.org/) for Continues testing tests passing on github


Tested On   
- Chrome. 
- Internet Explorer.
- Microsoft Edge.
- Firefox. 
- Opera.
- Continous design Testing SonyXsperia Mobile Phone 
- Continous design Testing Windows10XL Mobile Phone 
- Continous design Testing 42 Inch sharpSmart Led TV
- All Browsers & Mobile devices Display the whole site as was intended 
- [LightHouse](https://chrome.google.com/webstore/category/extensions) 


## Testing


USER1 :
gets wind of an awesome surfing website where he can buy surfboards,
he finds the link thru soacial media & connects , he browses the site for a few minutes & decides he might make a purchase , he completes his purchase with out having to create an account
Test1 User1 ( True/False )
Was User1 able to complete his purchase with out having to create an account?
True


USER2:
is just packing up from surfing for the day, when she hears an advert on the radio about an online surf shop , she clicks on ,after being in the water all day she fills in her details incorrectly, she tries again with all the correct details , but being in such a hurry , she never finishes the task , so she puts the phone down , when she arrives home , she brings her mobile with her , she puts it down , her daugther picks it up & begins exploring the website, she gets thru most of it & discovers the cart , she manages to get all the way with a pink surfboard she quite fancied, she gets to the stripe popup box, & recalls her dad working treiesly on something the exact same on his computer, she remembers what to do , she manages to remeber the test long password with the same numbers , then she remembers the easy one with 3 numbers , 

She is then left with the calender, she does not qiute understand this type of calender, so she fills in what she knows and carrys on , she see,s the little box shake with disagreement & decides she better put it away

Test1 User2 ( True/False )
Was User2 able to create an account when she filled in her details incorrectly?
Falsh
Was User2 daugther able to make a purchase when she filled in her details incorrectly?
falsh
RESULT 100%



USER3
is coming home from work on the bus  he begins to shoulder surf another passengers laptop , as he admires the website he retrives his mobile from his pocket & reads the address, connects to the website, he attempts signing up for the first time , USER3 has only been using a mobile for a week he has spent most of his life on the beach, must be why his eyes are so good,
he fills in his details with the first name & the last name as the same name,
he then attempts to only enter in 6 characters in the passsword field, with an incorrect email address , 

After a bit of a shock from all the errors he concetrates on the insructions before him , after a few minutes studying , he fills out all the info correctly, except for his email address, he then attempts for the second time to register an account , observing the error , he realises he has forgotten his @ symbol , he then corrects his typo & proceeds , 

Test1 User3 ( True/False )
Was User3 able to create an account when he filled in his details incorrectly?
Falsh
Was User3 able to create an account when he filled in his details with just the @ symbol missing?
falsh
Was User3 able to create an account when he filled in his details correctly?
True
RESULT 100%

## Bugs

### Email
### Translations
### Notifications

## Please edit configuration/connection/logging settings in '/home/ubuntu/workspace/migrations/alembic.ini'

If this section grows too long, you may want to split it off into a separate file and link to it from here.

 

## Testing

In this section, you need to convince the assessor that you have conducted enough testing to legitimately believe that the site works well. Essentially, in this part you will want to go over all of your user stories from the UX section and ensure that they all work as intended, with the project providing an easy and straightforward way for the users to achieve their goals.

Whenever it is feasible, prefer to automate your tests, and if you've done so, provide a brief explanation of your approach, link to the test file(s) and explain how to run them.

For any scenarios that have not been automated, test the user stories manually and provide as much detail as is relevant. A particularly useful form for describing your testing process is via scenarios, such as:

1. Contact form:
    1. Go to the "Contact Us" page
    2. Try to submit the empty form and verify that an error message about the required fields appears
    3. Try to submit the form with an invalid email address and verify that a relevant error message appears
    4. Try to submit the form with all inputs valid and verify that a success message appears.

## My Application looks amazingly responsive across al screnn sizes this is maonly down to the flask framework & FlaskBootStrap 



## Deployment

- The stages to deploy this project were very ordered & structured,
- first I needed to make sure I had an up to date version of HerokuCLI
- Once established I proceeded to login to my heroku account in my cloud9 bash terminal
- With my project all ready under source control I reinitilised my git repo with git init 
- My Next task was to create an app with a unique name from the HerokuCLI with the command heroku apps:create 
- With my new app created I recieved my new heroku git address/url 
- I clarafied my new remote address with the command git remote -v 
- To clarafay my app creation I checked my heroku cloud managment console once satisfied I proceeded 
- Herokus ephemeral file system dictates that the file storage is not permanant, because of this I used the technuigue of provisioning a postgres database on my
- heroku platform
- I achieved this with the HerokuCLI by running the command heroku addons:add heroku-postgresql:hobby-dev , this gives me the free thier , the excate same as
- creating from the heroku cloud managment console
- this task attached a database url connection & set the env varaiable to DATABASE_URL , this url acts as a pointer when I deploy my application to my new
- postgres database

## Deployment Stage2

- Next task in deployment was to update my requirements.txt with the package psyscop2 & gunicorn, heroku needs these packages to
- psyscop2 is the postgres database driver sql depands on this driver when you connect to a postgres database with heroku as the hosting platform
- I also added gunicorn , this package is required to connect to heroku server,
- next I needed to freeze my requirements to make sure all my packages are updated 
- Procfile was next up , I created this file in  the top level of my project the folder on cloud9 & then added the relevent values to tell heroku
- Then I created a Procfile , to establish with heroku what type of app is being served ,
- in my Procfile I made the necessary configerations of web: flask db upgrade; flask translate compile; gunicorn blog:app
- I then used the herokCLI to set my env variable with the command heroku config:set FLASK_APP=blog.py
- With this command this env variable, will exist in heroku in side the application env


## Deployment Stage3

- Next I needed to
- Git add ./Git commit -m ""/ Git push/ to my local repo on my machine
- this will also sync my repo on GitGub, now both my branchs are now at the master branch
- Finally I ran the command Git push heroku master to sync my Heroku repo
- 
## My Live Practical Python Project CodeNote can be viewed fully deployed on heroku [here](http://my-book-of-hue.herokuapp.com/)

## VERSION CONTROL

- The  project folder lives at this address
  [github](https://github.com/90t/book-club) <------ THIS IS THE LIVE PROJECT FOLDER
- heroku  https://git.heroku.com/book-of-hue.git 
- origin  https://github.com/90t/book-club 


  












##  style="background-image: url('{{ url_for('static', filename='img/g.jpeg') }}" "height: auto;" "max-width:100%"  "background-repeat: no-repeat;"  



## 
## Created FLASK_APP variable in the cli
## Set envirion variable
## $export FLASK_APP=blog.py
## 
## 
## Created templates dirctory with base & index living inside , being a child
## 
## 
## Created Config.y file to store the secret key, this will be imported
## 
## 
## 
## 
## Created Login Auth System with FlaskWTF, protection agianst vunrabiltys, with login.html
## Login Auth System working with validation in place thanks to flaskWTF
## 
## Created views in my routes
## 
## Creating Database for users & Post & followers with SQLACHemy
##  & falsk-Migrate with one to one , many to many, many to one, one to none, relationsips
## 
## Created form class & form model
## 
## 
##
## 
#### Migrate Workflow
## git add .
## git commit -m "Trying to flush out posts problem"
## git push origin master
## flask db migrate
## flask db upgrade
## flask db downgrade
## flask db current 
## flask db history 
##  
## Please edit configuration/connection/logging settings in '/home/ubuntu/workspace/migrations/alembic.ini'
## 
## 
## flask shell
## 
## 
## Creating user login subsystem with password hashig with Werzurg 
## 
## Created Register.html with rer hashing method in conjunction flask-login & UserMixin
## 
##  ?pybabel extract -F babel.cfg -k _l -o messages.pot .
## pybabel extract -F babel.cfg -k _l -o messages.pot .?
## Translation 
## 
##  pybabel init -i messages.pot -d app/translations -l es
##  pybabel compile -d app/translations
##  
##  pybabel update -i messages.pot -d app/translations
##  flask translate init LANG to add a new language
##  flask translate update to update all language repositories
##  flask translate compile to compile all language repositories
## 
## 
## 
## export MS_TRANSLATOR_KEY="api key from azure go,s here without the qoutes" in the cli while sister cli server is running
##
## import requests
## r = requests.get('https://api.microsofttranslator.com/v2/Ajax.svc/Translate?text= 
## como estas?&from=es&to=en', headers={'Ocp-Apim-Subscription-key': app.config['MS_TRANSLATOR_KEY']})
## 
## r.status_code
## 
## 
## 
## 
## 
## 
###### heroku 
##
##
## (env) clivenoonan:~/workspace (master) $ heroku apps:create book-of-hue
## Creating ⬢ book-of-hue... done
## https://book-of-hue.herokuapp.com/ | https://git.heroku.com/book-of-hue.git
## 
##
## Example
## (env) clivenoonan:~/workspace (master) $ git remote -v
## heroku  https://git.heroku.com/my-book-of-hue.git (fetch)
## heroku  https://git.heroku.com/my-book-of-hue.git (push)
## origin  https://github.com/90t/book-club.git (fetch)
## origin  https://github.com/90t/book-club.git (push)
## 
## 
## heroku addons:add heroku-postgresql:hobby-dev
## Creating heroku-postgresql:hobby-dev on ⬢ book-of-hue... free
## Database has been created and is available
## 
## Created postgresql-shaped-66481 as DATABASE_URL
## 
## heroku logs
## 
## 
## 
##
##
##<nav class="navbar" style="color:#666;" "font-family: "Source Sans Pro",Helvetica,sans-serif;">
##

## 
##
##
##
##
##
##
##
##

## 
##
##
##
##
##
##
##
##

## 
##
##
##
##
##
##
##
##

## 
##
##
##
##
##
##
##
##




