# Typescript Geolocation

Web App - Typescript tuto project

## Summary

The app randomly generates a user and a company. Every user and a company has a location property attach to them, locaiton which is used to show as markers on a google map inside the browser

## Run

To see the app running on a browser a library called parcel-bundler is used.
So:

1. Install `$ npm install -g parcel-bundler`
1. Run `parcel index.html`

The parcel library is in charge of reading the script tag in the html, identify the ts, convert it to a js file and attach again the js bundle inside the html.
