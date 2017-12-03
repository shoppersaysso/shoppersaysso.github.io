---
layout: post
title:      "Straydar, an app to report stray cats"
date:       2017-12-03 17:38:51 -0500
permalink:  straydar_an_app_to_report_stray_cats
---


There are a lot of stray cats in my neighborhood. I mean, A LOT. They can be seen darting across the sidewalks, hiding under cars, or congregating in the parking lot behind my apartment building. They fight, they yowl, and when they are in heat, these sounds are exponentially louder.

I don't have anything against cats but they can be a bit annoying when trying to sleep or studying in peace and quiet. I also worry about their health and safety.

I happen to be very allergic to cats, so approaching them or rescuing them myself is not really a good option for me.

Enter Straydar.

Straydar is an app built to report stray cat sightings. You can report a stray cat sighting by filling out a simple form with basic information and the location you spotted the cat.  You can even upload an image if you managed to snap a photo on your phone. You can then filter through the list of already reported sightings to try to find specific cats.

The idea is to help track stray cats and also to help locate ones that might be lost cats that their owners are looking for.

In this first version, you can so far only sort the list by cat color. In the future, I hope to implement searching by all key words in the details section as well as trying to narrow down results by a specific map area.

In building this app, I worked with the Google Maps API (which was suprisingly easier than I had expected) to take the address inputted by the stray cat form and populate the location on a map. In the future, I'd like to be able to have one large map with markers of all stray cat reports on it.

I also worked with an image service called Cloudinary. Cloudinary offers photo storage in the cloud and is very friendly to web development. Their code was very easy to work with and they even offer a lot of pre-made code snippets in various code languages to help you get started.

Find the code on GitHub for the Straydar API (written in Rails 5) is here: https://github.com/shoppersaysso/straydar-api
And the code for the Straydar Client (written in React 16) here: https://github.com/shoppersaysso/straydar

Straydar is also deployed on Heroku here: https://straydar.herokuapp.com
