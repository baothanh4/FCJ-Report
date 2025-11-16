---
title: "Week 8 Worklog"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:
* Understand the fundamentals and use cases of AWS Step Functions, including its 7 core state types and how to orchestrate complex workflows.

* Gain hands-on experience creating and testing workflows in AWS Cloud9, focusing on task orchestration and error handling.

* Learn the key features and deployment steps of Amazon FSx, including its different variants (Windows File Server, Lustre, NetApp ONTAP, OpenZFS).

* Practice configuring an FSx file system integrated with AWS Managed Microsoft AD, ensuring proper setup of networking, authentication, and file sharing.

* Explore AWS X-Ray to understand how to trace and visualize requests across distributed applications for performance optimization and debugging.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn **AWS Step Functions**: <br>&emsp; + 7 states: Task state, choice state, a fail or success state, pass state, wait state, parallel state, map state <br>&emsp; + Uses cases to use AWS Step Functions <br>&emsp; + Benefits of AWS Step Functions                                                                                                   | 26/10/2025 | 27/10/2025      |<https://000047.awsstudygroup.com/1-intro/>
| 3   | - **Practice:**<br>&emsp; + Create **Cloud9** enviroment <br>&emsp; + Create sample services <br>&emsp; + Initialize workflow <br>&emsp; + Error handling                                             | 27/10/2025 | 28/10/2025      | <https://000047.awsstudygroup.com/1-intro/> |
| 4   | - Learn **Amazon FSx**: <br>&emsp; + FSx for Windows File Server <br>&emsp; + FSx for Lustre <br>&emsp; + FSx for NetApp ONTAP <br>&emsp; + FSx for OpenZFS  | 28/10/2025 | 29/10/2025      | <https://000025.awsstudygroup.com/> |
| 5   | - **Practice:** <br>&emsp; + Configure File system details <br>&emsp; + Choose existing VPC  <br>&emsp; + Choose AWS Managed Microsoft AD(Provide DNS name of domain, Service account username and password) <br>&emsp; + Define Windows file share name(Choose AWS Managed Microsoft AD) <br>&emsp; Review and create                            | 29/10/2025 | 30/10/2025      | <https://000025.awsstudygroup.com/> |
| 6   |- Learn **AWS X-Ray**: <br>&emsp; + Trace <br>&emsp; + Segment <br>&emsp; + Subsegment <br>&emsp; + Annotation / Metadata <br>&emsp; + Service Map                                                                                      | 30/10/2025 | 31/10/2025      | <https://000140.awsstudygroup.com/> |


### Week 8 Achievements:
* Successfully learned and explained the 7 states of AWS Step Functions, including how each contributes to workflow automation and state transitions.

* Practiced building a sample workflow using AWS Step Functions in Cloud9, implementing error handling and validating execution flow.

* Gained a solid understanding of the different Amazon FSx options and their ideal use cases for Windows workloads, high-performance computing, and enterprise storage.

* Completed hands-on setup of an FSx for Windows File Server, including file system configuration, VPC and AD integration, and file share creation.

* Learned how AWS X-Ray collects traces, segments, and subsegments, and visualized a Service Map to identify performance bottlenecks and errors across AWS services.
