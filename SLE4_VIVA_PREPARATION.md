# SLE-4 Viva Preparation — Basic AI Personal Assistant

Use these as practice prompts. Answer in your own words and refer to your actual code, diagrams, and SLE-2 measurements.

## 1. What is an ADR?
An Architecture Decision Record is a short document that records an important design decision, the alternatives considered, the reason for the choice, and its positive and negative consequences.

## 2. What is your project?
It is a Python-based, rule-driven terminal AI personal assistant. It accepts a command, matches it against predefined rules, performs a calculation when needed, and displays a response.

## 3. What decision are you defending?
I am defending the decision to keep input, command matching, calculation/handling, and output as distinct logical responsibilities. This makes the request flow easier to understand and maintain.

## 4. What alternatives did you consider?
- Putting the entire request-response process into one large function.
- Splitting every small operation into separate modules.
- Keeping a simple request flow with clearly separated responsibilities, which best fits the current project's scope.

## 5. Explain the request flow in one minute.
The user enters a command. The agent's main flow receives the input and passes the command to the response logic. The command is matched against predefined rules. If the command needs calculation, the calculator/handler is used. The resulting response is printed to the user.

## 6. What did SLE-2 profiling show?
Prepare this answer using your actual SLE-2 report. State the tested input or problem size, the metric measured, the recorded values, and what comparison those values support. Do not guess or invent figures.

## 7. How does SLE-3 relate to this decision?
SLE-3 documents the architecture through System Context, Container, Component, and Code views. These views help explain the system boundary and the relationships among the main parts of the request flow.

## 8. What happens if the system grows?
If the number of commands grows significantly, command matching could become harder to maintain. The command handlers could then be organized more explicitly and tested independently. Any redesign should be justified by actual requirements and measurements.

## 9. What did AI contribute?
AI helped draft and organize the ADR and practice questions. I must verify the content against my code and evidence, add the actual profiling values, and be able to explain and defend the decision myself.

## Final preparation checklist
- [ ] Re-open the actual SLE-1 code and confirm the function names and behavior.
- [ ] Locate SLE-2 profiling results and memorize the actual values.
- [ ] Review the SLE-3 Context, Container, Component, and Code diagrams.
- [ ] Replace every placeholder in the submission draft.
- [ ] Practice concise answers without reading.
