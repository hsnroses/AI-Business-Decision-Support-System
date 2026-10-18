# ai-engineering-ai-cyber-threat-detection-dashboard

# AI Cyber Threat Detection Dashboard

## Project Description

This project aims to develop an AI-powered cybersecurity dashboard that analyses network traffic data, identifies potentially suspicious activity, and displays detection results to support security monitoring.

## Problem Statement

Security analysts need to review network traffic and security logs to identify potential cyber threats. Large volumes of data can make manual investigation time-consuming. This project explores machine learning as a way to support threat detection and alert review.

## Evidence of the Problem

- CISA cybersecurity advisories provide information about documented cyber threats and recommended responses.
- The CICIDS2017 dataset provides labelled network traffic for intrusion detection research.
- Machine learning research investigates methods for identifying malicious network traffic.

Sources:
- https://www.cisa.gov/news-events/cybersecurity-advisories
- https://www.unb.ca/cic/datasets/ids-2017.html

## Initial Related Work

1. Snort — a rule-based network intrusion detection system.
2. Suricata — a network threat detection and inspection engine.
3. Machine learning-based intrusion detection research using datasets such as CICIDS2017.

The limitations of these approaches will be investigated further during the literature review.

## Engineering Gap

This project aims to integrate machine learning-based traffic classification with an API and dashboard so that users can review potential threats through a single interface.

## Initial Project Objectives

1. Develop and evaluate a machine learning model for network traffic classification.
2. Integrate model predictions into an API and dashboard.
3. Evaluate model performance using precision, recall, F1-score and false-positive rate.

## Target Users

- Security analysts
- Network administrators
- Cybersecurity students and researchers

## Proposed Data Sources

- CICIDS2017: https://www.unb.ca/cic/datasets/ids-2017.html
- UNSW-NB15: https://research.unsw.edu.au/projects/unsw-nb15-dataset
- MITRE ATT&CK: https://attack.mitre.org/

## Responsible AI Risks

- False positives may incorrectly flag legitimate traffic.
- False negatives may allow malicious activity to go undetected.
- Dataset limitations may reduce model performance on unseen networks.
- Sensitive network logs may create privacy and security risks.

## Weekly Progress

| Week | Activities | Status |
|---|---|---|
| Week 1 | Define the project scope, review initial sources, organise the repository, and document the proposed system. | In progress |
| Week 2 | Update this section with the actual work completed in Week 2. | Not started |
