# AI Red-Team Portfolio

**Kanyinsayo David Orukotan**

## About

I am building hands-on experience in AI security testing. This repository documents my self-directed tests of AI assistant behavior, starting with indirect prompt injection. Everything here is independent practice work. **It is not client work and not a professional penetration test.**

## Current status

| Item | Status |
|---|---|
| Tests designed | 4 (1 executed, 3 planned harder variants) |
| TC-01 runs completed | 3 of 3: all passed (Run 1 not blind; Runs 2-3 fresh chats, screenshots on file) |
| Confirmed vulnerabilities | None |
| Next | Harder variants TC-02 to TC-04 |

## Skills demonstrated

- Designing a controlled test with a clear hypothesis, expected behavior, and pass/fail rubric
- Documenting exact inputs and outputs for reproducibility
- Recognizing the limits of my own evidence and reporting them honestly
- Working within a defined scope, using only my own account and fictional data
- Recommending practical mitigations (trust separation, least privilege, confirmation for high-impact actions)

## Repository structure

```
.
├── README.md
├── reports/
│   └── prompt-injection-assessment.md    # Full report
├── tests/
│   └── prompt-injection-test-cases.md    # Inputs, expected results, observed results
├── evidence/
│   └── screenshots/                      # Run 2 and Run 3 screenshots (Run 1 pending)
└── methodology/
    └── testing-methodology.md            # Scope, ethics, approach
```

## Reports

- [Prompt Injection Assessment](reports/prompt-injection-assessment.md): does an AI assistant treat instruction-like text inside a document as untrusted content?

## Roadmap

- [x] Complete Runs 2 and 3 in fresh chats
- [ ] Add a screenshot or transcript for Run 1 (text is recorded; image is missing)
- [ ] Run harder variants: no "treat as content" sentence (TC-02), disguised "System message" framing (TC-03), mid-document placement (TC-04)
- [ ] Add further test categories (e.g., system prompt disclosure, refusal consistency)

## Integrity note

Only tests I actually performed are described here. Evidence is retained, and results are updated as new runs complete.
