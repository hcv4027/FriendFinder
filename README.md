# VealMatch's FriendFinder

Let us help you find that special someone you have been looking for. Take our survey, and watch as our application finds and then 
pairs you with someone of like mind!

## Live Link
 - https://vast-tor-46282.herokuapp.com/

## Usage

![screenshot_main](https://github.com/hcv4027/FriendFinder/blob/master/app/images/main.PNG)

Go to my homepage and take the survey. After submitting the survey, your matched friend will pop up.

## Requirements
- Use of `express`, `body-parser`, and `path` npm packages in the `server.js` file
- JavaScript files for routing (`apiRoutes.js` and `htmlRoutes.js`)
- Encapsultation is accomplished by using separate files for logic, matching friends, routing, and views
- GET and POST routes for serving HTML pages and API callshttps://murmuring-island-94264.herokuapp.com/
- Matching friends stored in a (`friends.js`) file.
- Calculate best match for user once survey is completed and return that match to the user
- 10-question survey to assess uniqueness of users

## Technologies Used

- Express.js
- node.js
- JavaScript
- jQuery
- HTML
- Bootstrap

## How it all works
- Our `server.js` file sets up the Express server, with a spoecific port number, the npm packages that need to be loaded, and also the routes needed.
- The HTML files (`home.html` and `survey.html`) display the front-end code (the homepage and the survey, along with their best match)
- Our 2 routing files (`htmlRoutes.js` and `apiRoutes.js`) handle the back-end logic (based on the request being made, the response that gets sent to the browser); the HTML routes display the survey and the homepage based on the URL that is accessed, and the API routes send back existing content in our server-side data or add new friends
- Best match is calculated by finding the friend with the minimal difference in scores and then sending that friend to the browser as a JSON object
- A modal pops up, showing the the best match to the person who just took the survey

- Here is an example of how Friends are stored:

```js
{
	name: "Chris",
	photo: "https://vignette3.wikia.nocookie.net/scooby-doo/images/0/0a/Chris.jpg",
	scores: [5, 3, 2, 1, 1, 2, 5, 1, 4, 1]
}
```
