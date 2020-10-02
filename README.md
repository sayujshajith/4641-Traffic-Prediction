Traffic Predictions with Uber Ride Data
=======================================
Swapnil Lad, Minrui Liang, Dean Long, Sayuj Shajith, Arnold Wang
----------------------------------------------------------------
Accompanying video presentation: 

https://web.microsoftstream.com/video/39cbb826-8d85-47f2-b95c-45ec666d6a8f

**Introduction**
Many problems of urban transportation begin and end with traffic. Traffic is responsible for increased pollution and increased wait times, and unpredictable traffic can cause complications in personal matters. The ability to accurately predict when traffic will flare up can increase the reliability of trip time estimates, reducing some of the societal friction incurred in-transit by urban and suburban road travelers. 
	Nowadays, a not insignificant percentage of vehicles on the road are vehicles for hire. Companies like Uber pay ordinary vehicle-owners to act as taxis for users of the Uber phone app. Uber and its competitors have an additional incentive to accurately predict trip times: they need to fairly compensate their drivers for their time and fuel. 
 
**Problem Definition**
Uber has released data representing a significant portion of the billions of trips booked on their platform from the past few years. Averaged data for all Uber trips departing from a particular origin and arriving at a certain destination over a given time frame can be downloaded in hourly, daily, monthly, and quarterly resolutions. Among the provided statistics is the mean trip time for the origin and destination pair. How can we use past trip data to make consistent and accurate predictions of trip times booked today or tomorrow? 
 
**Methods**
	The origin and destination pair format of the trip data naturally presents itself for analysis as a graph. Some trips dominate (contain) other trips, so nuance lies in how the graph and the nodes it contains can be constructed to accurately reflect the geospatial character of the data encoded. We expect a relatively densely connected graph.
	We intend to implement a graph neural network and explore different objective functions while trying to produce a consistent and reasonably accurate regression for any given origin-destination pair. Graph neural networks are a state-of-the-art approach to analyzing graph-formatted data; there are many novel infrastructures to explore and fit to our problem of traffic prediction. Graph attention networks and Graph LSTM models seem particularly fit to the problem of trip time regression [2]. 
	Random forest algorithms are also a viable backup plan for producing results [1].
 
**Potential Results**
State-of-the-art initiatives in traffic prediction hover over 97% accuracy [4]. We expect to achieve predicted times that come within a reasonable deviation’s distance from the ground truth. Interesting exploration topics that build upon those results include using data other than past traffic data, such as weather, accident frequency, or local/seasonal events to provide more accurate regression of traffic patterns.
 
**Discussion**
Traffic analysis is a topic many are invested in. Google Maps provides a very robust implementation that many are familiar with. To a student, traffic analysis can be seen as a canonical regression problem; implementing a machine learning system to provide homegrown results is a practical and interesting project. The hope is to apply new techniques and innovative approaches towards solving a problem that affects so many.
 
 
**References:**

[1]Y. Liu and H. Wu, "Prediction of Road Traffic Congestion Based on Random Forest," 2017 10th International Symposium on Computational Intelligence and Design (ISCID), Hangzhou, 2017, pp. 361-364, doi: 10.1109/ISCID.2017.216.

[2] A. Abadi, T. Rajabioun and P. A. Ioannou, "Traffic Flow Prediction for Road Transportation Networks With Limited Traffic Data," in IEEE Transactions on Intelligent Transportation Systems, vol. 16, no. 2, pp. 653-662, April 2015, doi: 10.1109/TITS.2014.2337238.

[3]Y. Lv, Y. Duan, W. Kang, Z. Li and F. Wang, "Traffic Flow Prediction With Big Data: A Deep Learning Approach," in IEEE Transactions on Intelligent Transportation Systems, vol. 16, no. 2, pp. 865-873, April 2015, doi: 10.1109/TITS.2014.2345663.

[4] O. Lange and L. Perez. “Traffic prediction with advanced Graph Neural Networks,” on DeepMind.com, September 2020. Available: https://deepmind.com/blog/article/traffic-prediction-with-advanced-graph-neural-networks
