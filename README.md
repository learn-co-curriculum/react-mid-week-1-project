React Mid Week 1 Project
========================

## Introduction

Your product manager has decided that the best way to deal with pesky clients is to tell them to Fuck Off! They have tasked you and your team with the job of creating an internal service for staff to use to tell clients to Fuck Off! Luckily, you found a great API to help you get started: [Fuck Off As A Service](https://www.foaas.com/)!

## Deliverables

1. Form with the following fields:
    - [ ] Dropdown => picks the endpoint to hit
    - [ ] Input => for your name = `:from`
    - [ ] Submit button will search the API.
    - List of these specific endpoints will be given.
    - Make this a _controlled form_.
2. Display your API search results:
    - When you have no search result:
      - [ ] P/H1/etc. => display some instructions
    - When you have a search result:
      - [ ] P/H1/etc. => display the insult
      - [ ] Button => to save insult; clicking this should save your insult to an array
      - [ ] Button => to discard insult; clicking this should clear the result
3. Display your saved insults:
    - [ ] table => list of saved insults
4. Add users to email insults to:
    - [ ] Form with two inputs:
      - [ ] Input: their name
      - [ ] Input: their email address
      - [ ] Submit button will save these people in an array.
    - [ ] table/list/etc. => list of `emailto:` links that show the name but will mail to their email address
5. Select and email your insults:  
    - [ ] checkbox => add a checkbox next to each insult
    - [ ] Update your `emailto:` links such that the opened email form will autofill the `subject` and `body`; the `body` should have all of the checked off insults.
    - [_About `emailto:` `subject` and `body`_](https://stackoverflow.com/questions/4782068/can-i-set-subject-content-of-email-using-mailto#)
    - _Hint:_ Think about how you structured your `state` for storing the `insult` array. What's a good data structure for this? What do you need to keep track of now?
6. Have fun!!!

## Setup

Make a new repository for your group. Then add your backend and frontend to the repository as follows so everything is in one repo:

### Backend

This is the backend you'll be using to make your API calls: [FOAAS](https://www.foaas.com/) ([Github Repository](https://github.com/tomdionysus/foaas))

From your repository's root folder:

```sh
git clone https://github.com/tomdionysus/foaas.git
cd foaas
npm install
npm start
```

This will run the server on `http://localhost:5000/`.

**API Endpoints**

All of their API endpoints are listed on the website. The only one's we are concerned about are the ones provided for you in `endpoints.js`.
- All endpoints are `GET` requests.
- You need an `Accept` header of type `application/json`.
- They should be a get to the `url` defined in each object inside the array.

### Frontend

You will be making a React app from scratch. A reminder of how to do so:

From your repository's root folder:

```sh
create-react-app your-app-name
cd your-app-name
npm start
```

Once setup, copy over `endpoints.js` into your `src` folder. (**Don't forget this!!**)
