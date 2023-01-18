Imagify is a single page web application that allows the user to generate art inspired by a song selected through Spotify's Web API. This app is designed in Webflow, with the frontend written in HTML, CSS, and Javascript, and deployed via Heroku. The backend uses Node.js framework.

It makes use of Spotify's Web API for track information, including album art and track meta data. Lyrics will be webscraped. This information is then handed over to OpenAI's API to cherry-pick key words from the lyrics, describe the track's mood based on the meta data, and then combines the two results into a text prompt. These results are assimilated into a single request to OpenAI's image generator API. Viola!

# TODO
[] Design SPA in Webflow
[] Create backend with Node.js
    > Safe place for API Keys
    > Handle the API requests/responses
[] Integrate Spotify API
[] Create or find lyric webscraper
[] Integrate OpenAI
    > Install Node.js library
[] Deploy to Heroku

# ACTIONS
MVP should be able to...
[] Search for + select a track from Spotify's library
    > Requires user input
    > Will send an API request
    > Response will be processed
[] Webscrape for song lyrics
    > Uses artist name and song title
    > Returns lyrics
[] Identify key words in lyrics
    > Finds specific types of words (noun, verb, etc)
    > Selects words used most frequently
    > Not sure yet how I will do this lol!
[] Create a MadLibs sort of prompt using lyric content
[] Send prompt to OpenAI
[] Allow user to save resulting image
    > File name should include track title and artist name