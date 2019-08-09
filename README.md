liri-node-app
Introduction
LIRI is like iPhone's SIRI. However, while SIRI is a Speech Interpretation and Recognition Interface, LIRI is a Language Interpretation and Recognition Interface. LIRI is a command line node app that takes in parameters and gives you back data.

Setup
Clone the repository

Run npm install, and the following packages should be installed:

Node-Spotify-API

Axios : This module will be used to get the IMDB and BandsInTown API data

Moment

DotEnv

Create a .env file in the same directory as the rest of the files. In the .env file should be:

'# Spotify API keys'

'SPOTIFY_ID=your-spotify-ID-here'

'SPOTIFY_SECRET=your-spotify-secret-here'

liri Available functions:
concert-this

spotify-this-song

movie-this

do-what-it-says

Running the following commands in your terminal will do the following:
node liri.js concert-this 'concert or band name'
This will show the following information about each event to your terminal/bash window:

Name of the Venue

Location of the Venue

Date of the Event

node liri spotify-this-song 'song name'
This will show the following about the song in your terminal/bash window:

Artist(s)

Song Name

Album of the Song

Song Preview Link

If no song is provided then the song "The Sign" will be searched instead

node liri.js omdb 'movie name'
This will output the following information to your terminal/bash window:

Title of the Movie

Year the Movie was Released

The IMDB Rating

Country the Movie was made in

Language the Movie is in

Plot of the Movie

Actors in the Movie

The Rotten Tomatoes Rating

If no movie is provided then the movie "Mr. Nobody." will be searched instead

node liri.js do-what-it-says
The program will take the text inside of random.txt and use it to call the first command with the second part as it's parameter

Currently in random.txt, the following text is there:

spotify-this-song,"I Want it That Way"

Screen Shoots from BS

This would call the spotify-this-song function and pass in "I Want it That Way" as the song.
PS C:\Users\cmurillo\Documents\Class\homework 10\liri-node-app> node .\liri.js spotify-this-song always
this is loaded
--------------------------------------------------------------------
Artist(s): Chance the Rapper
Song Name: I Got You (Always and Forever)
Album Name: The Big Day
Preview Link: https://p.scdn.co/mp3-preview/8f01573bee831ccace2d4b0da79d1ad6bdb6c4ca?cid=4fe42aa903974f3bb802c75e21618613
--------------------------------------------------------------------
Artist(s): Mariah Carey
Song Name: Always Be My Baby
Album Name: Daydream
Preview Link: https://p.scdn.co/mp3-preview/b1e31095de6722f08830226adaeaf91d54654bc5?cid=4fe42aa903974f3bb802c75e21618613
--------------------------------------------------------------------
Artist(s): Lady Gaga
Song Name: Always Remember Us This Way

PS C:\Users\cmurillo\Documents\Class\homework 10\liri-node-app> node .\liri.js movie-this  avatar
this is loaded
--------------------------------------------------------------------
Movie Title: Avatar
Year of Release: 2009
IMDB Rating: 7.8
Rotten Tomatoes Rating: 82%
Country Produced: UK, USA
Language: English, Spanish
Plot: A paraplegic Marine dispatched to the moon Pandora on a unique mission becomes torn between following his orders and protecting the world he feels is his home.
Actors/Actresses: Sam Worthington, Zoe Saldana, Sigourney Weaver, Stephen Lang




