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
