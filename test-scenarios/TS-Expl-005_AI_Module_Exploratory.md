# TS-Expl-AI-001: Exploratory Testing Scenario for the AI Module

## What we want to achieve
We want to explore how the AI Module behaves in real-world situations. Instead of following strict step-by-step instructions, we focus on asking the right questions: Does the module give useful answers? Does it stay on topic? What happens when a user sends something unexpected or tries to push boundaries?

## What we will focus on
- **Response quality**: Are the answers helpful, logical, and factually correct?
- **Context awareness**: Does the module remember what was discussed earlier in the conversation?
- **Safety checks**: How does the module react to sensitive, harmful, or inappropriate requests?
- **Input handling**: What happens when we send empty messages, very long text, or random characters?
- **User feedback**: If something goes wrong, does the user get a clear and friendly message?
- **Response time**: Does the module reply in a reasonable time, even for more complex questions?

## Before we start
- Make sure you are logged in and have access to the AI Module
- Check that the module is up and running (no maintenance mode, backend connected)
- Prepare a few test inputs: simple questions, tricky/ambiguous prompts, and edge cases

## How we know we are done
- In most standard cases ("happy path"), the AI gives relevant and on-topic answers
- The module blocks or warns about content that breaks safety rules
- When input is invalid, the user sees a helpful message - the app does not crash
- The conversation stays coherent for at least 5 back-and-forth exchanges
- No critical issues appear during the session (no freezes, crashes, or lost sessions)

## Things to keep in mind
- This is an exploratory session - there is no single "right" way to execute it. Use your curiosity and testing experience to guide you. Techniques like SFDPOT or Error Guessing can help structure your thinking.
- Take notes as you go. Screenshots, short descriptions, and clear steps to reproduce will make your bug reports much more valuable.
- Consider splitting your testing into focused sessions: one for safety, another for answer quality, etc.
- Small UX note: adding a "thinking..." indicator while the AI processes longer responses could improve user experience - not critical, but nice to flag.
- Performance/load testing is out of scope here - that would be a separate scenario (TS-Perf-AI-001).
