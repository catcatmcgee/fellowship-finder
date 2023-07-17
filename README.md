# Fellowship Finder

Fellowship Finder is a web app that allows users to find and meet people with similar interests in games.

The app allows users to create profiles, filter through other users based on interests and meetup logistics, add friends, and plan events. Fellowship Finder is meant to provide a platform for people to make friends with shared interests and streamline the process of organizing tabletop sessions.

## Setup
1. If you don’t have Node.js installed, [install it from here](https://nodejs.org/en/). (We used Node v18.16.0 and have not tested on other versions)

2. Clone this repository and navigate into the project directory

3. Install the requirements

```
npm install
```

4. Make an account or sign in the [Google Cloud](https://cloud.google.com/).

5. Navigate to the [credentials section](https://console.cloud.google.com/apis/credentials?project=massive-concept-383720) of the API's and services.

6. Create a OAuth client ID credential. Name it whatever you like. For *Application type* select Web application. 

7. Add the following Authorized origins:
```
http://localhost:8080
```
```
http://localhost:3001
```

8. Add the following redirect URI's:

```
http://localhost:3001/auth/google/redirect
```
```
http://localhost:8080/auth/google/callback
```


9. Make a copy of the config/keys.js file by running this command.

    On Linux or Mac: 

```
cp config/keys.example.js config/keys.js
```

    On Windows:

```
copy .config/keys.example.js .config/keys.js
```

10. Inside of the new config/keys.js file, replace the empty strings with your new Google Oauth Client ID and Client secret. The session cookieKey can be named whatever you like. 

11. Run the app

```
npm run dev
```


12. You should now be able to access the app at [http://localhost:7000](http://localhost:7000)

## Designed by @party-cubed:
  *Emmy Bishop*
  @emmy-bishop

  *Kalypso Homan* 
  @catcatmcgee

  *Marvas McCladdie*
  @MarvyWarvy

## Stack

Node: v18.16.0

Database: mySQL

ORM: Sequelize

Deployment site: AWS

Server: Express

Authentication: Passport and Google auth

Client: React

Styling: Material-UI

Project management: Trello


## License
This project is licensed under the VERYREALVERYSECURE License.

