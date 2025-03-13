# Web Security

## XSS

- avoid using `document.write()`, `insertAdjacentHTML()`, `innerHTML`, `outerHTML`

### Risks

- accounts getting stolen
- stealing data
- redirecting to fraudulent sites

### Solutions

- control every form input with validation and sanitize
- `Content-Security-Policy: default-src 'self';`
