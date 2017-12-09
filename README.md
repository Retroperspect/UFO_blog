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
- System failures are the byproduct of human design as we humans are prone produce errors without knowing it, in the current digital age this present problems as system failures can at best have minor impacts both financially and user satisfaction, and at worst cripple corperations or even result in the lose of lives.  
Avoiding this as a developer is our top priority, therefor the use of monitor systems like prometheus and grafana is crucial, for maintaining our system and avoiding future issues, or in the worst case stop the system before it does too much harm.  
Another benefit from monitoring is learning from mistakes that havn't happened yet, you know the saying "A fool learns only from his own mistakes. A wise man learns from the mistakes of others." we learn from mistakes that havn't happened yet by monitoring.
