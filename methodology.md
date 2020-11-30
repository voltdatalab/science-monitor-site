---
layout: pages
title: Methodology
last_update: "August 17, 2020"
description: "How Science Pulse works."
social_description: "How Science Pulse works"
main_img: '{{ site.baseurl }}/img/header_red.jpeg'
---

_You can get the core code for the application [in this link](https://github.com/voltdatalab/science-pulse-public). With time, we will make more elements available._

_[Leia a metodologia em português](metodologia)_

## ABOUT THE DATA

### PROFILE COLLECTION
All the profiles of scientists, experts, physicians, organisations and scientific initiatives were compiled by Science Pulse's development team through a number of methods. We found those profiles mostly through three ways:

1. A crowdsourcing, where people were invited to suggest a profile;
2. By identifying users with profiles verified by Twitter and checking the profiles that they follow;
3. Consulting Twitter lists of scientists made by universities and journalists.

Anyone can suggest a new profile to include in our platform through [this form](https://forms.gle/KHufKHzJxJVdsD7s8).

If you are a scientist or expert with a profile mapped by this tool, you can ask us to be left out. Send an email to [sciencemonitor@icfj.org](mailto:sciencemonitor@icfj.org).

### DATA COLLECTION

New posts in social media are collected constantly. For now, we are limiting the display of information for only 30 day-periods at a time. Our database is updated regularly with new tweets and counts, in respect to Twitter's free API limits.

We are still working on modules to include other social media platforms.

## ABOUT THE ALGORITHM

### TWITTER TRENDS TAB

All our trends consider only tweets published in the last 12-hours by our listed profiles. They consider both authored tweets and retweets as separate posts.

Trending tweets are separated into three groups for each language:

1. **Popular within pulse**: lists tweets authored by Pulse's list members that had the largest number of retweets from the whole population of Twitter users (retweet count), at the moment of the last data collection. Users can choose from two options: *Enhance Discovery* shows tweets from users who are below the median of the followers count from all profiles listed on Science Pulse; and *Focus on Popularity* shows tweets from all users listed in Science Pulse's database.

2. **Rising in popularity**: ranks the five tweets with the highest RT:followers ratio published by Pulse's list members (and only if they had more than 10 retweets). This list displays posts that had a significant engagement (RTs) from Twitter users considering the reach (number of followers) from the profile who wrote it. If a tweet has 200 RT and its author 400 followers, the tweet has a 0.5 RT:followers ratio.

3. **Discover more**: shows a random list from 5 tweets with more than one retweet and originally authored by profiles listed on Science Pulse. By clicking on "Get New Tweets" users get a new sample from random tweets under the same criteria.

### EXPLORE TWEETS TAB

The explore tabs digs deeper into our databases. It contains four sets of information on tweets posted in the last 12 hours and they are also filtered by language:

1. **Active Users**: the users who have tweeted the most over this period;

2. **Hashtags**: the most shared hashtags in the same time-lapse;

3. **Also popular within pulse**: we use a clustering algorithm (k-means clustering) to classify those tweets into four groups according to their retweet count at the time of the last data collection (1 through 4, with 4 being those with the most retweets). Then, we consider only tweets from "group 2", eliminating those that are probably personal messages and thus have less retweets (group 1) and those that had reached our main trends (Trends tab) or had reached users' Twitter timelines by their own organic reach (groups 3 and 4). Inside group 2, the also popular within pulse set uses the same metrics as the Popular within pulse set from the Trends tab.

4. **Pulse radar**: this set shows a random sample of five tweets from the previously described group 2. Tweets can coincide with the previous set, but gives the user a chance to find other interesting content that is not trending.

5. **Popular among scientists**:  shows the most retweeted posts published in Pulse’s database by the list’s own members. Every time one member shared a tweet, it counts as one. The highest ranked posts had the highest number of retweets inside the sample, thus identifying the tweets that got the most attention by the listed accounts. For example, if 15 profiles in our sample shared this [@WHO tweet](https://twitter.com/WHO/status/1275349898209173505), it has a 15 share rate.

### COVID-19 TWEETS TAB

The Covid-19 tab filters tweets in the last 12 hours by keywords related to Covid-19. Thus, it shows trends focused on pandemic-related issues. The metrics used here are same for the **Active users** and **Hashtags** from the Explore tab - with the caveat that we exclude common hashtags, such as [#COVID-19](https://twitter.com/hashtag/covid19), and the **Popular within pulse**, **Rising in popularity** and **Popular among scientists** from the Trends tab.

These are the keywords we apply as filters: "Covid", "covid", "Coronavirus", "coronavirus",
                    "Corona", "corona", "SARS-CoV-2", "Sars-CoV-2",
                    "SRAG", "sindrome", "syndrome", "pandemic",
                    "pandemia", "WHO", "OMS", "quarantine", "social distancing",
                    "quarentena", "isolamento social", "distanciamento social",
                    "mascara", "mask", "distanciamiento social", "spread", "asymptomatic",
                    "epidemic", "outbreak", "epidemia", "vacina", "vaccine", "wuhan", "Wuhan",
                    "herd immunity", "imunidade de rebanho", "imunidade coletiva".
                    
### SEARCH TWEETS TAB

In the **Search** tab, users can search from tweets over tha last 30 days, according to different filters, such as user-defined keywords, date range, verified profiles, retweets or replies.

### PROFILES TWEETS TAB

In the Profiles tab, we list all members from the group of scientists, institutions, researchers and experts curated by Science Pulse. To help users discover new and reliable sources of scientific information, the Find New Experts table shows a random sample of five accounts which have a number of followers smaller than the median number of followers from the profiles in our sample.
