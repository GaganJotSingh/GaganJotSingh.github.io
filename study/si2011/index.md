---
layout: page
title: Summer Internship - 2011
description: Summer Internship duing Bachelors
---

### Anonymization of Network Trace Data for the Homework Project

**Supervisor:** [Prof. Joe Sventek](https://www.cs.uoregon.edu/People/Faculty/Joe_Sventek.php){:target="_blank"}

**Advisor:** [Mr. Alexandros Koliousis](http://www.doc.ic.ac.uk/~akolious/){:target="_blank"}

**About:**

[Homework](http://homenetworks.ac.uk/){:target="_blank"} project studied the use of computer network in the home and investigated future networking.
Based on the use and the needs of the user, it led to a fundamental re-invention of the protocols, models and architectures of the domestic setting.
For research purposes, home network trace data was collected.
The project was a research collaboration between the Universities of Nottingham and Glasgow, Imperial College London and Georgia Institute of Technology with industrial partners Microsoft Research (Cambridge) and BT.

**Abstract:**

It is very difficult to manage various aspects of the home networks.
The Homework Project aims to help non-expert users in this task by monitoring and visualizing various aspects of the home network using stream database concepts.
The tools developed in the Homework Project automatically collect and store the home network trace data in the form of log files.

These logs are collected and explored to investigate the behaviour of computer and network systems.
Releasing network measurement data, including packet traces, to the research community is a virtuous activity that promotes solid research.
Because traces are expensive to store and collect, and because it is desirable to replicate experimental results, it is common to publish trace data for use by other researchers.
However, due to the risk of exposing sensitive information (e.g. IP addresses, MAC addresses, etc) to potential attackers, sharing does not occur to the degree that is desired.
To eliminate the exposure of sensitive information, traces are usually anonymized before publication.

Anonymization of network traces is very important in today’s world of sharing data for research purposes.
The main objective of this project is to anonymize the network trace data collected in the Homework Project.

Anonymization is the process of removing sensitive information from the raw data and is used to sanitize logs before their release.
Various tools have been developed for the anonymization of network trace data by **CAIDA**.
Some well-known tools include *tcpmkpub*, *flaim-nfdump*, and *SCRUB-tcpdump*, each proposing various anonymization techniques.
This report describes many of these anonymization methods for different attributes of the network trace data; in addition, it describes the implementation of tools that apply a subset of these methods to IP addresses, MAC addresses, port numbers, protocol numbers, timestamps, and hostnames in the Homework trace files.
The ultimate goal of anonymization of these attributes is to minimize exposure of sensitive information while maintaining critical correlations between data in the various trace files, so that the anonymized data does not loose it's use to the researchers.
Adhering to this goal, anonymization should preserve as much information as possible, should be irreversible and not unnecessarily increase the size of trace files.
Efficiency of the anonymization process is not an important goal as it is performed only once on a trace.
