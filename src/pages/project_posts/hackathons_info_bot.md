---
layout: ../../layouts/Md_Layout.astro
title: Hackathons Info Bot
originPage: ../../projects/index.html
author: Oli
pubDate: "2024-07-03"
lastUpdated: "2024-09-12"
---

# Hackathons <span class="text-gradient">Info Bot</span>

## Idea
I had this idea when running for trips and hackathons secretary of <a href="https://hacksocnotts.co.uk/">Hacksoc</a> at the University of Nottingham. Initially I was only going to include hackathons sponsored by Hackathons UK because they have an API, but after realising that they weren't going to give me access (the API wasn't public) I decided that I would scrape the information I needed off the relevant public webpages and so this bot may also do MLH hackathons at some point in the future

## Development
I've written it in python for the time being but I feel like I should write it in rust to get to know the language better. Setting up a discord bot was interesting because the bot doesn't directly interface with my code, discord manages the bot and my code polls an api to ask if there's any jobs waiting for it to process.


## Links
Click <a href="https://github.com/oli-cs/hackathons-info-bot">here</a> to see the GitHub repository