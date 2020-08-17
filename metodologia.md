---
layout: pages
title: Metodologia
last_update: "17 de agosto, 2020"
description: "Como o Science Pulse funciona."
social_description: "Como o Science Pulse funciona."
main_img: '{{ site.baseurl }}/img/header_red.jpeg'
---

_Você pode acessar nosso código aberto desta aplicação [neste link](https://github.com/voltdatalab/science-pulse-public)._

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

1. **Popular within pulse**: lists tweets authored by Pulse's list members that had the largest number of retweets from the whole population of Twitter users (retweet count), at the moment of the last data collection.

2. **Popular among scientists**:  shows the most retweeted posts published in Pulse’s database by the list’s own members. Every time one member shared a tweet, it counts as one. The highest ranked posts had the highest number of retweets inside the sample, thus identifying the tweets that got the most attention by the listed accounts. For example, if 15 profiles in our sample shared this [@WHO tweet](https://twitter.com/WHO/status/1275349898209173505), it has a 15 share rate.

3. **Other popular tweets**: records the most shared tweets considering the most recent retweet counts of each. In this set, we identify those posts with wide repercussion on Twitter that were also shared by our experts’ and institutions’ list. They count retweets among the whole set of Twitter users, at the time of the most recent share by one of the accounts in our sample. For example, it considers the total RT count for this [tweet by @WHO](https://twitter.com/WHO/status/1275349898209173505) at the time it was shared in the sample (564 RT at 5:15pm GMT -3).

### EXPLORE TWEETS TAB

The explore tabs digs deeper into our databases. It contains four sets of information on tweets posted in the last 12 hours and they are also filtered by language:

1. **Active Users**: the users who have tweeted the most over this period;

2. **Hashtags**: the most shared hashtags in the same time-lapse;

3. **Also popular within pulse**: we use a clustering algorithm (k-means clustering) to classify those tweets into four groups according to their retweet count at the time of the last data collection (1 through 4, with 4 being those with the most retweets). Then, we consider only tweets from "group 2", eliminating those that are probably personal messages and thus have less retweets (group 1) and those that had reached our main trends (Trends tab) or had reached users' Twitter timelines by their own organic reach (groups 3 and 4). Inside group 2, the also popular within pulse set uses the same metrics as the Popular within pulse set from the Trends tab.

4. **Pulse radar**: this set shows a random sample of five tweets from the previously described group 2. Tweets can coincide with the previous set, but gives the user a chance to find other interesting content that is not trending.

### COVID-19 TWEETS TAB

The Covid-19 tab filters tweets in the last 12 hours by keywords related to Covid-19. Thus, it shows trends focused on pandemic-related issues. The metrics used here are same for the Active users and Hashtags from the Explore tab - with the caveat that we exclude common hashtags, such as [#COVID-19](https://twitter.com/hashtag/covid19), and the Popular within pulse and Popular among scientists from the Trends tab.

These are the keywords we apply as filters: "Covid", "covid", "Coronavirus", "coronavirus",
                    "Corona", "corona", "SARS-CoV-2", "Sars-CoV-2",
                    "SRAG", "sindrome", "syndrome", "pandemic",
                    "pandemia", "WHO", "OMS", "quarantine", "social distancing",
                    "quarentena", "isolamento social", "distanciamento social",
                    "mascara", "mask", "distanciamiento social", "spread", "asymptomatic",
                    "epidemic", "outbreak", "epidemia", "vacina", "vaccine", "wuhan", "Wuhan"

### POPULARITY TWEETS TAB

The Popularity tab allows the user to check the most posted hashtags and active users in a selected date range, and also plot a graph on the number of posts that included a specific keyword.

### PROFILES TWEETS TAB

In the Profiles tab, we list all members from the group of scientists, institutions, researchers and experts curated by Science Pulse. To help users discover new and reliable sources of scientific information, the Find New Experts table shows a random sample of five accounts which have a number of followers smaller than the median number of followers from the profiles in our sample.
