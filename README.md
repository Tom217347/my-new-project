# my-new-project
Building AI Course project
<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 

# Foghorn - find me the best route

Final project for the Building AI course

## Summary

Personalised app/portal that helps user to find the best route for any sport (e.g. cycling, canoeing, running) using route features, significantly enhanced by textual data from user prompts/reviews/qualitative preferences


## Background

Which problems does your idea solve? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?

Finding suitable route is a tedious process, requiring lot of click through various portals, information often not complete, not aligned to personal preferences.
With multitudes of data available users are losing time and often not get a good result
Current routing applications or “portals” are typically one-dimensional (e.g. distance), but would not reflect qualitative views such as: what the users written about it, what my personal preferences are (e.g. training phase I am in, type of weather, what I like “long climbs”.

## How is it used?

User is any person seeking a route for sport or sport-like activity, whether for training purposes or leisure.
Instead of using existing apps and tediously filtering, the user can use natural language prompt such as "I want to do a 10k run in a forrest, that is not very hilly, accessible by car from my address in 10 minutes, with a parking lot. Has to be a round-trip. Typical user would be somebody training for half-marathon"

## Data sources and AI methods

Underlying data: internet and routing applications such as Komoot and Strava (note: this is a plan "A", fallback plan "B" would initially depend on AI generation of routes and subsequent reviews) . Personal history, preferences and evalutions captured and processed through Foghorn

Data scope: technical parameters (distance,….etc) , verbal description by authors of the routes, user reviews, personal preferences, personal history of previous selections or routes completed.

The origin of data is existing routing applications and other internet sources. Those data need to be scraped and regularly updated. This done through API. Quality of data is reasonable but with time further optimisation possible. 
Critical point would be to process and analyse the verbal evaluation of routes (reviews) and allow for effective cross-reference against the user’s preferences and history. 
Personal preferences will be captured via Foghorn and further analysed against the pool of information from its other users.
AI techniques would need to do the following:
The underlying ROUTE model would need to cross-reference technical route features for individual route segments with the underlying textual description of the route and the verbal assessment of users. Segments have to be ranked against the technical criteria (in measurable units), facts (hilly, flat), assessment by users (ranking x qualitative). Model has to allow sequencing the segments as per existing routes, but also into combining those into new routes.
User prompts a) facts (sport, location…) b) preferences (easy, no busy street, no natural risks) and c) automated an embedded user history -weighted preferences, usage etc. will then be an input into ROUTE Model, leading to a route selection.
Further fine tuning of prompts and question will allow further fine tuning of the first choice.
Deep-learning models, Graph neural networks, etc. will be required. TBD.

## Challenges

It might have an effect on incumbents such as Strava. However, unlike Strava, Foghorn purpose is not to measure performance and capture/analyse the personal performance data. Its not used for competition on segments. Its purpose is to help the user to find the best routes from any available source.
It will be very much focus on qualitative criteria enhancing the technical data sets of “incumbents”
Apps such as Strava can benefit from this additional tool – Foghorn will share its data with Strava and such, as much as Foghorn will be using their data. 

Technical limitations: the verbal, qualitative data processing and usage in route selection could be a challenge. Not yet clear there is enough data and not yet clear how those could be best processed. 
User limitations: users would have to be productively engage in order to share their views and history. This could be overcome by them seeing the utility of the solution
Commercial limitations: lot will depend on building an eco-system with incumbents and data owners -> requires building a sound commercial and financial model that would benefit all involved. Fallback: build the data set from scratch by creating routes using AI and sourcing those routes from publicly available geo / gps data, frequency of mentions of routes on internet and adding some qualitative data. The routes will be free to use by users of Foghorn, but the users will be required to actively contribute with their verbal assessments and comments (any new route only available as gpx only after the user evaluated the previous route)


## What next?

Technical review is needed to build the solutions architecture; 

Make a decision whether Plan A working with the existing app owners and their data is viable commercially and technically. 
If not, pursue the fallback solution that would require building an engine that generates the routes based on technical geo data and some additional environmental paramaters (type of location, traffic, ...)

