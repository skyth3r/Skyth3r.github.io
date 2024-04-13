---
title: TfL to Monzo
date: 2019-04-01
images:
- https://raw.githubusercontent.com/skyth3r/skyth3r.github.io/master/assets/portfolio-images/tfl-to-monzo.png
description: A Monzo API project to import TfL journey data and link it to TfL transactions on a Monzo account
---

TfL to Monzo was an severless application built as my project for my Cloud Computing module at university with a friend.

It was written in Python and made use of AWS Lambda to process TfL jounrey data into Monzo recipts.

The Lambda function would recieve incoming transcation webhook events from a linked Monzo account, check if they were TfL transcations and then run a web scraper script to extract the matching journey data from the TfL web portal before then submitting this data as a reciept to the Monzo receipt API endpoint.

This was one of my favourite projects at university and overall we recieved a final mark of 98/100. I also posted a [tweet](https://twitter.com/akashgoswami_/status/1112685400336855040) of this project and it was highly received.

**Screenshots 👇🏽**

![](/portfolio/tfl-to-monzo-tweet.png)

![](/portfolio/tfl-monzo-1.png)

![](/portfolio/tfl-monzo-2.png)

![](/portfolio/tfl-monzo-3.png)

![](/portfolio/tfl-monzo-4.png)


