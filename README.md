# Web Security

## XSS

- avoid using `document.write()`, `insertAdjacentHTML()`, `innerHTML`, `outerHTML`

### Risks

- accounts getting stolen
- stealing data
- redirecting to fraudulent sites

### Solutions

- control every form input with validation and sanitize
- allow content only from the origin `Content-Security-Policy: default-src 'self';`

## CSRF

### Risks

- taking control of someone else's account
- modifications to sensitive data
- deleting or stealing account

### Solutions

- use csrf tokens to validate requests
- checking referer header

## SSRF

### Risks

- accessing internal ressources
- using the server to attack other systems

### Solutions

- list the trusted domains
- disable internal dns resolution
- form input validation
