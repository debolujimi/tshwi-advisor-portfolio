# Privacy and Security

## Privacy-by-design

Tshwi Advisor is designed so that career guidance does not require unnecessary collection of personal contact information.

### Data minimisation

- Prospective students can complete the assessment without supplying a name, email address or phone number.
- Anonymous recommendation requests are not persisted as leads.
- Optional contact information is separated from the recommendation requirement.

### Consent

The public workflow requires explicit consent before optional adult contact details can be submitted for programme or admissions follow-up. Production acceptance testing confirmed that contact details submitted without the required consent are rejected.

### Access

Protected administrative functions require authenticated and authorised access. Student/profile access is subject to ownership or administrative authorisation in the production design.

## Security controls

The production implementation incorporates controls including:

- bounded input validation;
- trusted-origin enforcement for relevant state-changing operations;
- CORS allow-listing;
- API and authentication rate limiting;
- secure password hashing;
- short-lived authentication tokens;
- secure HttpOnly production cookies;
- role-based administrative authorisation; and
- non-disclosure of internal server errors to public clients.

## POPIA positioning

The platform is described as **POPIA-aligned by design**, reflecting data-minimisation, consent and access-control measures. This technical design statement is not a declaration of institutional legal compliance and does not replace formal governance, retention, data-subject-rights or cross-border-processing assessments.

## Public-repository boundary

This repository contains no:

- credentials or API secrets;
- production environment variables;
- real student or lead data;
- production database exports;
- authentication secrets;
- operational logs containing personal information; or
- detailed administrative implementation code.
