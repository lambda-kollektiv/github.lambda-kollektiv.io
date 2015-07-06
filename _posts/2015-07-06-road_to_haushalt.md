---
title: Road to Haushalt
layout: post
author: konny
abstract: A vision of managing domestic resources digitally
---

Having always a bunch of bills laying around and being too lazy to type all the stuff by hand in some spreadsheet, we are lots of the time in the dark about our current financial situation. Sometimes only the way to a bank machine solves this problem because online banking system is not available. Digitalizing our bills by using object recognition algorithms and analyzing them statistically should be a useful day-to-day application. Furthermore, if we have an online account, we want to synchronize it with our application data. 

In the following we will draft a vision of this application by describing some user stories and then giving a short overview of resulting features. At the end we will give a rough roadmap of the next development steps.

## User Stories
- Eva is a student, who has only few money to spend and decides to take a yoga class for 30€ a month and a gym membership for 40€ a month. She wants to know if she can afford both. She opens *haushalt*, selects *statistics* button and sees in the *overview* that she has only 60€ to spare a month at the current time. Now she knows she only could take the yoga class. Good choice, Eva! ;)
- Adam comes home after shopping groceries and clothes. As a very strictly person, he wants to record this entries and opens the *haushalt* app. The screen shows a navigation pane with the buttons for statistics and settings. Below there are input fields for his purchases. For each of them he fills in the necessary values and finishes them with the *done* check mark.
- Now Adam wants to compare the current purchase to previous ones and selects *compare* in the main screen. The *statistics* view opens and a red mark shows in a graph that he has spend a little bit more than usual today. He should only buy water and bread in the future.
- Eva has just received the email receipt of an online shop. Now she records this purchase by visiting the *haushalt* site. As this is not her first time there the home screen welcomes her personally and shows her most used activity on the site: recording new purchases. She clicks this button and the screen shows input fields for her new purchase: amount, category, cash? and shop. She copies the relevant data from the email an clicks the save button. Her smartphone notifies her that a new transaction was made. 
- **FUTURE**: Adam comes home after shopping groceries and instead of writing all what he has bought into a notebook he opens *househalt* and uses the scan button to take a picture of the bill. The screen shows the bought entries and the market as well as the time. Additionaly it shows a *done* and *edit* button. Adam sees that the market is not correctly scanned, so he clicks the *edit* button, selects the market, corrects it and pushes *done*.

## Features
- simple finance management
- distributed database in smartphone, web frontend and server
- website and mobile application
- input manually first, later recognition
- statistics
- passwordless login

## Roadmap
- more user stories
- feature set evaluation
- design and technology decisions
- simple prototype showing expenses
