Deplloy backend: https://backend-mern-calendar-app-production.up.railway.app/

# Auth:
/api/auth

# Events:
/api/events

## You can test the app with the next instructions:
Sending this in postman:
https://backend-mern-calendar-app-production.up.railway.app/api/auth/new (post)

body-raw-json:
{
    "name": "Yor Name",
    "email": "youremail@google.com",
    "password": "YourPassword"
}

then https://backend-mern-calendar-app-production.up.railway.app/api/auth to login: (post)

body-raw-json:
{
    "email": "youremail@google.com",
    "password": "YourPassword"
}

then https://backend-mern-calendar-app-production.up.railway.app/api/events: (post)
You need to put the token brinded in the login in headers with name: x-token

body-raw-json:
{
    "title": "Go to the gym",
    "start": 2, //date to start in JS
    "end": 100000, //date to end in JS
    "notes": "Do excercise"
}

then https://backend-mern-calendar-app-production.up.railway.app/api/events: (get)
You need to put the token brinded in the login in headers with name: x-token

body-raw-json
{
    "email": "youremail@google.com",
    "password": "YourPassword"
}

then https://backend-mern-calendar-app-production.up.railway.app/api/events/:idOfTheActivity: (put)
You need to put the token brinded in the login in headers with name: x-token

body-raw-json
{
    "title": "Title Update",
    "start": 7,
    "end": 700000,
    "notes": "Note update"
}

then https://backend-mern-calendar-app-production.up.railway.app/api/events/:idOfTheActivity: (delete)
You need to put the token brinded in the login in headers with name: x-token

body-raw-json
{
    "email": "youremail@google.com",
    "password": "YourPassword"
}
