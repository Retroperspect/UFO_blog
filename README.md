# LSD Blog

## Abstract

- System Failure is a commen issue related to human errors, The biggest errors are the ones you don't even realise are happening, as some system failures aren't so obvious to notice unlike the entire system is dead while your interacting with it, if this happened before anyone touched the system you wouldn't know when the issue appeared depending on your implementation of the system.
- Customers hate paying for broken promises, and corperations hate loosing customers and money on fixing these issues whenever they creep up, likewise depending on how curcial the system is for human lives, a system failure could lead to injury or even lose of human lives.
- You can reduce or even eliminate these problems by implementing monitoring for your system, using systems like Promethues and grafana, enables the developers to specify and monitor every angle of a system, enabling you to identify current and new problems that appear as you develop your systems.
- Monitoring your systems insures your ability to respond when the system is starting to experience issues or even alert you the moment the system reaches critical or none functional states, this enables better testing of the system and increases both user and corperations satisfaction.

?# Extend by 2-5 lines (No more)

## Running in the dark
- Expalin the problem better.
- Explain how many people are running their system without actully knowing real time what goes in the system, and not realy knowing completely how the system functions or how well it performes.


??? DO NOT MENTION MONITORING (THAT IS OUR SOLUTION)
## What does our survey say about companies running in the dark?

We wanted to see what developers working in IT-companies think of implementing monitoring and metrics in their IT-systems. Do they have it implemented why and why not? We made a poll in a facebook group of 13247 coders many of whom work as software developers in Sweden. We got more than 70 votes.
The question in the poll was:

### Question in poll

**Do you use monitoring and metrics ( with tools like New Relic, Grafana/Kibana) to the extent that you want in your IT systems?
Although there are only advantages to have it implemented for both small and large systems. I suspect that it might not be implemented (in IT systems) for some reasons.**
- Both yes and no. It depends on the project. (40 votes) 
- Yes. We always use monitoring and have control of what is going on in our IT systems. (21 votes)
- No. We don't use monitoring but it would probably be good. (12 votes)
- No. We manage without. (2 votes)
- No. We don't use monitoring because it made more damage than good. (1 vote)

### Result from the Facebook poll
From our poll, the target group says they implement monitoring and metrics depending on the type of project. Second highest target group identified with the option implementing monitoring and metrics always and having full control of whats going on in their IT-systems.
The image shows the result of the poll.

![Facebook poll in a group for coders](/images/fb_poll.png)


When doing the poll we also got some feedback in the comments indicating that there seem to be developers that have passion and are experts in monitoring and metrics. We also got feedback that some IT-systems suffered from implementing monitoring. 
Their experience was that monitoring isn’t just about pulling statistics but it is a matter of choosing wisely and even taking in experts to get it right otherwise, otherwise, it can have an opposite effect. Some people have experince of metrics showing data that lead in the wrong direction and taking time away from doing actual debugging.

### Indication from a survey targeting people having insight to IT-systems

We also did a survey to get further insights into how widley used monitoring is in companies.

The survey was targeting people working within IT-companies of whom 50%, when having a monitoring system, says they have been involved implementing monitor systems in their company.
In our survey 80% says that they use some kind of monitoring systems like Grafana/Kibana etc.
For those saying they dont use monitoring system "Lack of time" was the main reson why they haven’t implemented it.

On the question: Have you IT-system ever one down or not functioned correctly without your knowledge? 50% using monitors systems say yes. 100% not using monitor systems answer positively to this question.

