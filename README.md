This is a note taking app server that provide several API endpoints.
It is a personal project to improve my back-end development skills.  

The original app took 4 days to develop as part of Lambda School's curriculum.  It used Postgres DB and had more features. It is deployed at Heroku (https://ed-notes.herokuapp.com/) with same endpoints specified below.

Using this app as a base, I modified to implement MongoDB and other features.



### to test site

Deploy URL is @@@@@@@@@


### Installation

To install the application in a local dev environment, run `yarn install` in the root folder as well as the client folder. Then, in the root folder you run `yarn server` and in the client folder you run `yarn start`.

### Tech Stack Rationale


#### Back End

**Solution:** Node, Express

- JavaScript on the front and back end
- Reduces server-side logic complexity -> faster development
- Minimalist and un-opinionated framework
- Performance and cross-platform coverage

#### Database

**Solution:** MongoDb

### Back-end API

##### GET /api/allnotes
Returns an array of all the notes of logged users.

##### GET /api/notes/:id
Returns an note of the id.

##### POST /api/addnote
Add a new note to DB
The content of new note is send as req.body in a format of
{
title : "title",
textBody : "notes"
}


##### PUT /api/notes/:id
Edit an existing note of the id. The content of edited note is send as req.body in a format of
{
title : "title",
textBody : "notes"
}

##### DELETE /api/notes/:id
Delete a note of the id

##### GET /api/search?query='query'
Returns those notes that matches query

End