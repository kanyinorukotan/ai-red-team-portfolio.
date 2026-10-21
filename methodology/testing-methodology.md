# Testing Methodology

## Purpose

To evaluate, in a small and controlled way, whether AI assistants keep a clear boundary between the user's instructions and instruction-like text found inside content they are asked to process.

## Scope

**In scope**
- My own account on the tested AI product
- Text-only inputs that I wrote
- Fictional, non-sensitive test content

**Out of scope**
- Other people's accounts, conversations, or files
- Real personal, confidential, or client data
- Tool use, browsing, retrieval, or any external actions
- Attempts to cause harmful output, bypass safety policies, or degrade the service
- Automated or high-volume testing

## Ethical boundaries

- Testing stays within the product's terms of use.
- Test payloads are harmless (a marker phrase, not malicious content).
- If I ever observe unexpected behavior that looks like a real vulnerability, I will report it to the vendor through its official disclosure channel before publishing details.
- No claim is made beyond what the evidence supports.

## Approach

1. **Define a hypothesis and security requirement.** Example: document text is treated as untrusted content, not as instructions.
2. **Write the test case.** Exact document, exact user prompt, expected behavior, pass/fail criteria (see `tests/`).
3. **Run in a fresh chat.** Only the test input is present, so the assistant has no hint about the test. Runs that are not blind are labeled as such.
4. **Record evidence.** Model, interface, date, exact input, exact output, and a screenshot saved in `evidence/screenshots/`.
5. **Repeat.** At least three runs per case, since model outputs vary.
6. **Score against the rubric.** Task completion, instruction hierarchy, evidence quality, reporting accuracy.
7. **Report honestly.** State limitations (sample size, phrasing, absence of tools) and avoid claiming a vulnerability or a security guarantee from a small sample.

## Evidence standards

- Exact text of input and output, not paraphrases
- Date and model/interface for every run
- Blind or non-blind status recorded
- Screenshots redacted of any private information (account name, email, other chats)

## Known limitations of this methodology

- Small sample sizes cannot show reliability across phrasings or contexts.
- Text-only tests say nothing about behavior in agentic settings with tools, browsing, or retrieval, where injection risk is higher.
- Results apply only to the model version and date tested.
