
# LSD Blog 
 
## Abstract 
 
- System Failure is a common issue related to human errors, The biggest errors are the ones you don't even realize are happening, as some system failures aren't so obvious to notice unlike the entire system is dead while you are interacting with it, if this happened before anyone touched the system you wouldn't know when the issue appeared depending on your implementation of the system. 
- Customers hate paying for broken promises, and corporations hate losing customers and money on fixing these issues whenever they creep up. Likewise depending on how crucial the system is for human lives, a system failure could lead to injury or even loss of human lives. 
- You can reduce or even eliminate these problems by implementing monitoring for your system, using systems like Prometheus and grafana, enables the developers to specify and monitor every angle of a system, enabling you to identify current and new problems that appear as you develop your systems. 
- Monitoring your systems ensures your ability to respond when the system is starting to experience issues or even alert you the moment the system reaches critical or none functional states. This enables better testing of the system and increases both user and corporations satisfaction. 
 
## Running in the dark 
Running in the dark is a made up term which describes the problem that is, to do something without observing. Running a system without monitoring is like riding a caravan. You have a vague idea of what direction you want your system to go in, and you have a feeling that it's going there as your running it. But imagine you were deaf to the horses complaining, unable to notice the horses slowed down, and you only would notice when they collapsed on the floor. The wheel on the wagon can break but the wagon can still run if there's enough support, but all these parts that can wear and tear can break at any moment without you knowing when or why. If you don't know what parts are slowing down or breaking you'll never react, but at the same time all parts could also run longer than the system is supposed to run, and then you'll never notice if paying attention was needed at all. 
 
## What does our survey say about companies running in the dark? 
 
