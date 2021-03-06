---
title: SEng 462 Stakeholder Update
date: "2021-08-18"
description:  Maximilian Cunningham (V00877737), Yuying Zhang (V00924070), Joseph Padayattil (V00951220)
---

Over this term, we have done a significant amount of work surrounding the use of satellite and remote sensing data, and how it can be leveraged by distributed systems. Our project initially evolved around how to use satellite imagery from the sentinel 2 mission. The second phase of the project was finding applications for different data sources, and how they could be integrated with a variety of distributed applications. Our group ran into some issues as we were working this term with regards to team composition. There were a significant number of students who dropped the course early in the terms, which led to shifting team composition as the term progressed. As a result, our group was not fully formed until the end of phase 1 of the project.  Each member in our current group was originally from a different team, however- we still managed to collaborate efficiently on all project deliverables and achieve productive teamwork.  

# Project Phase 1

## Platform and Methods Review Document

In order to work with large amounts of data within a reasonable time frame, extensive computing resources are necessary. Often, these needs are well above what an individual has at their disposal. As a result, we will be using cloud computing platforms for this project. These are services which rent out computing resources such as processing power and storage. The platforms we are considering are Compute Canada’s Arbutus, Colaboratory on Google Cloud, Cognitive Services and Data Lake Analytics on Microsoft Azure, and Amazon Elastic MapReduce.

In order to fully understand the types of statistics and indicators we can create throughout this project, we need to explore the data available to us. The Copernicus program, started by the European Space Agency, provides free, open access to a variety of data produced by a pair of orbiting, Sentinel-2 satellites.  Working with such a vast data set allows for a plethora of statistics and indicators to be created. The applications for these vary significantly, as the parties involved have different needs. From land monitoring that highlights the effects of climate change to disaster relief organizations, border surveillance, and maritime monitoring, the metrics are widespread and are highly varied in scope.  

For the purposes of this project, the focus will be on environmental and climate variables. Metrics involving the environment are important for both economical development as well as increasing sustainability by ameliorating the population’s carbon footprint.  The metrics created in this section includes: The Environmental Monitoring Metrics (EMM) which will be responsible for analyzing current environmental data and comparing this data with what has been previously collected in order to detect patterns, identify changes, and generate predictive models for the future; The Land Management Metric (LMM) which will be responsible for providing land-use information to support planning of urban and agricultural regions; and the Water Pollution Metrics (WPM) will analyze geospatial data for indicators of water pollution along coastal regions, wetlands and in-land lakes. 

## Test sites, data, and proposed architecture involving Arbutus and at least one other platform

![image](./metric.jpg)

Proposed test sites:
- Testing Site #1 - Mid Vancouver Island and Cathedral Grove
- Testing Site #2 - Thompson River Valley
- Testing Site #3 - Vancouver

Tools used for proof of concept:
- Python
- Rasterio for Visualization
- Google Collab

![image](./architecture.jpg)

## Initial results for 3 example properties

![image](./site1a.jpg)
![image](./site1b.jpg)
![image](./site2a.jpg)
![image](./site2b.jpg)
![image](./site3a.jpg)
![image](./site3b.jpg)

## Natural Asset monitoring prototype

Our created metric the Environmental Monitoring Metrics (EMM) will generate insight through utilizing information derived from a variety of indices such as:

Normalized Difference Vegetation Index (NDVI)
(B8 - B4) / (B8 + B4), where: B8 = 842 nm, B4 = 665 nm
Normalized Difference Index (NDI45M)
(B5 - B4) / (B5 + B4), where: B5 = 705 nm, B4 = 665 nm
Modified Chlorophyll Absorption Ratio Index (MCARI)
[(B5 - B4) - 0.2 * (B5 - B3)] * (B5 - B4), where: B5 = 705 nm, B4 = 665 nm, B3 = 560 nm
Soil Adjusted Vegetation Index (SAVI)
(B08 - B04) / (B08 + B04 + L) * (1.0 + L); L = 0.428 where: L is a soil brightness correction factor ranging from 0 to 1 L = 1 low vegetation cover, L = 0 high vegetation cover, L = 0.5 intermediate vegetation cover.

