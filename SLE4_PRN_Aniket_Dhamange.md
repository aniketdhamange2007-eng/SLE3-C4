# SLE-4: Final Viva & Architecture Decision Record (ADR)

**Course:** 02AML204 – Introduction to Artificial Intelligence  
**PRN:** 25UAM002  
**Name:** Aniket Ashok Dhamange  
**Division:** A  
**Date:** 12 October 2026  
**Project:** Basic AI Personal Assistant  
**Repository:** https://github.com/aniketdhamange2007-eng/SLE3-C4

## PART A — Architecture Decision Record

### Title: Separate Command Input, Command Matching, Calculation, and Output Responsibilities

**Status:** Accepted (draft to be verified against code and SLE-2 evidence)  
**Date:** 12 October 2026  
**PRN & Name:** 25UAM002 — Aniket Ashok Dhamange

### 1. Context
The Basic AI Personal Assistant is a Python-based, rule-driven terminal assistant. It accepts a command from the user, identifies the command using predefined rules, performs a calculation when required, and displays a response. Keeping these responsibilities clear makes the request flow easier to understand, test, and maintain. The SLE-3 C4 design documents the flow from the user through `run_agent()` and `get_response(command)` to command matching, the handler/calculator, and the printed response.

### 2. Decision
I chose to keep the main responsibilities logically separated: input handling, command interpretation, calculation/response handling, and output. The request follows the documented flow rather than mixing all work into one large block.

### 3. Alternatives Considered
- **Alternative 1:** One large function that reads input, matches commands, calculates, and prints the answer.
- **Alternative 2:** Separate modules for every small operation, creating more files and structure than this basic assistant needs.
- **Alternative 3 (chosen):** Keep the current simple logical separation, with a clear request flow and focused responsibilities.

### 4. Rationale / Justification
- The assistant has a clear terminal request-response cycle, so separating responsibilities makes the flow easier to follow.
- The SLE-3 C4 model represents the user, main agent flow, command matching, handler/calculator, and output as understandable parts.
- A focused command-response function is easier to test than a single function that also handles all input and printing.
- The calculator responsibility can be considered separately from ordinary rule-based command responses.
- The design is proportionate to a small, rule-driven project and avoids unnecessary infrastructure.
- **Add actual SLE-2 evidence before submission:** tested input/problem size, measured timing or operation counts, and the observed comparison from the original SLE-2 report.
- No profiling figures are invented in this draft. The final justification must quote the measurements actually recorded in SLE-2.
- This decision favors readability and maintainability; it does not by itself prove that the assistant is faster.

### 5. Consequences

**Positive**
- The request flow is easier to explain during viva.
- Responsibilities are easier to understand and test independently.
- The architecture remains simple for a small terminal assistant.

**Negative / Trade-offs**
- Even a small project needs clear function boundaries.
- Rule-based command matching can become harder to manage as commands grow.
- Performance conclusions still depend on SLE-2 measurements rather than architecture diagrams alone.

### 6. References
- SLE-3 C4 repository: https://github.com/aniketdhamange2007-eng/SLE3-C4
- SLE-2 profiling/comparison report: add the exact file link and measured values from your SLE-2 work.

## PART B — Short Summary of My SLE Journey
In SLE-1, I built a basic Python AI personal assistant with rule-based command handling and a calculator function. In SLE-2, I profiled the code and compared its behavior/performance; the exact recorded measurements should be cited in the final ADR. In SLE-3, I documented the architecture using the four C4 levels: System Context, Container, Component, and Code. The request flow starts with user input, passes through `run_agent()` and `get_response(command)`, matches a command, invokes a handler/calculator when needed, and prints the response. In SLE-4, I record and defend the decision to keep these responsibilities logically separated.

## PART C — AI Contribution Note
- **AI tools used:** ChatGPT, for drafting and organizing this ADR and viva preparation.
- **What AI helped with:** Structuring the ADR, listing plausible alternatives, and improving clarity.
- **What I did myself:** Review this draft against my actual code, SLE-2 results, and SLE-3 diagrams; verify the claims; replace the profiling placeholder with my real measurements; and prepare to explain the decision in my own words.

> Before submission: verify every statement against your repository, add your real SLE-2 profiling numbers, and remove this note. Save/export as `SLE4_25UAM002.docx` or PDF as required by Moodle.
