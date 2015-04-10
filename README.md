App Engine application for the Udacity training course.

Live Url: http://exam-conf.appspot.com/

Design Choice:
very simple i copied and modified the conference schema to make my session so its really similar . A session 
is created from a parent key ( Conference )
for the speaker i went with a StringField so any name could be added!


Queries : describe 2 queries:

1:  Get all session available in the morning only and that last between 60-90 minute . 

2. Get all session with highlights about programming python

Problem query : cannot use 2 inequality in the same query.

solution : use 2 qiery, Query Session to find all session before 7 pm ( 19 ) and query session to find all typeofsession that doesn't equal workshop . with a for loop go through both query to find matching session returned and append them to a list. return the list.  


## Setup Instructions
1. Update the value of `application` in `app.yaml` to the app ID you
   have registered in the App Engine admin console and would like to use to host
   your instance of this sample.
2. Update the values at the top of `settings.py` to
   reflect the respective client IDs you have registered in the
   [Developer Console][4].
3. Update the value of CLIENT_ID in `static/js/app.js` to the Web client ID
4. (Optional) Mark the configuration files as unchanged as follows:
   `$ git update-index --assume-unchanged app.yaml settings.py static/js/app.js`
5. Run the app with the devserver using `dev_appserver.py DIR`, and ensure it's running by visiting your local server's address (by default [localhost:8080][5].)
6. (Optional) Generate your client library(ies) with [the endpoints tool][6].
7. Deploy your application.