Through using the combination of results from relevant indices and assigning weights to each individual index, the EMM would produce results that more accurately reflects the environmental situation of a region.  

### Platforms used includes:

Google Colab

Google Colaboratory (Colab) is a hosted Jupyter notebook service that allows users to access computing resources, such as graphics processing units (GPUs) and Google’s tensor processing units (TPUs). Especially suited to data analysis, Colab allows users to execute Python 3 code on provided VMs.  Colab provides these resources for free, however there exists no guarantee on what underlying hardware is being used, nor how many resources are allocated.  

Copernicus Sentinel-2 Database

The Copernicus Open Access Hub  provides complete, free and open access to Sentinel-1, Sentinel-2, Sentinel-3 and Sentinel-5P user products, starting from the In-Orbit Commissioning Review (IOCR).  Sentinel-2 is a constellation with two twin satellites, Sentinel-2A and Sentinel-2B that conducts earth observation and systematically acquires optical imagery at high spatial resolution (10 m to 60 m) over land and coastal waters.

Architecture used:

![image](./architecture1.jpg)

Final testing site was Vancouver site, generated results based on our created metric is as follows:
![image](./result1.jpg)
![image](./result2.jpg)


## Natural Asset monitoring report and notes on future work

In terms of potential future work, the focus should be on refining the results generated by the unique Environmental Monitoring Metric (EMM), especially research into how to weigh the different component metrics more effectively to generate more accurate results.  This could be done through machine learning analysis, further discussion with stakeholders, as well as incorporating further remote sensing data analysis research into the project.  Another aspect of consideration would be the implementation of other created metrics through a calculated composition of preexisting metrics, and creating an effective evaluation strategy for such designed metrics.  


# Project Phase 2

## Mosaic Review 

Mosaic is a remarcable up an comming tool that takes advanatage of sentinel satalight imagery. It does theis by combing the satalight images in the best way possible in order to create a high resolution satalight image that can be easily used and queried. This provided an interesitng insight into how proprietyary information can be created, and how that infomration can be used in other tools. Our analysis of mosica incluses a description of how it was to use, as well as some suggestion that might improve it in the future.

## Decentralized and Democratized Modern Platforms 
This was an opportunity to use the experienced gained so far to propose a new design for a distributed system from scratch. This was a design that was based on local-first software and decentralized blockchain technology. Local-first software offers the advantages of cloud apps, while also allowing users to retain full ownership of the data they create, while a blockchain is an excellent way of recording and validating information, even among multiple systems. In this system, the primary copy of the data would be the copy stored on the user's device, rather than a centralized database. 

In terms of a modern decentralized and democratized distributed platform, there are a number of other technologies that have been used to approach distributed problems, and our implementation is designed to take advantage of some of them. Our design for a modern decentralized and democratized distributed platform for sharing of data and information is based on a local-first software structure and takes advantage of decentralised blockchain technology.  Local-first software offers the advantages of cloud apps, while also allowing users to retain full ownership of the data they create, while a blockchain is an excellent way of recording and validating information, even among multiple systems.

In our distributed platform design the copy of the data on the user’s local device would be referenced as the primary copy.  External servers still exist, however these servers would hold secondary copies of the data and work in updating and increasing accessibility of data to multiple devices.  Synchronization and concurrent collaboration of data would occur through the use of a decentralized blockchain system, where servers that make up the network will cooperate together on verification of transactions.  By keeping the primary copy of the data on the local device, there is never a need for the user to wait for a request to a server to complete. All operations can be handled by reading and writing files on the local disk, furthermore- data synchronization with other devices occurs in the background.

To ensure real time collaboration for shared data in a situation of multiple users, each user will have a local filesystem.  The focus on primary local data storage allows for users to quickly access the data and also work offline.  The server that supports the local device would frequently pull from the local device’s data storage in order to integrate new changes made on the local copies, these changes would then be updated into the secondary copies of the data stored on the server.  The local data storage would also pull from the distributed servers in order to assimilate changes made to the data by other accessing devices.  If the sync procedure malfunctioned, each user’s files would still remain unharmed on their local disk, and they could easily switch to a different syncing service.  Conversely, should the user’s computer hard drive fail, they can restore their work by simply installing the platform and waiting for it to sync by pulling secondary data stored in the distributed server system.

