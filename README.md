# Web Security

## XSS

- avoid using `document.write()`, `insertAdjacentHTML()`, `innerHTML`, `outerHTML`

### Risks

- accounts getting stolen
- stealing data
- redirecting to fraudulent sites

### Solutions

- control every form input with validation and sanitize
- allow content only from the **origin** `Content-Security-Policy: default-src 'self';`

## CSRF

### Risks

- taking control of someone else's account
- modifications to sensitive data
- deleting or stealing account

### Solutions

- use **csrf** tokens to validate requests
- checking referer header

## SSRF

### Risks

- accessing internal ressources
- using the server to attack other systems

### Solutions

- list the trusted domains
- disable internal dns resolution
- form input validation

## SQLi

### Risks

- inserting or modifying data in the database
- bypassing permissions
- executing commands on the server

### Solutions

- sanitize inputs
- limit database privileges
- limit permission

## LFI / RFI

### Risks

- accessing the server
- code execution
- data theft

### Solutions

- disable remote file execution `allow_url_include = Off` (**php**)
- restrict access with permissions
- validate and sanitize file paths received as input

## XXE

### Risks

- accessing sensitive files
- **ssrf** exploitation
- bypassing security restrictions

### Solutions

- disable external entity processing in **xml** parsers
- use secure **xml** parsers that block external access
- sanitize **xml** inputs

## Global protection

- `HTTPS` using **TLS**
- setting up **Constent Security Policy** (**CSP**) to restrict loaded scripts
