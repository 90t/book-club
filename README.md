###### Flask on cloud 9 venv setup python3
###### Create blank instance of cloud9 ubuntu
## sudo pip install virtualenv
## virtualenv -p python3 env <<<-----name of virtual enviroments
## clivenoonan:~/workspace $ source env/bin/activate
## $ pip freeze  -r requirements.txt
## $ pip install --upgrade -r requirements.txt
## (env)clivenoonan:~/workspace $ 
## export FLASK_APP=blog.py
## env/bin/flask run --host=0.0.0.0 --port=8080
## export FLASK_DEBUG=1 <<---ON
## export FLASK_DEBUG=0 <<-- OFF
## python -m smtpd -n -c DebuggingServer localhost:8025

##  style="background-image: url('{{ url_for('static', filename='img/g.jpeg') }}" "height: auto;" "max-width:100%"  "background-repeat: no-repeat;"  


###### BookClub
## test222@gmail.com
## Username:
## Al
## Password:
## mynewflask2236vg

## test22522@gmail.com
## Username:
## Joey
## Password:
## mynewflask2236jko0vghh7dfhg

###### BookClub
## t@gmail.com
## Username:
## Jarvis
## Password:
## mynewflask2236vg

## Jarvisui@gmail.com
## Username:
## Jarvisui
## Password:
## mynewflask2236dfg


### Migrate Workflow
## git add .
## git commit -m "Trying to flush out posts problem"
## git push origin master
## flask db migrate
## flask db upgrade 
##
##
##
## Created App Package Module
##
##
##
## Created Routes to the app package
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
## export MS_TRANSLATOR_KEY="api key from azure go,s here without the qoutes" in the cli while sister cli server is runnings
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
## sET ENVIROMENT VARIBLE
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
##
##
##<nav class="navbar" style="color:grey;">
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




