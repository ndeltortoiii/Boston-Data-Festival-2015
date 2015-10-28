#Data Protection Law

omnibus data protection laws

The privacy act, don’t have omnibus broad based legislation used by the private sector

Germany: employer, lender, legislative, and constitutionally protection

on average 1200 pieces of data on each person in US
#International Laws
Convention #108
OECD Guidelines

#Standards
*27000 Thousand Series Standard: Security information
*27018 Protection of Personal Information in the Cloud
**Companies can get certified as well as audit provision
**not a legal requirement
**Takes traditional data laws

#PII: Personally Identifiable Information
#Privacy by design
#Right to be forgotten

#Theory on driver
*People began to turn away from american products because of privacy weakness

#One way ratchet
*Data minimization

#Trends
*Where is the data: Laws geographically based

#Privacy Tools project at Harvard: Social Science Database protection

#anonymizing data and protection of re-identification of data

#adopt federal and legislative protection

#In Europe sees data protection as a human right
*directive for data protection: EUI

#Marketing and getting access to data (experion)
*European Data Protection Law has to get permission of the user
*micropayment individuals should be remunerated for personal information
—————————————————————————————————————————
#Visions from the Internet of Things
#Chad Jones Chief Strategy Officer, Deep Information Sciences
#Vision of Future
*Gartner Hype Cycle 2015
*The Opte Project: mapping the internet through visualization through IP Address mapping with clusters of networks

#Intelligence Everywhere
*advanced, pervasise, invisible analytics
*Context Rich Systems
*Smart Machines

#Fog Computing: anywhere along the chain of computing you can have a point of process
*set more process locally and everywhere in between

#Build with purpose: Shawn Lorenz
*1. Identify Business Case
*2. Create a connected object
*3. Build Infrastructure
*4. Create Applications
*5. Business Systems Integration
*6. Analytics & Automaton: Stream Processing
*7. Service and Support

Use Case: Nest Protect and ecosystem 

#A Different Use of Machine Learning
*machine learning database engine: adaptive database kernel and information orchestration system that leverages machine learning to evolve the database: MySQL: observer, analyze , predict, adapt, orchestrate , optimize
*scale and performance: true relational HTAP concurrent OLTP and OLAP 
*Relational Database e for the IoT: allow objects data to more easily interconnect, real time observations on data sets as they occur
*machine learning in engine itself

*Carbon Based

#U of W Ambient Backscatter, Flexible Battery, Wireless Electricity
——————————————————————
#Yan Zhang: Advanced data Analytics in IOT applications concepts and tools
*data 
*what should i do: automation, recommendation
*what will happen 
*why did it happen
*what happened: people and insights
*move toward decision and action

#agenda: concepts, IOT: where the analytics happen, challenges, tools and emo: predictive maintenance use case

#The old machine learning landscape: high bar, limited applications
*expensive hardware investment: big data challenge
**data collection and storage
**processing of large volume of data
**handling high speed data streams
*Limited Expertise: lack of data science experts
*disconnected tools: data scientists use different languages eg R, python from the rest of the development team different from python
*Deployment complexity: many models never achieve business value due to difficulties wth deploying to production

#ML for ambient intelligence: target to apply ML in everything
*Cloud: expensive hardware investment: Platform as a service: (PaaS), 
*Predictive API: cloud based ML web services that help analyze data for different predictive tasks e.g. retail forecasting, customer sentiment analysis, recommendation engine

#What is IoT
*Things data is generated, transmitted, stored, and shared | advanced analytics is performed | action is taken to improve how the things work
*analysis and storage happens in the cloud

#IoT is an Inflection Point
*hardware is cheap, connectivity is pervasive, development is easy, huge benefits fuel demand, new innovative scenarios
*example is predictive maintenance

#home automation: smartthings, revolv, belkin wemo, phillips hue, zigbee, z wave
#smart lighting: cloud, hub gateway, PAN: ZigBee, lets you know whether light is on or off
*IoT Applications in different categories can required very different hardware applications

