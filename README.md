# Equity Desk Workflow

A working demo of a gated equity-team workflow: from new information to an approved decision and a limit order, with every step on the record.

**Live demo:** open `index.html` in any browser, or visit the GitHub Pages site for this repository.

## The four stages

1. **Data hub**: every source (emails, news, filings, market data) synthesized by company and ranked by materiality, weighted by position size. Includes an earnings calendar with pre- and post-earnings reviews.
2. **Analysis and valuation**: the book, price charts, and an analyst valuation model updated by plain-English instruction through a simulated Claude-in-Excel agent (preview → accept → write → automatic checks → undo).
3. **Approve**: a target price or rating change needs Risk, Compliance and the Portfolio manager before anything moves.
4. **Execute**: approved decisions become limit-order tickets for the trading team, with pre-trade checks. The tool cannot place orders.

## Design principles

- Claude reads, maps and drafts. Excel does the math. People decide.
- Retrieval, not fine-tuning: every claim carries a source.
- Guardrails: approved sources only, writes limited to input cells, every action logged and reversible.

## What is real and what is simulated

Real: holdings and weights from a public Q2 2026 13F filing, prices to the 15 Oct 2026 close and the September CPI print, consensus figures, and paraphrased, attributed headlines. Simulated: the emails, analyst models, house ratings, approvers, policy limits and the trading team. No real emails are sent and no orders are placed.

In the browser version, questions to the model agent are answered with calculations from the model. Live written answers from Claude run in the claude.ai version.

Independent demo by Atul Magoon, built with Claude. Not affiliated with Temasek.
