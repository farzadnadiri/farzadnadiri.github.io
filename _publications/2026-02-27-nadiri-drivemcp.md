---
title: "DriveMCP: An MCP-Powered Agentic Driver Assistance System"
collection: publications
category: preprints
permalink: /publication/2026-drivemcp-agentic-driver-assistance
excerpt: "Decomposes a monolithic vision-language driving assistant into specialized Model Context Protocol expert servers, coordinated by a stateful orchestration graph and gated by an RSS and TTC safety arbiter."
date: 2026-02-27
venue: "IEEE Transactions on Intelligent Vehicles"
paperurl:
citation: 'Nadiri, F., & Rad, A. B. (2026, under review). "DriveMCP: An MCP-Powered Agentic Driver Assistance System." IEEE Transactions on Intelligent Vehicles.'
---

Grounded in a CARLA camera and LiDAR perception stack (RGB detection, range refinement, Kalman tracking) feeding a typed world state with per-field confidence. Evaluated against VLM-direct, RAG and no-arbiter baselines under injected perception and CAN faults. The telemetry server in this stack is open source: [MCP-CAN](https://github.com/farzadnadiri/MCP-CAN).
