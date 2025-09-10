# Data Engineer System Design Assignment

## Overview

You are tasked with designing a real-time analytics platform for a growing e-commerce company.

## Business Context

Our e-commerce platform currently processes 50,000 orders per day, with peak traffic during sales events reaching 500,000 orders per day. The business needs real-time insights to:

- Monitor key business metrics (GMV, conversion rates, inventory levels)
- Detect fraud patterns and anomalies
- Personalize user experiences based on behavior
- Generate daily/weekly executive reports

## Current State

- **Order data**: MySQL database (primary transactional system)
- **User behavior**: Web analytics events via JavaScript SDK (~1M events/day)
- **Inventory**: Third-party API with rate limits (100 requests/minute)
- **Team size**: 3 data engineers, 2 analysts, 1 ML engineer

## Requirements

**Functional:**

- Ingest data from multiple sources in real-time
- Process and transform data with <5 minute latency for real-time metrics
- Support both streaming and batch analytics
- Handle schema evolution gracefully

**Non-functional:**

- Scale to 10x current volume over next 2 years
- Data retention: 7 years for compliance
- Cost-conscious solution (startup budget)

## Constraints

- Must use cloud services (AWS, GCP, or Azure)
- Cannot modify existing MySQL schema
- Team has experience with Python, SQL, and basic Docker
- **Time to deliver**: Solution must be implemented within 3 months

## Deliverable

Write a 1-2 page system design document using the [RFC template by Juan Pablo Buriticá](https://github.com/buritica/mgt/blob/master/templates/rfc_template.md) as a starting point. You don't need to follow the exact same structure as the template, but use it as guidance. What matters is delivering your ideas in a concise document. Focus on:

- High-level architecture
- Technology choices and rationale
- Data flow and processing strategy
- Scalability and reliability considerations
- Implementation phases/timeline
