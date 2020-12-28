---
title: 'PhotoStream.Live'
subtitle: 'Solving my own problem to create a bootstrapped product'
date: 2020-12-22 00:00:00
featured_image: '/images/photostream2.png'
excerpt: A successful side project that has grown organically after I built it for my own wedding in 2016. The product allows events to run a live stream from audience photos and videos. Customers from around the world have used the product for their events. This has been a great project to learn and apply skills in design, web development, marketing, sales and product management.
---

![](/images/photostream2.png)


Checkout this project at <a href="wwww.photostream.live">PhotoStream.Live</a>


## First Update (22/12/2020)


### Solving my own problem


The initial idea for this project occurred when my wife and I were planning our reception wedding dinner in 2016. We were over budget and needed to cut down on one of our big expenses. The choice was between our food and drink package  or photography during our reception dinner. That's when the idea struck me, why not just crowd-source our photos from all our event guests! We would still keep professional photography for our ceremony and bridal shoot, but during dinner we can just ask our guests to snap more pics on their smartphones. To help incentivise photo sharing I would run a live stream on a central projector so that everyone could see their shared photos in real time. 


I built a very hacky version of this idea using third party APIs to monitor a hashtag on Twitter and Instagram and a dedicated inbox for emailed photos. The live stream page used long polling to monitor a queue of processed photos on the backend, with everything running off my laptop for the event. There were a lot of bugs (I have the fond memory of ducking out of my own wedding dinner to reset some queues on my laptop) but the overall idea worked well. We got some really cool photos that we probably wouldn't have collected without the incentive of the live stream. 


### Organic Validation


After my wedding I noted down some improvements but didn't really find the time to work on the idea. Then a year later a friend from my wedding asked to run it for his wedding. I spent a few days implementing the improvements I had noted down. At this event everything worked smoothly and the idea really took off, people were posting tons of selfies, photos and memes. There was even a few times I had to turn off the projector because it was proving to be a distraction during important parts of the night! 

After this, some people who saw the live stream at my friends wedding asked to run it for their events. I converted the code to a run on a cloud server and got my first paying customers! There was a hairy moment for one of these events, where I found out a couple of hours before it started that the email service I was using changed a critical part of their API. I had to manually post emailed photos to the live stream while simultaneiously try to fix the issue as well. Luckily I could keep up with the volume of emailed images and the users ended up providing positive feedback for how everything went.


After running the product for a number of events without any marketing or pushing and seeing the high level engagement the idea definitely felt reasonably 'validated' to invest more time in. 


### Building a MVP


After leaving my full time job at the end of 2019 I took some time to build out the idea properly. I now had a really good list of requirements from the events that had used the product so I didn't have to worry about the usual problem in early product development of building too many features or building features that no one wanted.


Given I had been using Python for my full time job I choose Django for the web development (with vanilla javascript mixed in where I needed it as well). I also used the excellent <a href="https://www.saaspegasus.com/">SaaS Pegasus</a> Django starter template to help cut down on dev time. For the live stream component that processes posts from users I chose a serverless solution (AWS Lambda) due to the event-driven nature of the problem. The alternative would have been using some type of long polling architecture that would be harder to scale. Serverless also seemed more efficient as events only run for small periods time and require short bursts of compute when a user posts a photo. The <a href="https://www.serverless.com/">serverlress framework</a> was critical in overcoming some of the challenges in working with AWS Lambda. I might document my experience implementing on Lambda in a seperate post.


### Launching into the pandemic


After finishing development in March 2020 the pandemic had just started to become a reality which meant most live events were cancelled or delayed. Pretty bad timing! Once again I moved the project to the side with the intention to return as the pandemic started easing.


### Marketing and sales


In November 2020 I started receiving some emails about the product which seemed to indicate an uptick in event planning so I took some time to focus on marketing and sales. My initial plan was to niche down and target weddings. It's become clear that this was the wrong path to go down. The wedding industry is definitely huge, but getting enough traffic that would convert into sales would take some time through SEO, paid marketplaces and partnerships. Because the product is mainly bought for one-off usage, casting a wider net to all events is necessary to generate enough ROI more quickly. The pandemic cancelling so many weddings also made this decision easier.


Another challenge I had was determining the best positioning of the product. There are many potential problems a live crowd sourced photo stream can solve:

* Save money on photography by crowd-sourcing photos and videos (the original reason I made it)
* A cheap and easy live stream solution for your event from guest photos and videos (more pertitent because of guests who can't attend events due to the pandemic)
* Collect lots of cool photos and videos from your guests (weaker selling point that isn't really solving a problem as most events who need to get photo will have photographers)
* Entertain your event audience and boost engagement


You might be thinking that this is a classic case of a solution searching for a problem. But I knew that customers loved the product, I had people offer me money without any pushing to use the prouduct and these are all legitimate problems that were being sovled. It's just a questions of whether the volume of sales could reliably overcome the opreating costs and customer acquisition costs. Theoretically, the best positioning is the one that can charge the most, solves the biggest problem (related to charging the most), occurs most frequently and is cheapest to acquire customers repeatedly for. Whichever positioning maximises the combination of these levers would be the best choice. 


After testing the above positioning options and talking to customers it has become clear that the best positioning is 'Entertain your event audience with a live photo stream'. While replacing professional photography is the biggest problem being solved (in terms of adding value and saving money), it is too hard of buying decision to make on an unfamiliar product people will to spend money on a professional photography in the first place. The product was also not strong enough of a solution for the 'live stream your event to remote viewers' positioning. It's definitely possible a small set of users will buy the product for these usecases once they are familiar with it and are in some special constrained budget scenario (like I was at my wedding), but it's not strong enough for a the main solution positioning.


The other surprising benefit that has come out of the pandemic are customers using the product for virtual events. If you want an easy way to increase engagement from a large virtual event audience then there really isn't any other solution (apart from direct competitors). So while the pandemic initially crushed the idea, its looking like it's created a new form of consistent demand. 


### Growth


I can now see a clear positioning and path to consistent growth. Of course it's going to interesting to reflect back on this confidence in the future. There are people who are definitely searching for ways to increase engagement at their events and I have an easy to use solution that users really enjoy. The next step is to build out reliable channels of acquisition with this current 'best positioning' in mind.



### Updates


I plan to keep updating this page with new learnings and results, mainly as a way to journal my thoughts and observe my decision making.