#Where can analytics happen
*mobile app, home gateway hub, edge node (multi sensor data fusion), cloud

#optimization and prediction provides the greatest value for IoT data

#beneficial analytics in the cloud: make use of historical data, multiple source from surrounding things, more processing power, optimization and prediction

#Challenges—Analytics solution in the cloud
!!!*CRISP-DM Model
*latency due to network
*security (maliciious intrusion, data security)
*one stop shop for data ingestion, data storage, data stream analytics

#Cortana Analytics Suite

#Power BI dashboard to consume the data

#predictive maintenance concepts: goal improve production/maintenance efficiency
*data stream (time varying features), multiple data sources
*scope: component level, system level
*1. problem is predictive in nature, 2. Data is relevant, with sufficient quality
——————————————————
#enterprise iot: network of systems of connected devices, multiple user groups, situational awareness, corporate intelligence, mission critical
#How to realize value (question not how do we access data):
#The Data Prizm
*data ingestion (bluetooth LE, NFC, Zigbee) fro devices
*Automation and visualization
**Eddge Analytics (Cisco, Intel, ARM): device automation, communication, even driven alerts & actions
**Stream Analytics (Amazon AWS, Microsoft Azure): system automation, dashboards, performance monitoring, tactical decision support, sequence of events driven
**Deep Analytics (python, R: trend analysis, pattern recognition, data correlation, performance evaluation, strategic decision support
*Analytics Platforms (Splunk, Hadoop, Cloudera)

#ability to respond to data driven commands: ground up collaboration, business leaders, system architects, engineers, developers, data scientists
need to use feedback loop

#Realizing Stream Analytics: operations processes automation
*define outputs, establish business rules, define workflows, develop visualizations interfaces

#digging deeper from data
*infrastructure: accumulation, storage, retrieval, experienced, data scientists, creativity, business insights
*accumulation with proper storage and compliance

#Joining all 3

#intrinsic skills to look at massive trends and what questions could be asked, not just querying data
#partner with industry experts

#design considerations
*3 vs of big data: volume, velocity, and variety
*consider: mobility, form factor (size), communication, safety, environment, cyber security
———————————————————
#Analysis & Visualization Techniques for Environmental IoT Systems Rob Purser (MATLAB)
*collection without analysis has negative ROI
*”Most IoT data are not used.  Only 1 percent of data from an oil rig with 30,000 sensors is examined”
*MATLAB, Simulink (control systems), ThingSpeak (data aggregator)
*Projects: Counting Cars: Edge Node Analytics

#Analytic Workflow
*edge nodes: local embedded algo, data reduction communicates with data aggregator (online analysis, visualization, and reporting) connected with exploratory analysis (historical analytics & algorithm development [where matlab is used])
*!!How can I build out edge nodes that feed in clean data

#edge node analytics: http://goo.gl/KGdofK
*embedded devices have always used: signal processing, matrix math, closed looop control
*powerful mobile processors enable: sensor fusion, trained machine learning, statistical modeling, small vocab voice recognition
*RaspberryPI
*Blob Analysis
*FPGA

#processing and performing analytics everywhere throughout the system

#!!median filter to clean the data best option, overlaid with expected levels (based on median at a given time), normalized based on first 3 hours after normalized (polynomial fit of expected noise levels, move polynomial up or down to compensate for variation (get conditions that would cause differences), identify alarm conditions > 1 std deviation above expected (not getting false positives), to do: investigate what happened
*windowed median filter with 15 minute window, used heavily in industrial automation
*contrast with mean filter with same window
*smooths out highs and lows

#keep in mind: median filter friend, you haven’t seen all the scenarios, always convert to on line analytics, pipeline

#Tide prediction — Online Analytics: http://goo.gl/uXHkYU “Tide matlab thingspeak
*on-line analysis: hysteresis and stat machine to avoid being to “tweekative” Ockway bay
*analysis happens at every stage
*dependatble, real-work online analytics take tiem to develop tune and test
rob.purser@mathworks.com @rpurser47
http://slides.com/rpurser/environmental_analysis





