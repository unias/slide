---
layout: singleslide
title:  "论文介绍：Next generation cloud computing: New trends and research directions"
date:   2017-12-25 00:45:41 -0700
categories: "slide"
---

<style type="text/css">
.floatleft{float:left;width:40%;}
.floatright{float:right;width:60%;}
</style>


<textarea id="source">

class: center, middle

# Next generation cloud computing: New trends and research directions

&nbsp;
&nbsp;

#### Future Generation Computer Systerms, Volume 79, February 2018 
##### Blesson Vargese, Rajkumar Buyya
##### Queen's University Belfast, UK 
##### The University of Melbourne, Australia
#### 2017-12-25


---

## Overview
<div style="text-align: center">
<img src="/slides/assets/images/2017_12_25/overview.png" style="width:85%;height:85%">
</div>
---

## Outline

- Changing infrastructure

- Emerging computing architectures

- Avenues of impact

- Research directions

---

## Changing infrastructure
- Multi-cloud

    - Hybrid cloud: a combination of public and private clouds or a combination of public and private IT infrastructure. These clouds cater for bursty demands or resource demandsknownbeforehand.

    - Federated Cloud: bringing together different cloud providers under a single umbrella resulting in a federated cloud. Federated clouds can address the vendor lock-in problem in that applications and data can be migrated from one cloud to an- other.

- Microcloud and cloudlet
    
    - There are recent efforts to decentralise computing towards the edge of the network for making computing possible closer to where user data is generated. In a decentralised cloud computing ap- proach, application tasks will need to be offloaded both from data centers and user devices on to microclouds.

---


## Changing infrastructure
- Ad hoc cloud 

    - Ad hoc computing has existed from the grid era. The context of an ad hoc cloud is changing with,
    increasing connectivity of a large variety of resources to the cloud. This is becoming popular for smaller mobile devices, such as smartphones, which on an average have less than a 25% per hour of usage. These devices may be used in conjunction with existing data centers to enhance connectivity.

- Heterogeneous cloud
    
    - Different types of processors are combined to offer VMs with heterogeneous compute resources. The key challenge is achieving a high-level abstraction that can be employed across multiple architectures, such as GPUs, FPGAs and Phis.

---
## Emerging computing architectures

- Volunteer computing

    - The availability of compute resources is not guaranteed in an ad hoc cloud or cloudlet as in a conventional data center and therefore a pay-as- you-go or an upfront payment for reserving compute, storage or network resources will not be suitable.

    - In volunteer computing, users of a social network may share their heteroge- neous computing resources in the form of an ad hoc cloud. This is referred to as ‘social cloud computing’. More reliable owners are rewarded through a reputation marker within the social network.

    - Challenges: how to minimise the overheads for setting up a highly virtualised environment given that the underlying hardware will be heterogeneous and ad hoc. Moreover, there are security and privacy concerns that will need to be addressed to boost confidence in the public to more readily become volunteers for setting up ad hoc clouds.

---
## Emerging computing architectures

- Fog and mobile edge computing

    - Fog computing is to leverage the existing compute resources on edge nodes, such as mobile base stations, routers and switches, or integrate additional computing capability to such (network) nodes along the entire data path between user devices and a cloud data center.

    - Mobile Edge Computing is similar to fog computing. However, it is limited to the mobile cellular network and does not harness computing along the entire path taken by data in the network.

    - Challenges: Firstly, complex management issues related to multi-party service level agreements, articulation of responsibilities and obtaining a unified platform for management given that different parties may own edge nodes. Secondly, enhancing security and addressing privacy issues when multiple nodes interact between a user device and a cloud data center.

---
## Emerging computing architectures

- Serverless computing

    - Serverless does not mean that computing will be facilitated without servers. In this context, it simply means that a server is not rented as a conventional cloud server and developers do not think of the server and the residency of applications on a cloud VM.

    - Advantages: developers do not need to care about the deployment of an application on a VM, over/under provisioning of resources for the application, scalability and fault tolerance do not need to be dealt with. The infrastructure, including the server is abstracted away from the user.

    - Challenges: developing programming models that will allow for high-level abstractions to facilitate serverless computing.

---
## Emerging computing architectures

- Software-defined computing

    - Software Defined Networking (SDN) is an approach of isolating the underlying hardware in the network from the components that control data traffic. This abstraction allows for program- ming the control components of the network to obtain a dynamic network architecture.

    - With emerging distributed cloud computing architectures,‘software defined’ could be applied not only to networking, but also to storage and compute as well as resources beyond data centers for delivering effective cloud environments. This concept when applied to compute, storage and networks of a data centerand resources beyond is referred to as Software Define Computing (SDC). This will allow for easily reconfiguring and adapting physical resources to deliver the agreed QoS metrics. The complexity in configuring and operating the infrastructure is alleviated in this case.

---
## Avenues of impact

- Connecting people and devices in the Internet-of-Things Innovation

    - Innovation in the cloud arena along with prolific growth of the sensors and gadgets is bringing people, devices and the associated computing closer. 

- Self-learning systems

    - Currently, a large volume of user generated data in the form of photo, audio and video and metadata, such as network and user activity information, are moved to the cloud. There is ongoing research in applying machine learning to speech/audio recognition, text, image and video analysis, and language translation applications. 

    - A related avenue in future clouds is Cognitive Computing. Cognitive systems will rely on machine learning algorithms and the data that is generated to continually acquire knowledge, model problems and determine solutions. Examples include the use of IBM Watson for speech and facial recognition and sentiment analysis. It is anticipated that these architectures will be integrated in next generation clouds.

---
## Avenues of impact

- Big data computing
    
    - The data that is stored may never be used again and is often referred to as dark data. It is usually expensive to move data out of the store and perform any analytics. The opportunity to process data is before it is stored in the cloud.

    - As the cloud infrastructure becomes decentralised, more opportunities unveil to facilitate processing closer to where it is generated before storing it. However, existing research in big data usually considers centralised cloud architectures or multiple data centers.

- Challenges
    
    - Data processing and resource management on distributed cloud nodes.

    - Building models for analytics that scale both horizontally and vertically.

    - Software stacks for end-to-end processing.

---
## Avenues of impact

- Service space

    - The abstraction of infrastructure, platforms and software were initially offered as services (IaaS, PaaS and SaaS) on the cloud.How- ever, the service space is becoming richer with a wide variety of services.

    - **Acceleration-as-a-Service**: to offer acceleration provided by GPUs to applications. Further, a wider variety of accelerators, such as coprocessors, FPGAs and ASICs (such as Tensor Processing Units (TPUs) need to be integrated in future clouds to enable computing in device rich environments.

    - **Container-as-a-Service**: container monitoring, live migration, security aspect will need to be developed. Dealing with dependencies and the portability of containers remains an open issue.

    - **Function- as-a-Service**: This is in contrast to current execution models in which an application is constantly running on the server to furnish a client request and is billed even when the server application remains idle when it is not servicing requests.


---
## Research directions
- Guaranteeing enhanced security

- Achieving expressivity of applications for future clouds Expressing

- Developing a marketplace for emerging distributed architectures

- Offering efficient management strategies in the computing ecosystem

- Ensuring reliability of cloud systems Reliability

- Building sustainable infrastructure for the future

---
## Research directions

<div style="text-align: center">

<img src="/slides/assets/images/2017_12_25/direction.png" style="width:40%;height:40%">

</div>
---
class: center, middle

# Thanks

</textarea>