To increase the real-time synchronization proficiency of our distributed platform in multi-user cases, it will use the distributed systems algorithms called Conflict-free Replicated Data Types (CRDTs) for the storage and transmission of data. Essentially all data structures will be stored on the platform as CRDTs.  The CRDT algorithm can keep track of any changes that are made, and syncs the changes with other devices in the background when a network connection is available.  Furthermore, if a data state was concurrently modified on different devices, the CRDT merges those changes automatically, where the merged state contains all of the added items in a consistent order.  Given multiple users concurrently updating the same property of the same object; the CRDT data structure will be able to keep record of the conflicting values in the data.  By using CRDT as the method of data storage and transmission, our platform can achieve real-time synchronization and is an effective collaboration software that gives users full ownership of their data. 

Lastly, to ensure security and democratization of data, each remote server would service a number of devices, and each of these servers would be considered as a node in a decentralized blockchain system. Using blockchain technology can provide immutable data storage and access with the combination of Proof-of-Work verification.  Proof-of-Work in this case would be done by users of the platform who would review over the shared data and resolve any data conflicts due to concurrent data input from multiple users.  

The use of blockchain technology for our decentralized distributed platform involves using encrypted blocks of secondary data maintained in the distributed servers of the system, then chaining them together to form a chronological single-source-of-truth for the data.  Furthermore the user’s digital assets are distributed instead of copied or transferred, creating an immutable record of the data.  The decentralized nature of the data allows for full real-time access and transparency that preserves the integrity of the data on the platform.  

Our team’s designed decentralized and democratized distributed platform diagram:
![image](./demoplat.jpg)

When it comes to the use of the platform for industry use cases such as kelp industry monitoring, it can be leveraged for asset tracking so that kelp farms can monitor their crops to help optimize their growth. In this context, each of the local devices that are part of the platform would constitute an intelligent edge device, that is a smart sensor embedded within the crop that needs to be monitored. With the platform being leveraged in such a way by industrial IoT devices that can sense, communicate and store information about the kelp crop, and further use software applications that can perform analytics and derive valuable business information from the raw data that it collects, so that the farmer is able to optimize crop yields. 


## Architecture Design and Prototype Implementation for local Drone and/or Sensor data


Not every problem can be solved using a distributed system. There are often limitations on network availability, information security, and other similar issues that can prevent us from being able to use the large, pre-built or custom designed systems of distributed computers to solve difficult problems. Instead, in such cases, it may be necessary to rely on local solutions to problems. Using simple, less powerful local computing systems comes with some challenges and limitations that we would not face to nearly the same extent in a distributed system.

The problem of how to handle data being stored and used in local environments is one best solved not through the creation of a highly complex system, but rather, by attempting to find a simplified version of a problem that can be more easily solved at a local level. An example of this would be the issue of image recognition using drone footage. The computers that are available for such an item are definitely not capable of properly training and image recognition problems. Such applications often require thousands of hours of computing time to traine, and an immense amount of resources. With that said, once a model has been trained, the effort required to actually perform the recognition is comparably miniscule. For example performing image recognition on an image of size n * m would take time on the order of O(mn) rather than the incredibly large amount needed for training. As a result, an incredibly difficult problem can be solved in a local environment simply by relaxing the requirement on the local machine. 

The chosen problem for this stage of the project is the use of sensors distributed through an area, and the problem of how best to create an overlay of a “heat map” demonstrating the sensor data values over an area. 

By using the output heat map, and combining it with satellite image data using python, we can create the following image overlay:

![image](./heatmap.jpg)


While this does not use actual data, and instead uses arbitrary data, this is not a true representation of the area. With that said, we could relatively easily create a more elevent version of this by taking temperature data from environment canada monitoring stations, then normalizing it and doing the steps described earlier to make a genuine heat map of the victoria region.

