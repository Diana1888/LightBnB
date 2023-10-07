# LightBnB Project
A simple multi-page Airbnb clone that uses a server-side Javascript to display the information from queries to web pages via SQL queries.

Users can view property information, view their reservations, create listing and view their listings. They can also search property by city, minimum and maximum price per night, and by rating.

## Project Screenshorts

All properties - shows list of all properties
![All properties](https://github.com/Diana1888/LightBnB/blob/master/docs/allProperties.png?raw=true)

Create Listing - allows user to create property
![Create Listing](https://github.com/Diana1888/LightBnB/blob/master/docs/CreateListing.png?raw=true)

My Listings - allows to view all listings that belongs to user
![My Listings](https://github.com/Diana1888/LightBnB/blob/master/docs/myListings.png?raw=true)

My Reservations - allows to view all reservations made by user
![My Reservations](https://github.com/Diana1888/LightBnB/blob/master/docs/myReservations.png?raw=true)

Search function - allows to filter all properties by city, price per night and rating
![Search](https://github.com/Diana1888/LightBnB/blob/master/docs/Search.png?raw=true)

Search result 
![Search](https://github.com/Diana1888/LightBnB/blob/master/docs/search-result.png?raw=true)

## Project Structure

```
.
├── db
│   ├── json
│   └── database.js
├── public
│   ├── javascript
│   │   ├── components 
│   │   │   ├── header.js
│   │   │   ├── login_form.js
│   │   │   ├── new_property_form.js
│   │   │   ├── property_listing.js
│   │   │   ├── property_listings.js
│   │   │   ├── search_form.js
│   │   │   └── signup_form.js
│   │   ├── libraries
│   │   ├── index.js
│   │   ├── network.js
│   │   └── views_manager.js
│   ├── styles
│   │   ├── main.css
│   │   └── main.css.map
│   └── index.html
├── routes
│   ├── apiRoutes.js
│   └── userRoutes.js
├── styles  
│   ├── _forms.scss
│   ├── _header.scss
│   ├── _property-listings.scss
│   └── main.scss
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
└── server.js
```

* `db` contains all the database interaction code.
  * `json` is a directory that contains a bunch of dummy data in `.json` files.
  * `database.js` is responsible for all queries to the database. It doesn't currently connect to any database, all it does is return data from `.json` files.
* `public` contains all of the HTML, CSS, and client side JavaScript. 
  * `index.html` is the entry point to the application. It's the only html page because this is a single page application.
  * `javascript` contains all of the client side javascript files.
    * `index.js` starts up the application by rendering the listings.
    * `network.js` manages all ajax requests to the server.
    * `views_manager.js` manages which components appear on screen.
    * `components` contains all of the individual html components. They are all created using jQuery.
* `routes` contains the router files which are responsible for any HTTP requests to `/users/something` or `/api/something`. 
* `styles` contains all of the sass files. 
* `server.js` is the entry point to the application. This connects the routes to the database.

## Project Setup

`cd` to `LightBnB_WebApp` and use `npm install i` command to install dependencies.

`npm run local` command will start the web server.

Application will be running on http://localhost:3000

### Project Dependencies

   ```
   "bcrypt": "^3.0.6",
    "cookie-session": "^1.3.3",
    "express": "^4.17.1",
    "nodemon": "^1.19.1",
    "pg": "^8.11.3"


