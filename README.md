# Android Developer Nanodegree

Projects while attending the Android Developer Nanodegree program at Udacity

IMPORTANT API KEY note for Project 1/2 - Popular Movies App:

Use your own API key for the usage of The Movie DB API. Place a file called 'themoviedb.txt' in the
resources folder /res/raw (create if not exists). The file only has one single line, namely the API key.

##P0 - My Portfolio App

This simple app shows buttons, which start the apps developed in the course projects. 

<img style="position: center;" src="static/screenshots/P0 - My Portfolio App.png" width="300">

##P1 - Popular Movies Stage 1

Popular Movies is an app, which enables the user to instantly look up the most popular (or top rated) movies. Starting in a grid view, the posters of the movies are shown. When the user selects a movie, a detail view shows further information, like title, year, rating, and a short description. Movie data is asynchronously fetched from [TheMovieDB.org](https://www.themoviedb.org/). The user is able to sort the movies by rating, or popularity. 


[Screenrecord on Youtube](https://www.youtube.com/watch?v=ZUfGoRsqetg)
    
##P2 - Popular Movies Stage 2

Stage 2 of Popular Movies enhances the experience of the app. The user is now able to watch trailers, read reviews, and also an offline functionality is introduced. When a movie is marked as a "favorite", the movie information gets stored in a local database, which preserves the data in a persistent manner. So the user can see movie information of favorites also when there is no internet connection. To access the favorites, another toolbar entry is added. 
Finally, the app design is optimized for tablet usage, providing a master-detail layout.

[Screenrecord Phone Layout on Youtube](https://www.youtube.com/watch?v=iGYWjl--L5s)

<img style="position: center;" src="static/screenshots/P2 - Popular Movies Stage 2_Phone_1.png" width="300">
<img style="position: center;" src="static/screenshots/P2 - Popular Movies Stage 2_Phone_2.png" width="300">

<img style="position: center;" src="static/screenshots/P2 - Popular Movies Stage 2_Tablet_1.png" width="600">
<img style="position: center;" src="static/screenshots/P2 - Popular Movies Stage 2_Tablet_2.png" width="600">
<img style="position: center;" src="static/screenshots/P2 - Popular Movies Stage 2_Tablet_3.png" width="600">

##P3 - Stock Hawk

During this project a basically working app should be enhanced in a way, so it is "ready for production", for publishment e.g. via the Google Play Store. Stock Hawk is an app, which provides data from the Yahoo Finance API. The user can search for stock symbols and add them to his watch list (stored in a local database). 

The project starts with the current sources of the Stock Hawk app, and a list of user reviews:

---------
**User Feedback for Stock Hawk:**

Hellen says:
"Right now I can't use this app with my screen reader. My friends love it, so I would love to download it, but the buttons don't tell my screen reader what they do."

Your boss says:
"We need to prepare Stock Hawk for the Egypt release. Make sure our translators know what to change and make sure the Arabic script will format nicely."

Adebowale says:
"Stock Hawk allows me to track the current price of stocks, but to track their prices over time, I need to use an external program. It would be wonderful if you could show more detail on a stock, including its price over time."

Gundega says:
"I use a lot of widgets on my Android device, and I would love to have a widget that displays my stock quotes on my home screen."

Jamal says:
"I found a bug in your app. Right now when I search for a stock quote that doesn't exist, the app crashes."

Xaio-lu says:
"When I opened this app for the first time without a network connection, it was a confusing blank screen. I would love a message that tells me why the screen is blank or whether my stock quotes are out of date."

---------

Based on the users' feedback, certain aspects of the application are enhanced/implemented:

####Accessibility (A11y)
The most important aspect before publishing an app is to be aware of the wide range of potential users of the app. So it is crucial to support visually handicapped useres with Screen Reader properties. Google's TalkBack service provides spoken feedback for every interaction with the device. Stock Hawk does not yet have description for all buttons and other UI elements, so this missing information is added. 

####Localization (L10n)
As important as A11y is, localization is also a very essential key for a successful app. Based on the feedback of ***the boss***, the release in Egypt is planned, so the app should be fine with Arabic translations and support for RTL (right to left) layouts. 

###Homescreen Widgets
Widgets are an effective way to gain the attention of the user, without the need of opening the app. They can be placed on the Android homescreen, where they provide essential and compact information. In this project, two types of widgets are implemented. A 4x1 single-row widget shows the top most stock symbol, and a so called collection widget provides a resizable 4x3 container, which shows a scrollable list of the stored stock symbols. 

####Displaying data in a chart
One user requests a chart view, which shows the stock changes over time in a graph. For this purpose, the library [WilliamChart](https://github.com/diogobernardino/WilliamChart) is used, which shows the stock changes, when the user selects a stock symbol on the main screen.

####Error handling and misc changes
Stock Hawk could not handle stock searches for non-existing symbols, so it crashed. This problem and several minor issues are addressed and fixes are provided.


