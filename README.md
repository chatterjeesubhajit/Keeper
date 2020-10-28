#Keeper

## Website : https://sleepy-reaches-20043.herokuapp.com/

## Inspiration
I built this note keeping application while learning full-stack web development using M(ongoDB) E(pressJS) R(eactJS) N(ode.js) stack. This implementation helped me learn both backend and frontend development alongside deployment in production.

## What it does

 - This application is a light implementation implementation of Google Notes.
 - Users can login using Google Oauth2 authentication (using Passportjs-google-oauth2 strategy) or register with their manually with email.
 - Users can type in notes and view all previously saved notes as a listing. 
 - Users can change the styling of the notes as well, e.g. font color and background color for each note. This is achieved by maintaining a local state for each note and maintaining each note as a component, updating asynchronously.
 - Users can also modify their older notes , and also have a expanded view of their notes.

 
## How I built it

This application is built using :
- Node.js to build the backend server environment, along with ExpressJS framework to design the backend   application layer 
- MongoDB as database to store the user authentication details and the notes saved for each user.
    - A user schema which holds the user authentication credentials and also embeds an array of notes
    - A note schema which captures the note title, content and styling attributes, which is embedded into the user schema
- React (to check the client side code check `frontend` directory) library to design the client end interface which is the served as static build
- [Passport](https://www.npmjs.com/package/passport) library is used to implement the Google and Local OAuth2 authentication strategy

- React hooks useState, useEffect and useContext are used to effectively create a single page application through maintaining (useState) , refreshing (useEffect) and sharing data (useContext) amongst component states without props drilling

## Challenges I ran into and learnings
- This was my very first hands on experience with full stack web development. So, entire process was a steep learning curve for me. Following are the key challenges and learnings which helped me immensely in future projects:

    - Designing a schema for efficiently storing user data, without redundancy and to optimise data pulls from mongodb database
    - Setting up local and the third party oauth-2 authentication using passport-js library, which is very handy for most web development projects involving user authentication
    - Setting up a proxy connection (using `cors`) between react and backend express server environments during development was a challenging task since create-react-app bundle can't be modified too much without ejecting the bundle
    - Designing effective server side routing for authentication, note reading, creation, edit and deletion was a challenging task as well as a beginner
    - Maintaining a clean project structure through separating configuration, data models, main server and route components and setting up the connection between all of them has provided a good foundation for future projects

## Built With
- Node.js
- Express.js
- MongoDB
- React






    








