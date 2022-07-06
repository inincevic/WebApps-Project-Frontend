# Author
Ivan Ninčević

# Description
The idea of this web application is a simple guessing game, somewhat like Akinator, but for Pokémon.
There are two options for user experience: guest and registered user.

On the homepage, user can choose to use the application as a guest or to register/login.

If guest option is chosen the user is right away led to a webpage where he chooses attributes from dropdown menues or enters them themselves.
Two attributes, primary type and primary colour, are required and all others are optional.
After the attributes are entered, the backend is contacted and searches for a Pokémon withthose attributes in the database. Later on that Pokémon is displayed.

The register option alows someone to register as a user so that they are able to use all features available to registered users.
After logging in, they are able to see how many Pokémon they have guessed, what those Pokémon are and they are able to choose their favourite Pokémon.
They can also guess, just like guests can, but after they choose their guess is recorded on their profile. The Pokémon is added to the list and user's number of guessed Pokémon increases.


# History of PokéGuesserProject

The original idea for this project has been created by Ivan Ninčević and Anton Maurović back in 2017
That year the wrote a basic version of it in C++ using .txt files for simple comand line based guessing experience

In 2021 and 2022 Ivan Ninčević and Matia Perčić used this idea as a project for "Računalni praktikum 2"
That version of the code was written in Java, offered a GUI and used a database to store data

This version was witten by Ivan Ninčević alone.
The languages used are be HTML, Javascript and CSS.
HTML, Javascript and CSS are used in the frontend trough Vue.js. Backend is written in javascript and database is a NoSQL database hosted on MongoDB.


# frontend

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
