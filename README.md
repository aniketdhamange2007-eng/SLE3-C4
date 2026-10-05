# SLE-3: Architectural Design using Full C4 Model

## Basic AI Personal Assistant

**Student:** Aniket Dhamange  
**PRN:** 25UAM002  
**Program:** SY B.Tech CSE (AI & ML)  
**Division:** A  
**Course:** 02AML204 – Introduction to Artificial Intelligence  

---

## Project Overview

This repository contains the SLE-3 architectural design of the **Basic AI Personal Assistant** developed in SLE-1 and analyzed in SLE-2.

The system is a Python-based, rule-driven terminal AI assistant. It accepts commands from the user, identifies the command using predefined rules, performs basic calculations when required, and displays the response.

---

## C4 Model Levels

This project follows all four levels of the C4 Model:

1. **Level 1 – System Context**
2. **Level 2 – Container**
3. **Level 3 – Component**
4. **Level 4 – Code**

---

## Main Request Flow

```text
User
  ↓
run_agent()
  ↓
input(command)
  ↓
get_response(command)
  ↓
Command Matching
  ↓
Handler / Calculator
  ↓
Response
  ↓
print(response)
  ↓
User
