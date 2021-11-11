# BBC News Apps (iOS/Android) Coding Challenge

## Introduction
You have been asked to kick off a new native news app, initially consisting of just two screens
- The first screen will display a list of the headlines (fetched from a server - see below) and the last updated date
- When the user taps on a headline, the application then shows a second screen containing the headline and the last updated date again, as well as the introductory paragraph

## Design
The designer has asked that the typography be as follows:

Components | Color | Font
-----------| ------|------
headline | 0x000000 | large, bold, system font
last updated | 0x3d3d3d | normal, light, system font, 
introductory | 0x000000 | normal, regular, system font

### Timestamps
The returned timestamp is in epoch time but the design calls for this to be a human readable day, month and year. So, for example, it should show as "1 January 1970" for an epoch timestamp of 0.

### API
A backend engineer in your team has made a first cut of the API available for you to test with. The list of headlines, datestamps and introductions is available at
https://github.com/bbc/news-apps-coding-challenge/blob/master/headlines.json

```bash
curl -G https://raw.githubusercontent.com/bbc/news-apps-coding-challenge/master/headlines.json
```

### Analytics
The product manager has asked if you could also record some UI and network events as people use the app. This can be done by issuing [fire and forget](https://proandroiddev.com/making-asynchronous-network-calls-with-kotlin-coroutines-in-android-e3e72ea26632) GET requests to https://github.com/bbc/news-apps-coding-challenge/blob/master/analytics

Event specific query parameters should be appended to the URL as follows:

*UI Display Events*
* `event=display` – whenever a screen is shown (the headline or the article)
* `screen=XXX` - an identifier for the screen that was shown

*Network Load Events*
* `event=load` – any network request
* `time=xxx` - the time (in ms) for the network request to complete

```bash
curl -G https://raw.githubusercontent.com/bbc/news-apps-ios-coding-challenge/master/analytics?event=load&data=100
```
### Tap/Pull To Refresh
Ideally, the user should also be able to trigger a reload of the data from the server.

### Languages
For iOS roles, you can write the app in either Swift or Objective-C, but _you should avoid third party libraries_. If you use them, please explain why. For clarity, anything in the Apple SDKs we would consider first-party and an essential part of most any iOS app.

For Android roles, you can write the app in either Kotlin or Java, but _you should avoid third party libraries_.  If you use them, please explain why. For clarity, anything in the Android SDKs we would consider first-party and an essential part of most any Android app.

### Considerations
Remember we are looking for a demonstration of your skills - not perfection. A comment about what you would do next might be better than squeezing in everything but not doing anything to your usual standard. 

We think this is likely to take a couple of evenings...please don't feel you have to spend more time on it than that. Again, comments about next steps will help us to understand your thought processes.

This is an opportunity to demonstrate your understanding of what modern app development looks like. We believe that good contributors to achieving this are typically code readability, unit testing, separation of concerns, the open/closed principle, error handling, and an intuitive, responsive, user interface.

### Playbook
You may find our playbook of use in guiding your development and decision making

https://github.com/bbc/news-weather-apps-playbook

### Submissions
To submit your code, please create a private GitHub repo (it’s free) and share your code repo with our GitHub user, [bbcnewsapps](https://github.com/bbcnewsapps). Please note that we will be considering your git commit history during our evaluation.

_Under no circumstances make the repository public._
_Please email your BBC Careers contact separately as well to confirm your submission._

