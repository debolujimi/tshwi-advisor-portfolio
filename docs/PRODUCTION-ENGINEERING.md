# Production Engineering

## Delivery lifecycle

Tshwi Advisor progressed through a controlled engineering lifecycle:

1. requirements and career-guidance scope;
2. programme knowledge-base construction;
3. deterministic recommendation implementation;
4. weighted-profile and domain-discrimination refinement;
5. synthetic persona validation;
6. load-test harness development;
7. isolated performance-test deployment;
8. security hardening;
9. privacy/data-minimisation hardening;
10. course-data presentation review;
11. production deployment;
12. desktop and mobile acceptance testing; and
13. formal v1.0.0 production baseline.

## Release discipline

The tested production baseline is versioned as **v1.0.0**. Subsequent production changes should be developed and reviewed separately rather than rewriting the baseline.

A conventional semantic-versioning approach is appropriate:

- **v1.0.x** — backward-compatible fixes;
- **v1.x.0** — backward-compatible functionality;
- **v2.0.0** — breaking redesigns or incompatible public behaviour.

## Operational separation

The production frontend, API and persistent data services are operationally distinct. Synthetic performance testing is also isolated from production persistence to avoid contaminating real operational records.

## CI and source control

Git-based development, pull-request review and automated checks are used to maintain a traceable change history. Production-sensitive configuration remains outside the public portfolio.

## Production baseline

**Version:** v1.0.0  
**Baseline date:** 23 September 2026  
**Acceptance status:** production journey, privacy controls, administration, catalogue and responsive presentation verified.
