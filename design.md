# design.md

## System Architecture Overview

LumosRoad follows a **mobile-first, cloud-backed architecture** optimized for scalability and low latency.

---

## High-Level Architecture

**Client (Mobile App)**

* Android-first (Flutter / React Native)
* Offline caching for maps & routes

**Backend (AWS)**

* API Gateway
* Lambda-based microservices
* DynamoDB for user & route metadata

**AI & Data Layer**

* Route Risk Scoring Engine
* Anomaly Detection Model
* Historical + real-time data ingestion

---

## Data Sources

* OpenStreetMap
* Government accident & road data
* Crowd-sourced user feedback
* Time-based environmental signals

---

## AI Components

### 1. Route Safety Scoring Model

**Inputs**

* Road type
* Lighting availability
* Accident frequency
* Time of travel

**Output**

* Normalized Safety Score (0–100)

---

### 2. Anomaly Detection (Guardian Mode)

**Approach**

* Time-series behavior modeling
* Rule-based + ML hybrid

**Triggers**

* Unplanned long halt
* Sudden direction change
* Missed check-in

---

## SOS Flow Design

1. User taps SOS
2. Backend fetches live location
3. Alerts emergency contacts
4. Continuous tracking until resolved

---

## Privacy & Security Design

* Location data encrypted at rest and in transit
* Guardian Mode data auto-deleted after session
* User-controlled data sharing

---

## Scalability Plan

* Serverless infrastructure
* Region-based data partitioning
* Offline-first UX for rural areas

---

## Future Enhancements

* Integration with government emergency systems
* Voice-first navigation in regional languages
* Community-driven road safety feedback

---

## Design Philosophy

**Safety > Speed > Convenience**
Built for Bharat, grounded in real-world road conditions, and designed to protect first.
