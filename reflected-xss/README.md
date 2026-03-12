# Reflected XSS

## Description
Reflected XSS occurs when user input is reflected in the response without proper encoding.

## Example Payload
<script>alert(1)</script>

## Impact
- Cookie theft
- Phishing attacks

## Prevention
- Output encoding
- Input validation
