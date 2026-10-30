# payment-failure-lab

Reproducible experiments that inject failures into a fictitious payment flow
and measure loss, duplicate effects, latency, recovery time, and backlog.

> **Status:** proposal. Work starts after
> [payment-ledger-lab](https://github.com/ralfguth/payment-ledger-lab) reaches
> its first reproducible release. All data is synthetic.

## Planned scope

- Idempotent consumer with verifiable persistence.
- Scenarios: consumer crash after commit, broker down, slow processing,
  invalid message, duplicate, exhausted retries.
- Retry with backoff and jitter. Dead letter queue with an observable reason
  and a safe manual replay.
- One command per experiment, producing a JSON and Markdown report with
  automated assertions.

This lab does not claim exactly-once delivery. It shows the difference between
at-least-once delivery and an idempotent business effect.
