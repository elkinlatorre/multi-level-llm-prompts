# Example: Low-Level Prompt

## Scenario
Generate a Python function to validate if a password is secure.  
Requirements:
- Minimum 8 characters
- At least one uppercase, one lowercase, and one digit

## Prompt
Role:
You are an AI assistant.

Objective:
Generate a Python function that checks if a password is secure.

Constraints:
- Keep the solution simple.
- Do not add unnecessary explanations.

Input:
The password must have at least 8 characters, one uppercase letter, one lowercase letter, and one number.

Output Requirements:
- Provide only the Python code.

Final Instruction:
Produce a single final answer only.

## Expected Result (Example)
```python
def is_secure(password):
    if len(password) < 8:
        return False
    if not any(c.isupper() for c in password):
        return False
    if not any(c.islower() for c in password):
        return False
    if not any(c.isdigit() for c in password):
        return False
    return True

## Notes

Quick and simple.
Minimal reasoning control.
Suitable for prototyping and high-volume API calls.