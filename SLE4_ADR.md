# SLE-4 — Architecture Decision Record (ADR)

**Project:** Basic AI Personal Assistant  
**Student:** Aniket Ashok Dhamange  
**PRN:** 25UAM002 | **Division:** A  
**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Status:** Accepted (draft to be verified against code and SLE-2 evidence)

## Title
Separate command input, command matching, calculation, and output responsibilities.

## 1. Context
The project is a Python-based, rule-driven terminal assistant. It accepts a user command, identifies it through predefined rules, performs a basic calculation when needed, and prints a response. The SLE-3 request flow is documented as User → `run_agent()` → input → `get_response(command)` → command matching → handler/calculator → response → print.

## 2. Decision
Keep input, command interpretation, calculation/handling, and output as distinct logical responsibilities instead of combining the whole request-response cycle into one large function.

## 3. Alternatives Considered
1. One large function for input, matching, calculation, and output.
2. Many separate modules for every small operation.
3. A simple, clearly separated request flow suited to the current project (**chosen**).

## 4. Rationale / Justification
- The request flow is easy to trace from input to output.
- Clear responsibilities improve readability and make focused testing easier.
- Calculation handling can be reasoned about separately from ordinary rule-based responses.
- The C4 diagrams can explain how the main parts collaborate without unnecessary complexity.
- This structure is proportionate to a small terminal-based assistant.
- Add actual SLE-2 measurements here: **[insert test case / input size]**, **[insert measured timing or operation count]**, and **[insert comparison result]**.
- Do not claim a performance improvement unless your recorded SLE-2 data supports it.

## 5. Consequences

### Positive
- Clearer code responsibilities and easier explanation during viva.
- Easier to reason about and test the command-response flow.
- Simple architecture without unnecessary infrastructure.

### Negative / Trade-offs
- Requires care to keep function responsibilities clear.
- Rule matching may need redesign if the command set becomes large.
- Profiling evidence is needed to make performance claims.

## 6. References
- SLE-3 repository: https://github.com/aniketdhamange2007-eng/SLE3-C4
- Add the exact path/link to the SLE-2 report after checking where it is stored.
