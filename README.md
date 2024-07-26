# Backend Deployment
The backend is deployed at: https://backend-mern-calendar-app-production.up.railway.app/

## API Endpoints

### Authentication
Base URL: /api/auth

### Events
Base URL: /api/events

## How to Test the App

You can test the app using Postman with the following instructions:

1. **Register a New User**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/auth/new (POST)

   Body (raw JSON):
   {
       "name": "Your Name",
       "email": "youremail@google.com",
       "password": "YourPassword"
   }

2. **Login**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/auth (POST)

   Body (raw JSON):
   {
       "email": "youremail@google.com",
       "password": "YourPassword"
   }

3. **Create an Event**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/events (POST)

   Headers: 
   - x-token: <your_token>

   Body (raw JSON):
   {
       "title": "Go to the gym",
       "start": 2, // JS timestamp for start date
       "end": 100000, // JS timestamp for end date
       "notes": "Do exercise"
   }

4. **Get All Events**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/events (GET)

   Headers: 
   - x-token: <your_token>

5. **Update an Event**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/events/:idOfTheActivity (PUT)

   Headers: 
   - x-token: <your_token>

   Body (raw JSON):
   {
       "title": "Title Update",
       "start": 7, // JS timestamp for start date
       "end": 700000, // JS timestamp for end date
       "notes": "Note update"
   }

6. **Delete an Event**

   Endpoint: https://backend-mern-calendar-app-production.up.railway.app/api/events/:idOfTheActivity (DELETE)

   Headers: 
   - x-token: <your_token>
