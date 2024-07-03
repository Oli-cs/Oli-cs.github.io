---
layout: ../../layouts/Md_Layout.astro
title: HackTheBurgh X
originPage: ../../projects/index.html
author: Oli
pubDate: "2024-07-03"
lastUpdated: "2024-07-03"
---

# <span class="text-gradient">HouseLink</span>

## Idea
We came up with this idea a couple of days before HackTheBurgh X, a 24hr hackathon at the University of Edinburgh. During this hackathon our team of 3 were in the middle of a coursework which involved designing and building the backend of a system that a fictional letting agency would be using, which is where the idea "What if there was a housing app that had Tinder mechanics" came from.

## Development
We built our app using Python, utilising libraries such as tkinter to create a GUI for the user to interact with it. Users are able to use the arrow keys to "swipe" left and right to like and dislike properties. Users can view images and descriptions of the properties - their price, number of bedrooms/bathrooms, their addresses and also the agencies/landlords who currently own them.<br/>

To store all the houses available to view along with their details, we used an SQLite database and integrated it with the Python application. This allowed us to manipulate the database by executing SQL commands directly from the program itself. Using SQLite, we were able to get all the relevant information for any given property and present it to the user, giving each property an autoincremented primary key to help identify it. Using SQLite meant we were able to store and access our data far more cleanly and effectively than if we were to use a flat file.<br/>

Our housing recommender system works by taking users' "swipes" as primary data to inform its decisions on which properties to recommend. Using these swipes, it calculates the means and scaled standard deviations for each different aspect of the property, then takes the field with the lowest variance in these standard deviations as the field most desired by the user. It uses this information to then recommend unseen properties that most closely match what the user likes.<br/>

One challenge we ran into was properly animating the frames to replicate the "swiping" motion of apps like Tinder, due to limitations of the GUI library we were using. We decided to work with what we had in favour of keeping time on our side, and so decided against replicating this swiping motion and to just slide through frames instead. While this is not the usual animation, we still believe it works well with the app we have developed.<br/>

Another challenge we faced was within our recommender system, in which we found recommendations were never being made on price. This is because the prices for houses varied so greatly that their standard deviations were always much larger than those of bedrooms and bathrooms, even if the user was consistently going for the cheaper/more expensive houses. To fix this issue, we decided to use a scaled standard deviation instead, and so multiplied each value by a constant to balance them out. This weighted standard deviation proved far more effective than our previous algorithm.

## Links
Click <a href="https://github.com/oli-cs/HackTheBurghX">here</a> to see the GitHub repository<br/>
Click <a href="https://devpost.com/software/housetinder">here</a> to see the Devpost submission