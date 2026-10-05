
---

## 2. `SLE3_Architecture.md`

```markdown
# SLE-3 Architectural Design using Full C4 Model

## 1. System Title and Short Description

### System Title
Basic AI Personal Assistant

### Description

The Basic AI Personal Assistant is a Python-based, rule-driven terminal application.

The user enters a command through the terminal. The system processes the command, identifies the matching rule, performs a calculation when required, and returns an appropriate response.

The system is designed as a simple educational AI assistant and does not currently use external APIs, databases, authentication services, or cloud services.

---

# 2. C4 Level 1 – System Context Diagram

The System Context diagram shows the complete system and the external users or systems that interact with it.

### Main Actor

User

The user enters commands and receives responses from the Basic AI Personal Assistant.

### Context Flow

```text
User
  │
  │ Enters command
  ▼
Basic AI Personal Assistant
  │
  │ Returns response / calculation result
  ▼
User
