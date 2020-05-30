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

### Google Maps exaplanation

1. Go to https://console.cloud.google.com/
2. Create new project
3. Add library maps javascript api (library section)
4. Create an api key
5. Add script in html (before our js code inside src)

As we added google api in a script, it adds a GLOBAL variable in the window object called `google`. This is great but ts complains about not finding any definition of that namespace / variable.

## Tip: '|' operator

Imagine we have:the following:

```
// class User and Company with syntax
User: { userName: string; location { lat: long; lng: number } }
Company: { companyName: string; location { lat: long; lng: number } }
addMarker(mappable: User | Company)
```

That '|' operator will map each property of each class and see if the other class has that property.
If they do not share the property, that property will be discarde to use inside the function. In this case, only location will be "available" to use inside the function