[![https://gyazo.com/16d84f47ac77d11390037ceeda6d9b6e](https://i.gyazo.com/16d84f47ac77d11390037ceeda6d9b6e.png)](https://gyazo.com/16d84f47ac77d11390037ceeda6d9b6e)

Of those using monitor system 50% say they experince no negative impact haveing it implemented.
50% answers it has some negative impact.

[![https://gyazo.com/81731fa62d81b76f8628bbfe75417f08](https://i.gyazo.com/81731fa62d81b76f8628bbfe75417f08.png)](https://gyazo.com/81731fa62d81b76f8628bbfe75417f08)

Giving the reason "overhead in maintenance" as the negative or con of using monitoring system.

For those having monitoring systems implemented we asked which part of the system they thought was the most important to monitor:

[![https://gyazo.com/3babd0a3e5a4fcc1ab7fc0c5faf142b8](https://i.gyazo.com/3babd0a3e5a4fcc1ab7fc0c5faf142b8.png)](https://gyazo.com/3babd0a3e5a4fcc1ab7fc0c5faf142b8)
## Consequence of running in the dark
>>>- Include a Qualitative method: Interview with a company who does not have monitoring
- Expalin the censequence of running in the dark.

## Solution
There is more ways to solve this specific issue, but the most common and standard way in the industry is by doing real time monitoring. Monitoring can be setup with real time logging with the help of example: [ELK stack](https://www.elastic.co/webinars/introduction-elk-stack) or capturing important metrics. This solution is leaning towards capturing important metrics and displaying them in a graphical dashboard which can be watched. This way you can in realtime see changes to these metrics which can help inform of how the system is actully doing right this moment. Examples of these would be: How many requests does my website get. Or, How many threads are my program running. Or, How much space is left on the harddrive which my database is running. There is many other cases which this can be applied to. This will provide a good way to know exactly how every inch of a system is doing at any time.

There is more ways to implement metrics monitoring, this solution will use prometheus in conjuction with grafana.
- [Prometheus](https://prometheus.io/): A database good at treating time-series data.
- [Grafana](https://grafana.com/): A User Interface good at representing time-series data in graphs.
These implementations are open source and therefor free to use. 
This is a guide for the solution: [Guide](https://github.com/vegasbrianc/prometheus)

Is this solution a good one?. According to mutiny it is. They provide 6 reasons why IT monitoring is important to a business.
[Mutiny's 6 reasons](https://www.mutiny.com/news/blogs/2016/6-reasons-why-IT-monitoring-and-reporting-is-important-to-your-business/)


## Gains
- From our own observation, the immidiate gain from having a prometheus and grafana was the overview, although some tweaking for what data we saw was needed, seeing the systems performance and having warnings notify the phone about system crashes was a huge help.  
Being able to both actively and passively monitor the systems performance ensured our systems uptime, as this was important for a above 95% uptime deal. By actively monitoring our systems performance, we noted that we slowly but surely weren't able to handle the amount of data we received, had it not been for monitoring we wouldn't have known this, and we wouldn't have been able to identify the issue was with the database, since we queried too much data too and from it.  
The issue was a human flaw in our understanding of relational databases, as we asked the database for many queries that by our research should work, we did not take into account that the lack of Foreign keys would result in such extreme slowdown, as we didn't notice these issues from our initial testing with smaller sets of data.  
Observing the performance enabled us to solve this and many other issues as they appeared, as anytime we observed abnormalities we would investigate the cause, with the help of monitoring we had a better idea of where these issues came from.  
One specific moment wasn't a issue in the general term, we observed from our teachers monitoring that our system was lacking behind another groups progress, which we had been mirroring in performance for a long time. Everything seemed alright on our local systems performance so we had to pinpoint what change could have resulted in this change, which resulted in the discovery of a recent implemented system incidentely had send our systems entry point futher away from it's original position physically, resulting in slower response time that made the system just a tiny bit slower.  
Monitoring doesn't solve issues but it alerts the developers about the issues, we personally don't know how we would have found these issues as it's mostly not related to code, which is the primary way for programmers to debug issues, but the issues that appears where  when multiple systems interact with eachother.  

## Conclusion
- System failures are the byproduct of human design as we humans are prone to produce errors without knowing it, in the current digital age this present problems, system failures can have minor impacts both financially and user satisfaction, or cripple corperations and even result in the lose of lives.  
Avoiding this as developers is our top priority, therefor the use of monitor systems like prometheus and grafana, is crucial for maintaining our system and avoiding future issues, or in the worst case stop the system before it does too much harm.  
Another benefit from monitoring is learning from mistakes that havn't happened yet, you know the saying "A fool learns only from his own mistakes. A wise man learns from the mistakes of others." we learn from mistakes that havn't happened yet by monitoring.
