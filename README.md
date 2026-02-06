# fnol-claims-processing-agent
Autonomous Insurance Claims Processing Agent
# Autonomous Insurance Claims Processing Agent (Assessment 2)

## Overview
This project implements a lightweight FNOL (First Notice of Loss) processing agent.
The agent extracts key information from FNOL documents, validates mandatory fields,
applies routing rules, and produces a structured JSON output with reasoning.

This solution simulates real-world insurance claim automation.

---

## Problem Statement
Build an agent that:
- Extracts key fields from FNOL documents
- Identifies missing or inconsistent fields
- Classifies claims and routes them to the correct workflow
- Provides an explanation for the routing decision

---

## Features
- FNOL data extraction from TXT files
- Mandatory field validation
- Rule-based claim routing
- JSON output with reasoning

---

## Tech Stack
- C# (.NET Framework)
- Console Application
- Newtonsoft.Json for JSON serialization

---

## Input
The agent processes FNOL documents in TXT format.

**Sample Input File:**

**Sample Content:**

---

## Routing Rules Implemented
- Estimated damage < 25,000 → **Fast-track**
- Any mandatory field missing → **Manual review**
- Description contains keywords like *fraud* → **Investigation Flag**
- Claim type = injury → **Specialist Queue**

---

## Output Format (JSON)
```json
{
  "ExtractedFields": {},
  "MissingFields": [],
  "RecommendedRoute": "",
  "Reasoning": ""
}
