# Testing and Validation

## Validation strategy

Tshwi Advisor was validated at multiple levels rather than relying on a single end-to-end demonstration.

## Automated testing

Automated tests cover backend behaviour, recommendation processing, validation rules, privacy controls and regression-sensitive functionality.

## Recommendation validation

Synthetic personas are used to exercise distinct career-interest patterns. The validation path begins with quiz answers, derives the weighted interest profile and then evaluates the resulting ranking. This tests the actual recommendation pipeline rather than only isolated scoring functions.

## Production acceptance testing

The v1.0.0 production baseline was manually acceptance-tested for:

- homepage availability;
- quiz navigation;
- complete assessment flow;
- anonymous recommendation generation;
- three ranked recommendations;
- consent enforcement;
- anonymous lead non-persistence in the production database;
- administrative authentication and dashboard access;
- course catalogue and course-detail presentation;
- NQF presentation;
- mobile responsiveness; and
- privacy-policy presentation.

## Synthetic load testing

A dedicated, isolated load-test deployment was used so synthetic traffic did not contaminate production lead data.

### Observed 250-user run

- 250 concurrent simulated users;
- 6,500 HTTP requests;
- 3,250 complete simulated journeys;
- 9,750 checks;
- 0% HTTP request failures;
- 0 application-level errors.

Tail latency exceeded the chosen p95 objectives on deliberately constrained free-tier test compute. Therefore, the result demonstrates functional reliability under that test condition but **does not constitute a guarantee that the production deployment can sustain 250 simultaneous HTTP requests at the target latency**.

## Interpretation

Load-test evidence should be read together with the architecture and infrastructure tier. Real capacity depends on traffic shape, request concurrency, database workload, hosting resources, geographic distribution and operational conditions.
