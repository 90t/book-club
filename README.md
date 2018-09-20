[![Build Status](https://travis-ci.org/90t/book-club.svg?branch=master)](https://travis-ci.org/90t/book-club)
# CodeNote flasks micro services
### The inspiration for this project came from studying python since 2016 before I attended IT & Maintenance in CoCC ,
#### this python class was of a night time in CoCC,
- Since then moving on to SoloLearn on my phone ,then Code institute with SoloLearn agian & then syllabus1_LMS1 & syllabus2_LMS2(cloud9)
- At this stage I was really looking forward to building something real in web development with the flask framework I had heard so much about
- Flasks Micro services was what I was really interested in , I was setting out to incorporate & learn microservices to speed up, improve, &
- build a website
- that could match the mern stack , the mean stack, django , this how ever is a long term goal as I am very pleased on how far I was able to
- push the development
- of this website
- I wanted to see if I could develop a messaging system without having to leave the flask eco system
- Creating Database for users & Post & followers with SQLACHemy
- A driver behind the conception of this project is the one to many, & many to many database relationsip of the followers
- For this task I would need a database, this was a key feature that I needed to explore & my application would depend on it 
- I also wanted to explore Flask-SQLAlchemy, the orm which allows a dev to programme a database
- Another key driver behind this project was idea of building a fullstack application with flask & cloud9, this was of course a challenge


## UX
 
The style of this website is very minimil, with a small bit of inline styling, this was down to the fact I wanted to focus on fuctionalty
- The nav bar is white to match the rest of the page , this is my attempt to bring the website together, with the hover of the links coming from
- the defualt styles from FlaskBootStrap, I also restyled the color of the navbar links , this had a massive effect on such a plain interface
- Changing the mail notification icon was also a massive changer in the over all aesthetics of my application
- When arriving on CodeNote you will be met with a sign in page where the user has the option of signing into the application
- or registering a new account, the user also has the option of email recovery & a remember me checkbox, since this is the first page
- the user will see,
- Once the user has logged in, the user will be greeted with a message with there user name that they had just signed with
- The main CodeNote/posts/forum/ page is accessible through the navbar with the link CodeNote,
- The users mail, logout , profile , & search engine are also availible on this page  


Once on this page the user has the abitly to go home to his own posts/notes page or the user can go staright to his profile page or
- straight to his own mail page, 
- This page the main page , is also the page with all the users ,here the user can select another user & view there profile
- When hovering over a user name a popup box will appear with details about the user such as There user name , there most recent
-  Post/CodeNote, & 
- the last time there were seen aswell as the date & year
- Also in this pop up box users can observe how many followers a user has & how many there are following
- The pop up box is also interactive, a user can select a user name & be transported to there profile page or a users profile page 
- They can also follow or unfollow a user by accessing there profile page , but the user can not follow themselves
- The users profile page is also the page where other coders/users can private message another coder/user
- The home page is the page where users can leave a Note/Post & then this Note/Post will show up on the CodeNotes page, & there own home page
- This application can come in very handy indeed , if 2 developers were working on a project ,
- they could very easliy communicate with one another through the use of the mailing system 
- with little to no distraction
- More devs on the note page or more team members could also join in & solve problems about there code & advise on going forward
- Where this application also would come in very handy is in a small business, or family business,
- This would give the all the team members access the communication to one another completly free of charge
- where this application can also be used is in a in house restaurnat communication system
 



###### Flask on cloud 9 venv setup python3

The setup for this project was similer Django but with slight variations 
- First I created a blank instance with an ubuntu server on cloud 9
- Then I ran the command sudo pip install virtualenv, this installed the virtualenv that comes bundled with the ubuntu server
- Next I created my venv with virtualenv -p python3 env <<<-----name of virtual enviroment
- My next task was to activate the virtualenv with  clivenoonan:~/workspace $ source env/bin/activate
- Since I had the majority of my project already built on a different ubuntu cloud workspace server, I copy & pasted my requirements.txt
- file into my new project
- Next I ran the command pip freeze  -r requirements.txt
- Also pip install --upgrade -r requirements.txt, this updated & synced my packages to my project folder
- Finally I started my development folder, with the command env/bin/flask run --host=0.0.0.0 --port=8080
- After settting my env vars in heroku , when evr I neede to workon my project after I set the vars , I would have to run export
- FLASK_APP=blog.py
- If I wanted to workon my project with debug mode on I would run the command  export FLASK_DEBUG=1 <<---ON
- To turn debug off for deployment I would run the command export FLASK_DEBUG=0 <<-- OFF
- To run my local debug built in email server I would run the command python -m smtpd -n -c DebuggingServer localhost:8025 in a new terminal,
- with my bash
- terminal also running



## Features

## BluePrints 
- blueprints are a brillant feature to the flask framework, a good example of this is this project , I fully indented to build my
- project with a
- blueprint structure , for large applications, even tho this is only a meduim to a small application, blueprints had a massive effect
- on the organisation
- of my project
- In Order to achieve this I created a main / auth/ errors BluePrints inside of my app folder
- I then registered my BluePrints in my __init package file
- This is similer to Django each BluePrint is like there own app 

## Enviroment Variables
- In Order to automate my env vars I configured a .env file , this technique is used by many frameworks such node.js, Django
- I also needed to install the dot.env exstention with the pip package manager with the command pip install python-dotenv
- To connect my python package with the alias of dot.env in my config.py file I created this alias in my config class
- Next I needed to create my.env file this is where I stored my SECRET_KEY, MAIL_SERVER, MAIL_PORT, MS_TRANSLATOR_KEY, variables
- while my application was running I saved my .env file , this process imports my varibles from me to my appliaction


## The Requirements.txt file
- To keep my packages up to date & in sync with my 3 repos GitHub/Heroku/Local
- I adopted the requirements.txt techniuqe , I updated & synced my package requirments with the pip package manager with the command pip install
- pip freeze > requirements.txt this essentially dumped all my projects dependencies to my requirements.txt, Heroku will heavily depend on this file in the
- deployment stages of my project
- When future up dates to my project are nessacary , I can then reproduce my project with just my requirements.txt file , aswell another developer


### Web Forms & Flask-WTF
- To work & set up my forms I had to have venv activated & I had intitiatd the project with my FLASK_APP=blog.py
- & ran my server 
- this was the only I could get cloud 9 to run the server
- A core component of my application is webforms, I accomplished this with Falsk web forms & the Flask-WTF exstention package which I installed with pip
- the python package manager, while my venv was active with the command pip inatll flask-wtf

### Flask-Babel
- flask babel & the message.pot workflow was a challenging micro service to intergrate in to my project
- In order to get up & running I needed install flask babel, I again installed this database python package with the pip package manager
- with the command pip install flask-babel
- I then again imported flask-babel package from flask & created an instance with an application as an argument in my mother __init_.py
- Next was to update my config.py to support my applications langauge prefrences
- In order to use my flask babel package I first needed to create a babel.cfg file with my jinja templates & python paths programmed
-  to parse
- My next command was to extract my languages with the command pybabel extract -F babael.cfg -k _l -o messages.pot 
- POT or otherwise known as portable object template
- To compile my this file to a format so babel can compile at runtime
- To achive this I used the babael package again & ran the command pybabel compile -d  when running this command in your own project
- this is where you need provide your top level directory path
- After compilation babel will generate a new messages.po, this is the file that will contain my langauges translations
- To extract any new langauges I just needed to run the command pybabel extract -F babael.cfg -k _l -o messages.pot .
- This command once again extracted my text , for the changes to take effect to my babel workflow, I needed to update
- I used the similer command pybabel update -i messages.pot -d app/transaltions
- This command updated my pot files with any new langauges that I decided to add to my project



## Translations & Ajax
- With accessibilty as the main point of this feature , language translation on each post would bring this application international
- With the transalate button acting as my hook to my Micrsoft Azure API Key
- I used Ajax to asynchronously update my translations
- To ahcieve this I neededd to create client side js scripts
- Next task was to set my MicroSoft Azure Translate Service API key
- This is a free thier, perfect for testing
- Next I had to add a translator resource in my Azure portal
- After retreiving & copying my API Key 
- I next I installed guess_language_spirit & requests
- I achieved this with the python package with the pip package manager
- I ran the command pip install guess_language_spirit  requests
- My next task was to update my models in my project models to take effect to my database, I needed to run a upgrade command,
- flask db upgrade became a part of my migration workflow 
- I then worked with the commands 
- flask db migrate
- flask db upgrade
- I next updated my routes to match my models logic



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
##### git add .
##### git commit -m "Trying to flush out posts problem"
##### git push origin master
##### flask db upgrade
##### flask db downgrade
##### flask db current 
##### flask db history 
- to manage & observe my database
- to populate my tables in my database I worked in the python interactive shell , I entered this shell with the command
- python
- I also used flask shell , this eliminated the need to import my instance into my python shell everytime I wanted to manage my database
- I entered my flask shell with the command flask shell

### Followers & Posts Schema 
- The Schemas in my application are a one to many relationship
- With post ownership representing my one to many relationship
- My one to many relationship is modeled so one user can write multiple posts
- The follower Schema in my application is a many to many relationship
- This is why my followers table is the most complex
- With A follower user following many users aswell been followed by many users
- So I have many to many relatonships managed by ORM



### Followers
- To implement this feature in my project I needed to create my followers table in my modles.py
- Which will be mapped & managed with my ORM
- to create my first migration I used to command flask db migrate -m "just like git commit messsage ", just like git a message can be
- included in my migration
- for the changes in my project models to take effect to my database, I needed to run a upgrade command,
- flask db upgrade became a part of my migration workflow
- I then worked with the commands 
- flask db migrate
- flask db upgrade
- flask db downgrade
- flask db current 
- flask db history 





### Moment.js
- To convert time in the browser using javascript I used a library called Moment.js
- I again installed this package with the pip package manager with the command pip install flask-moment
- I then again imported flask-babel package from flask & created an instance with an application as an argument 
- Next added a Moment.js JavaScript Block to my base template
- I then updated my jinja template code to reflect my changes , this was to show moment.js timestamp for the profile user
- Also I updated my posts jinja templates, this was to insure all pages that will dispaly posts/notes wil display there time stamp




### Email Support 
- For password recovery & emails I used flask-mail 
- For password recovery  I used pyJWT
- pyjwt will be sending links that include secuirty tokens , this is where I needed my jwt python package
- With my venv active I needed to install flask-mail & pyJWT
- I again installed these packages with the pip package manager with the command pip install flask-mail pyjwt
- To initliase flask-mail, just like my similer micro services, I needed to import into my mother init.py package file
- I then again imported flask-mail package from flask & created an instance with an application as an argument in my mother __init_.py
- To test my builtin email server I ran the command python -m smtpd -n -c DebuggingServer localhost:8025
- This started a test email server succesfully, to configer my server to listen to my sister terminal
- I needed to set my ENV VARIABLE, I acheievd this with the command
- export MAIL_SERVER=localhost 
- export MAIL_PORT=8025



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
- I needed to include my jinja if statements in my base.html to define that if the message count is 0 there is nothing dispalyed
- My mail badge will appear only when there is unread message 
- In order to make my badge more dynamic I need to use js by using a jquery fuction that searches for an element that repesents the badge
- when jquery finds the element the css method is applied by changing the visibilty of the badge to visible when there is a message &
- not viisble when there is !not a message
- Next was to create my notification models , I used the payload_json for this operation
- because of this addition I also added a new model field to my main models.py to reflect my changes




## Technologies Used

- [Flask](https://docs.djangoproject.com/)
    - The project uses Django 2 for rapid web development, clean design & a pragmatic approach .

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
    
- [MomentJs](https://https://https://www.w3schools.com/)
    - The project uses **Js** to add interactivity & to interact with stripe.
        
- [LightHouseChromeExstention](https://chrome.google.com/webstore/detail/lighthouse)
    - The project uses **LightHouseChromeExstention** to test seo data & accsseibitly & best practices
    
- [validator.w3](https://validator.w3.org/)
    - The project uses **validator.w3** to test seo data & accsseibitly & best practices
    
- [jigsaw.w3](https://jigsaw.w3g/)
    - The project uses **jigsaw.w3** to test validation of CSS3
    - also to test seo data & accessibility & best practices

- [Jinja.Templates](https://jigsaw.w3g/)
    - The project uses **jigsaw.w3** to test validation of CSS3
    - also to test seo data & accessibility & best practices

- [MARKDOWN](https://https://www.w3schools.com/)
    - The project uses **jigsaw.w3** to test validation of CSS3
    - also to test seo data & accessibility & best practices



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

## Translations Testing
- To test my API Key
- I first needed to assocaite my application with my MS_TRANSLATOR_KEY
- I achieved this by exporting another Enviroment Variable
- I achieved this with in my terminal , with my venv active I ran export MS_TRANSLATOR_KEY="api key from azure go,s here without the qoutes" in the cli while
- sister cli server is running
- Now my key is in my env my Next task was to update my projects config.py
- Flask Shell was next to test my api in my terminal
- I achieved this with the command flask shell
- My earlier installation of the python package requests will now come in to play in my apllication with a get request to microssoft for api validation










## Translations Testing In My Terminal
- First I needed obtain my microsoft url in my portal documentation
- In my terminal with my python flask shell active I first ran the config command form microsoft
- 
- In my terminal with my python flask shell active I first imported my requests
- With the command
>>> r = requests.get('https://api.microsofttranslator.com/v2/Ajax.svc/Translate?text= 
como estas?&from=es&to=en', headers={'Ocp-Apim-Subscription-key': app.config['MS_TRANSLATOR_KEY']})
- I then needed to import requests
>>> import requests
- I then needed to run
 r = requests.get('https://api.microsofttranslator.com/v2/Ajax.svc/Translate?text=hola como estas?&from=es&to=en', headers={'Ocp-Apim-Subscription-key': app.config['MS_TRANSLATOR_KEY']})
 - Next was check my status code for my get request with this code
 >>> r.status_code
 - This was because I stored my request in my r variable
 200
 - the final task was check my contend to verify the translation was succesfull
 - I did this with r.content command in my python flask shell
 >>> r.content
 b'\xef\xbb\xbf"Hi, how are you?"'

 ##### Success
 - [TranslationsTestingInMyTerminalScreenShot](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Translations/translator_api_proof.PNG)
 - [TranslationsTestingInMyTerminalScreenShot](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Translations/translator_api_proof2.PNG) 










 ## Testing
 ### jwt testing 
- To test my email in my terminal instance with my jwts 
- to test my email I imported my flask app Message instance into my terminal session, from here 
- I ran the command 
flask shell
>>> from flask_mail import Message
>>> from app import mail
>>> msg = Message('test subject', sender=app.config['ADMINS'] [0], recipients=['clivenoonan93@gmail.com'])
>>> msg.body = 'text body'
>>> msg.html = '<h1>HTML body<h1/>'
>>> mail.send(msg)
- [MyTestEmail](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/email_proof.PNG)
- I then updated my email.py methods & my jinja templates 
- next was to update my routes
- After my testing was complete I updated my routes to reflect my changes, my translate route







### jwt
- To use tokens in my emails I needed to base my structure on the Jason web token specification
- With this method I could create secure tokens that connot be forged according to jwt standards
- These jwt tokens are crypyographically signed , according to jwt standards, tampering with the data that jwt handles the data renders
- this signature invaid , this inturn rejects the token
- This whole process is controlled by the famous algorithm='HS256')
- With this package I generated hash tokens
- With this command I could verify & test the secuirty my applications email
- I achieved this by once again importing my jwt package into my flask terminal instance in my cloud9 ide with my venv active 
- to test my email secuirty I imported my flask app Message instance into my terminal session, from here 
- I ran the command 
flask shell
>>> import jwt
>>> token = jwt.encode({'a' : 'b'}, 'my-secret', algorithm='HS256')
- Next I needed to print my token , I acheived this with the command
>>> token
b'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhIjoiYiJ9.dvOo58OBDHiuSHD4uW88nfJikhYAXc_sfUHq1mDi4G0'
- [MyTestjwt](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/token_proof.PNG)
- Next I needed to verify my token,  I acheived this the commands
>>> jwt.decode(token, 'my-secret', algorithms=['HS256'])
>>> {'a':'b'}
- I then updated my models.py with my jwt decoding







### jwt testing password & email recovery part2
- to test my tokens I started a new flask shell session
- I ran the command 
flask shell
>>> u = User.query.get(1)
>>> u
<User CliveNooNAnBCliveNooNAnBFRase>
>>> u.get_reset_password_token()
'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyZXNldF9wYXNzd29yZCI6MSwiZXhwIjoxNTM3MjMwMzM2LjAxMTIyMjZ9.LqZvPtaWMXfH-ycjho3AtKbWPkHhUPe01f6V7xMDILU'
>>> 
- Verified 
- <User CliveNooNAnBCliveNooNAnBFRase>
- [MyTestjwtVerified](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/token_proof2.PNG)

- Next task was to update my forms.py & my jinja templates

### jwt testing password & email recovery part3
- To test my newly created email & password recovery feature I started my debugging server once again with the command
- python -m smtpd -n -c DebuggingServer localhost:8025
- Next I went to my application which was running a in my cloud9 instance
- On the main interface where a user logs in, the first page the user is greeted with I filled in the relevent details to recover my password
- [MyTestjwtVerifiedPasswordRecoveryDearCoffe](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/password_recoveryDearCoffe.PNG)
- [MyTestjwtVerifiedPasswordRecovery](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/password_recovery.PNG)



 ## User Testing   


##### USER1:
#### User1:David
- Clicks the saved tumbnail he has saved on his sony smartphone, he connects to his favourite CodeNote site, he has just read a very interesting article about a
- dashhboard website that compares plotly & d3, he has his link copied to his clipboard in his paste , he doesnt want to bookmark it , this is because he has so
- many bookmarks, he is beginning to loose all that on the go information, so he pastes the link into his CodeNote socail media home page, from here can comeback &
- check the date & time without any interuption or getting sidetracked along the way,
- just before he leaves he sees his mail box has 1 message , he checks his mail page,& see,s he has a message from Coffe, he reads the message & decides that he
- will reply,
- When logging out of his account, he never clicked the remember me button, User1:David is constantly clearing the storage in his phone , must be from all the
- bookmarks,
- He hasnt posted a note in a while, his popup profile box told him today, so he forgot what password he signed up with
- When User1:David arrives home he decides to have a look at that data website, as he proceeds to login, he reliases he cant remeber his passsword
- He selects the recover password option on the signinn page
- After reseting his password he checks the main codepost page & sees that his coder buddy has left a codenote in spanish
- He presses his translate button next to the post that coffe posted at 4:30,
- When User1:David was about the private message User2:Coffe back, he noticed a code post & clicked on the users profile, after reading that the user is a coder
- setting up his own coder dojo he decides to follow the user,
- After reading the coder dojo entusiaists profile User1:David decides to update his profile to reflect his coding expierence

##### Test1 User1:David ( True/False )
### Was User1:David able to recieve a message form User2:Coffe?
# True
- [USER1Testingmessage](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidWithOneMessagereplyFromCoffe.PNG)

##### Test1 User1:David ( True/False )
### Was User1:David able to send a message to User2:Coffe?
# True
- [USER1Testingmessage](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidWthMultipleMessageInboxFromCoffe.PNG)


##### Test1 User1:David ( True/False )
### Was User1:David able to complete a codenote/post to his main profile home page
# True
 - [USER1Testingpost](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidWthMultipleMessageInboxFromCoffe.PNG)



##### Test1 User1:David ( True/False )
### Was User1:David able to complete a codenote/post to his main profile home page & did the codeNote/post
### showup on both the homepage & the main codenote/post forum page
# True
 - [USER1TestingcodeNote/post](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidsPostMainPage.PNG)




##### Test1 User1:David ( True/False )
### Was User1:David able to recover his forgotten password  & setup another thru the use of email & hyperlink email in his email inbox?
# Inconclusive
 - [USER1Testinghyperlinkemail](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/password_recoveryDearCoffe.PNG)
 



##### Test1 User1:David ( True/False )
### Was User1:David able to follow the dojo entusiaists(mark) profile ?
# True
- [USER1Testingmark](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidViewingMarksProfileFollowingButNotSentMessage.PNG)


##### Test1 User1:David ( True/False )
### Was User1:David Succesfull In His search ?
# Falsh
 - [USER1Testingprofilesearch](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/Tokens/password_recoveryDearCoffe.PNG)








##### User2:Coffe
- User2:Coffe is rushing on the way to the biggest presentation of her career mabey even her life, she hurtles off the bus fresh into the blanket rain,
- In the mist of the panic she looses her wits & forgets about the rain, but more importantly, she forgets about the note book under her arm
- when she finally grabs the door as she arrives in the doorway of her campus, the notebook sails to the ground, she thinks to herslef thank god that wasnt my
- tablet, then I would of been up the creek & I havent had a paddle in years,
- Then she felt the uneasy feeling of her menthors dissapionted glare, the tought of her dragging him away from his studys for some break thru, the cheek of
- the girl , I mean she is a genius but , come on!
- This feeling came form the soaked note pad glaring up at her like her menthor, 
- The biggest break through of her career & she is sunked by the old faithfull Irish blanket rain,
- next she see,s her menthor briskly striding towards her,
- But wait she ponders for a flash & releises she posted her break thru to david in a private message, 
- 000000000000.9th of a second later, her menthor asks her in very smirk voice , "Well Coffe, whats this break thru you have been annoying me about, you know
- I was trying convince the board to let you..... " finishing his sentance would of beeen hard at this point with his jam firmly planted on the ground,
- He gasps, " I cant believe it, you did it , you solved the formula"
- mentor says to User2:Coffe, "All this time all I thought you were doing was drinking coffee, tell ya what send it on to me & while you at it get me the
- name of that developer of that code/post application"
- User2:Coffe replys " No problem, if you go to his profile page you can follow him & message him, I mean after all this Nasa"
- mentor replys " & Coffe , well done I knew you had it in you"
- User2:Coffe replys " gracious "



##### Test1 User2:Coffe ( True/False )
### Was User2:Coffe able to recieve a message form User1:David?
# True
- [USER1Testingmessage](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidWthMultipleMessageInboxFromCoffe.PNG)


##### Test1 User2:Coffe ( True/False )
### Was User2:Coffe able to send a message to User1:David?
# True
- [USER1Testingmessage](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingDavid/DavidWithOneMessagereplyFromCoffe.PNG)

##### Test1 User2:Coffe ( True/False )
### Did User2:Coffe badges & message number ount on there main page 
# True
[USER1Testingprofile](Linkhttps://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingCoffe/UserTestingShowingCoffe%26DavidsProfile%26MessagesBadgesCoffesInboxWithMessagesFormDavids.PNG)



##### Test1 User2:Coffe ( True/False )
### Was User2:Coffe able to complete a codenote/post to her main profile home page
# True
 - [USER1Testingpost](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingCoffe/CoffeWithOnePostToMainPage.PNG)



##### Test1 User2:Coffe ( True/False )
### Was User2:Coffe able to complete a codenote/post to his main profile home page & did the codeNote/post
### showup on both the homepage & the main codenote/post forum page
# True
 - [USER1TestingcodeNote/post](https://s3-eu-west-1.amazonaws.com/codenote-proof-screenshots/messagingCoffe/CoffeWithOneProfileToMainPageMoment.Js.PNG)



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

## Bugs

##### Email
- To integrate Email password recovery into my application I used flask mail & jwt tokens for incryption
- I did have a succesfull recovery of an email through the use of pasting the url I recieved in my testing of this feature
- I have yet to determine if Another outside of my network can achieve the same 
- Seemingly it is more diffucult than you think to convince users to signup for a social messaging application

##### Translations
- The transaltions feature of this application, was by far the most difficult work flow tp master
- I am convinced to problem lies in my compileing of my ready made spanish messages.pot file  
- I will be looking to this bug & when I have it resolved I will update this bug notice


##### redis
- When installing redis I had a succesfull installation & I was succesfull in starting a redis server in a sister terminal
- I was not succesfull in connecting to my server for testing
- 

### Elastic Search 
- To integrate Elastic Search into my flask application I needed install it on cloud9 , I had an installation failure here also


## Deployment

- The stages to deploy this project were very ordered & structured,
- first I needed to make sure I had an up to date version of HerokuCLI
- Once established I proceeded to login to my heroku account in my cloud9 bash terminal
- With my project all ready under source control I reinitilised my git repo with git init 
- My Next task was to create an app with a unique name from the HerokuCLI with the command heroku apps:create 
- With my new app created I recieved my new heroku git address/url 
- I clarafied my new remote address with the command git remote -v 
- To clarafai my app creation I checked my heroku cloud managment console once satisfied I proceeded 
- Heroku,s ephemeral file system dictates that the file storage is not permanant, because of this I used the technuigue of provisioning a postgres database on my
- heroku platform
- I achieved this with the HerokuCLI by running the command heroku addons:add heroku-postgresql:hobby-dev , this gives me the free thier , the excate same as
- creating from the heroku cloud managment console
- this task attached a database url connection & set the env varaiable to DATABASE_URL , this url acts as a pointer when I deploy my application to my new
- postgres database

## Deployment Stage2

- Next task in deployment was to update my requirements.txt with the package psyscop2 & gunicorn
- psyscop2 is the postgres database driver sql depands on this driver when you connect to a postgres database with heroku as the hosting platform
- I also added gunicorn , this package is required to connect to heroku server,
- next I needed to freeze my requirements to make sure all my packages are updated & in sync
- Procfile was next up , I created this file in the top level of my project folder on cloud9 & then added the relevent values to tell heroku
- what type of app is being served
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
## My Application looks amazingly responsive across all screen sizes this is mainly down to the Flask Framework & FlaskBootStrap

## VERSION CONTROL

- The  project folder lives at this address
  [github](https://github.com/90t/book-club) <------ THIS IS THE LIVE PROJECT FOLDER
- [heroku](https://git.heroku.com/book-of-hue.git) 
- [origin](https://github.com/90t/book-club)



## How to set up this project Locally or on cloud9
- If you want to setup this project on cloud 9 you can clone this repo & follow the setup instructions in the beginning of this file for cloud9
- If you get stuck leave a codenote on my website, or you can private message me, & I will gladly help you out
- If you dont have cloud9, then there is number of steps you will have to take in order to get this application from your workspace into your server
- flask & python environment,
- first you will have to have python3 installed on your pc/laptop/machine/computer
- next you will need git installed on your pc/laptop/machine/computer to clone my workspace from github
- next up you will have setup your venv, there are numerous workflows to guide you on this topic
- The reason I am not providing a more broader explanation on how exaclty how to do it is
- You will 100% find your own workflow, wheather it with the pip installer, the pip wrapper
- You will soon become a custom to creating venv,s in seconds
- Always use venv,s in your python projects not just flask
- For the sake of going through the task of mastering the workflow, it will be way more worth than your time
- It will save you endless hours of debugging & confusion to why your packages are conflicting with each other,
- This will happen if you just run , test , serve python projects in your workspace !without a venv
- Learning to setup a venv from & inside your terminal is essenital, which ever it maybe,
- The reason for this is , pycharm maybe amazing, but it also costs
- So when your pycharm subscription runs out, you wont be stuck not knowing how to correctly setup a venv in a fast & effecient manner
- If you are stuck you can check the resources I used to develop this application & they will get you setup in no time
- If you get stuck leave a codenote on my website, or you can private message me, & I will gladly help you out




## Credits
StackOverFlow

### Content
- I wrote all the content

### Media
- There no images in this website

### Acknowledgements
##### I didn't base my work off other code, I used only what I had learnt in syllabuss1/LMS1 & syllabuss2/LMS2(cloud-9) &
- [www.fullstackpython.com](https://www.fullstackpython.com/flask.html) 
- [flask.pocoo.org](http://flask.pocoo.org/docs/1.0/quickstart/) 
- [opensource](https://opensource.com/article/18/4/flask) 
- [www.digitalocean.com](https://www.digitalocean.com/community/tutorials/how-to-structure-large-flask-applications) 
- [www.ntu.edu.sg](http://www.ntu.edu.sg/home/ehchua/programming/webprogramming/Python3_Flask.html)

##### 19/09/2018 This is Clive Noonan , Code Initstute , Project Number4, Signing Off......