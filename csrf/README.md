# Command Injection

## Description
Command Injection occurs when user input is passed to system commands without proper validation.

## Objective
Execute arbitrary commands on the server.

## Example Payload
; ls

## Impact
- Remote command execution
- Server compromise

## Prevention
- Input validation
- Avoid system command execution
- Use safe APIs
