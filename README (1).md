# Personalization Flywheel

**Live demo:** https://vidhi20.github.io/Personalization-Flywheel/

A product concept for a sports and gaming app's Data Products team. Most good personalization ideas never get tested, because experiment slots are scarce and analysis is slow. This concept fixes that with two pieces:

1. **One personalization service for every screen.** The app sends a customer, a page and a moment, and gets back ranked content any screen can show. The demo covers cross-sell, customers with no history yet, and a responsible gaming guardrail that removes promotions.
2. **An experiment flywheel.** Ideas are pre-tested on past traffic, ranked by expected dollars per test slot each week, sized for statistical power (95% confidence, 80% power, 2-week minimum), and scheduled into live test slots. Each test gets a drafted hypothesis, guardrail metrics and a decision rule.

## Product definition
- **Users:** product managers, data scientists and analysts who own personalization ideas
- **Ships first:** an idea queue with sample-size checks and offline pre-tests
- **North star:** validated wins per quarter
- **Guardrails:** responsible gaming triggers, opt-outs, p95 latency, lost engagement in other products

## How it works
- Single HTML file with plain JavaScript, no build step
- Ranking score = customer affinity for each product + fit with the page and moment + popularity + a cross-sell boost
- Sample size uses the two-proportion formula, then weeks to read = users needed per arm divided by half of weekly reach

## Disclaimer
Independent concept by Vidhi Parekh. Not affiliated with or endorsed by FanDuel. All customers, content and numbers are simulated.

Related builds: [GrocerIQ](https://github.com/vidhi20/GrocerIQ) (collaborative filtering, segmentation) and [FinRAG](https://github.com/vidhi20/FinRag) (hybrid ranking with reranking).