We wanted to see what developers working in IT-companies think of implementing monitoring and metrics in their IT-systems. Do they have it implemented why and why not? Are they running in the dark? How much insight does monitoring system give? We made a poll on a [Facebook group](https://www.facebook.com/groups/utvecklare.stockholm/about/) of 13247 coders many of whom work as software developers in Sweden. We got more than 70 votes. 
The question in the poll was: 
 
**Do you use monitoring and metrics ( with tools like New Relic, Grafana/Kibana) to the extent that you want in your IT systems? 
Although there are only advantages to have it implemented for both small and large systems. I suspect that it might not be implemented (in IT systems) for some reasons.** 
- Both yes and no. It depends on the project. (40 votes)  
- Yes. We always use monitoring and have control of what is going on in our IT systems. (21 votes) 
- No. We don't use monitoring but it would probably be good. (12 votes) 
- No. We manage without. (2 votes) 
- No. We don't use monitoring because it made more damage than good. (1 vote) 
 
![Facebook poll in a group for coders](/images/fb_poll.png) 
 
### Result from the Facebook poll 
From our poll, the target group says they *implement monitoring and metrics depending on the type of project*. Second highest target group identified with the option *always implementing monitoring and metrics, having full control of what's going on in their IT-system*. 
The image shows the result of the poll. 
 
#### Feedback 
When doing the poll we also got some feedback in the comments indicating that there seem to be developers that have passion and are experts in monitoring and metrics. We also got feedback that some IT-systems suffered from implementing monitoring.  
Their experience was that monitoring isn't just about pulling statistics but it is a matter of choosing wisely and even taking in experts to get it right otherwise, it can have an opposite effect. One commented that their IT-system had experience of metrics showing data that lead in the wrong direction and taking time away from doing actual debugging. 
 
### Indication from a survey targeting professionals having insight to IT-systems 
 
We also did a survey to get further insights into how monitoring is used in IT-companies. 
 
The survey was targeting professionals working within IT-companies.¤  
In our survey 75% says that they use some kind of monitoring systems like Grafana/Kibana etc. 
For those saying they don't use monitoring system "Lack of time" (2 in total) was the main reason why they haven’t implemented it. 
For those using monitoring 50% says they have been involved implementing monitor systems in their company. 
 
On the question: Have your IT-system ever gone down or not functioned correctly without your knowledge? 50% using monitors systems say yes. 100% not using monitor systems answer positively to this question. 
 
#### How much insight would you say monitoring give to your IT-system? 
 
[![https://gyazo.com/a2a08275bd63f29522a4c2d6dc99db6e](https://i.gyazo.com/a2a08275bd63f29522a4c2d6dc99db6e.png)](https://gyazo.com/a2a08275bd63f29522a4c2d6dc99db6e)
 
*To the left - no insight. To the right - 100% insight.* 
 
### Negatives with monitoring IT-systems 
 
Of those using monitor system 50% say they experience no negative impact having it implemented. 
50% answers it has some negative impact. 
 

[![https://gyazo.com/6b9bb280f54f199592bdd46c06cf4f13](https://i.gyazo.com/6b9bb280f54f199592bdd46c06cf4f13.png)](https://gyazo.com/6b9bb280f54f199592bdd46c06cf4f13)
 
*To the left some negative impact. To the right no negative impact.* 
 
Giving the reason "overhead in maintenance", "extra overhead" and "risk sending sensitive data when monitoring is outsourced" as the negative or con of using monitoring system. 
 
For those having monitoring systems implemented we asked which part of the system they thought was the most important to monitor: 
 

[![https://gyazo.com/6c5f35e5ca81aae4502bde08042e6122](https://i.gyazo.com/6c5f35e5ca81aae4502bde08042e6122.png)](https://gyazo.com/6c5f35e5ca81aae4502bde08042e6122)
 
*¤When writing this blog post only 8 professionals have taken the survey. The statistics will be updated. [Full survey](images/survey_results.pdf)* 
## Consequence of running in the dark 
Neglecting your system can either result in no changes or critical failures, however knowing if either case applies is impossible to quantify, as you won't know until you pay attention to the system, some developers feel it's not worth paying attention to the system, as the system's lifespan is too short or simple to require such care. Others believe they don't have enough time to pay attention as other things take focus in their work, but the worst case is developers too arrogant about their abilities to make "flawless" systems that they see no need to pay a close eye on their fully functional work.   
Whatever your reasoning may be, it's important to remember that we as humans are prone to produce errors, and it's in our best interest to pay close attention to our own mistakes, so we can avoid problems with our systems. 

Another consequence is if you have a agreement with another company it is important to be able to prove their requirements are meet. Without being able to observce if the requirements are meet, you will not be able to prove it. This is typically important if a Service level agreement has been made. Then it is especially important to be able to prove their requirements are meet, which is very hard if not observed.
 
## Solution 
There are more ways to solve this specific issue, but the most common and standard way in the industry is by doing real-time monitoring. Monitoring can be set up with real-time logging with the help of an example: [ELK stack](https://www.elastic.co/webinars/introduction-elk-stack) or capturing important metrics. 

Important metrics vary from company to company, in some cases a service level agreement can be made. To solidify if requirements are meet or not. This way you can monitor the customers requirements and this way prove they are meet. Otherwise it is up to the development team to choose which metrics are important. This can potentialy lead to some cons of monitoring. If not handled correctly, alot of noise can be created. A surplus of unimportant metrics, false alarms and more can create alot of noise and actully diverge ressources from actual debugging or other important work, such as development of another important feature. This con is typically present when developers with low experience in monitoring implementing it.

The specific solution that we will look at here is leaning towards capturing important metrics and displaying them in a graphical dashboard which can be watched. This way you can in real time see changes to these metrics which can help inform of how the system is actually doing right this moment. 

Examples of these would be: 
- How many requests does my website get. This could be important to know when to scale up, if performance limitations are known.
- How many threads are my program running. This could be important to know when to scale up, if hardware limitations are known.
- How much space is left on the hard drive which my database is running?. This could be important to know if diskspace limitations are known.
If ignoring one of these examples, it could potentially lead to: Customers unable to access website, backend slowing down or chrashing cause of hardware limitations, database chrash or not saving new data.

There are many other cases which this can be applied to. This will provide a good way to know exactly how every inch of a system is doing at any time. 

There are other monitoring which can come out of the box, an example of this is Digital ocean and amazon's cloudwatch monitoring systems. They are monitoring the VM's which is setup. However these do not monitor specific actions within the programs that are running in the machine. If per say, that an important metric is something that is only obtained by observing how a process is doing. We will have to implement a way for us to observce whats going on inside the process. This can be done in more ways than one.
 
There are more ways to implement metrics monitoring, this solution which we will present, will use Prometheus in conjunction with grafana. 
- [Prometheus](https://prometheus.io/): A database good at treating time-series data. 
>- The database comes with a feature that can call a http endpoint at ```ip:port.../metrics``` the metrics. 
- Pros of prometheus: 
>- It is open source, and therefore free
>- It is not to troublesome to setup. (According to our experience)
>- It can store alot of data without taking up much space. Key value storage.
>- Easy to use
>- Reliable when setup
- Cons of prometheus: [1]
>- It is limited to time series data, this means it does not support logs.
>- It is limited to HTTP, which can be slower than a level down: TCP
>- Scaling becomes an issue in large developments 
>- It is taking time to implement into the actual application to setup monitoring metrics and what should be exposed, a few metrics come out of the box. (In our experience, the most wanted metrics is custom ones you'll need to make)
>- All metrics endpoints have to be reachable for the prometheus poller, implying a more elaborate secure network confugration.[1]
>- It is taking up additional computational power (Potential ressource to run the actual service)
We will be using prometheus to store metrics and to scrape metrics endpoints for that data to be saved.

- [Grafana](https://grafana.com/): A User Interface good at representing time-series data in graphs. 
![https://www.rittmanmead.com/blog/content/images/2017/01/05.-Prod-Performance-Analytics.png](https://www.rittmanmead.com/blog/content/images/2017/01/05.-Prod-Performance-Analytics.png)
>- Grafana is a Tool which setup a webapplication for use, to create dashboards to represent time series data in graphs. This will be the place to monitor the system.
- Pros of Grafana [2] [3]
>- It is opensource and therefor free to use.
>- It is not to troublesome to setup (According to our experience)
>- It is user friendly (Simplicity) 
>- It has alot of features
>- It has a big community 
>- It has alot plug-ins available for use.
>- It is supporting alot of different datasources (Prometheus included)
>- It is nice to look at (According to us)
- Cons of Grafana:
>- It requires a good design to not screw up on how to represent the data.
>- It requires time to setup dashboards
>- It is taking up additional computational power (Potential ressource to run the actual service)

These implementations are open source and therefore free to use.  
This is a guide for the solution: [Guide](https://github.com/vegasbrianc/prometheus) 

Is this monitoring a good solution?. According to mutiny, it is. They provide 6 reasons why IT monitoring is important to a business. 
[Mutiny's 6 reasons](https://www.mutiny.com/news/blogs/2016/6-reasons-why-IT-monitoring-and-reporting-is-important-to-your-business/) 

However, these 6 reasons should be taken with a grain of salt. Mutiny is a company who sells monitoring systems to firefighters, security firms, average companies and more. But their opinions and reasoning is still very compelling, according to us.  

Monitoring seems essential when you take everyday metaphors as examples, but it ain't so simple in reality, monitoring can also give you the wrong information even when you set it up perfectly, as the metric can be full of errors resulting in even more damage, when you trust the monitoring system too much. Everything has to be handled with care, and monitoring is another step in a chain of systems, that can be affected by human error on a daily basis, it's important to remmeber that monitoring can be as good and bad as you make it, and it's by your own hand that the system supports or undermines your operation.
 
## Gains 
From our own observation during one of our own student project, having a Prometheus and grafana system setup gave a great overview, although some tweaking for what data we saw was needed. Seeing the system's performance and having warnings notify the phone about system crashes was a huge help.   
Being able to both actively and passively monitor the system's performance ensured our systems uptime, as this was important for an above 95% uptime SLA metric we had to uphold. By actively monitoring the performance of our system, we noted that we slowly but surely weren't able to handle the amount of data we received, had it not been for monitoring we wouldn't have known this, and we wouldn't have been able to identify the issue was with the database, since we queried too much data too and from it. This is a prime example of how helpfull monitoring was for us.   
The issue was a human flaw in our understanding of relational databases, as we asked the database for many queries that by our research should work. However, we did not take into account that the lack of Foreign keys would result in such extreme slowdown, as we didn't notice these issues from our initial testing with smaller sets of data.     
Observing the performance enabled us to solve this and many other issues as they appeared, as anytime we observed abnormalities we would investigate the cause, with the help of monitoring we had a better idea of where these issues came from.   
One specific moment wasn't an issue in the general term, we observed from our teachers monitoring that our system was starting to slow down very slightly. Everything seemed alright on the performance of our local systems so we had to pinpoint what change could have resulted in this change, which resulted in the discovery of a recently implemented feature incidental had send our systems entry point further away from it's original position physically, resulting in slower response time that made the system just a tiny bit slower.   
Monitoring doesn't solve issues but it alerts the developers about the issues, we personally don't know how we would have found these issues as it's mostly not related to code, which is the primary way for programmers to debug issues, but the issues that appear where when multiple systems interact with each other.   
 
## Conclusion 
System failures are the byproduct of human design as we humans are prone to produce errors without knowing it, in the current digital age this present problem, system failures can have minor impacts both financially and user satisfaction, or cripple corporations and even result in the loss of lives.   
Avoiding this as developers is our top priority, therefore the use of monitoring systems like Prometheus and grafana is indicating that, it is crucial for maintaining a system and avoiding future issues, or in the worst case stop the system before it does too much harm.   
Another benefit from monitoring is learning from mistakes that haven't happened yet, you know the saying "A fool learns only from his own mistakes. A wise man learns from the mistakes of others." we learn from mistakes that haven't happened yet by monitoring. With monitoring, you can to a certain extend predict the future. 

[1]:https://www.coscale.com/blog/prometheus-monitoring-pros-and-cons
[2]:https://grafana.com/grafana/testimonials
[3]:https://www.rittmanmead.com/blog/2017/01/time-series-visualisations-kibana-or-grafana/
