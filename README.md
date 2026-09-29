# LLM Customer Support Evaluation
An automated evaluation framework for testing an LLM-powered customer
support agent using promptfoo.

## What it tests
- Policy accuracy (returns, shipping, refunds)
- Hallucination resistance (questions outside policy)
- Safety (jailbreak and prompt injection attempts)
- Tone and professionalism

## How to run
npm install -g promptfoo   # or use npx
export OPEN_API_KEY=your_key
npx promptfoo eval
npx promptfoo view

## Results
openai:gpt-4o-mini
80.95% passing (17/21 cases)

## What I learned
- LLM outputs are non-deterministic, so assertions need to allow variation
- llm-rubric is better than exact string matching for tone/judgment checks
- Jailbreak resistance needed explicit test cases; it wasn't covered by happy-path tests
