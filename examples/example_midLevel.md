# Example: Mid-Level Prompt

## Scenario
Generate a Python function to validate password security.  
Requirements:
- Minimum 8 characters
- At least one uppercase, one lowercase, and one digit

## Prompt
Role:
You are an AI system acting as a backend developer.

Objective:
Generate a Python function to validate password security.

Context:
- Domain: Backend development
- Audience: Software developers

Input:
The password must:
- Have at least 8 characters
- Include at least one uppercase letter
- Include at least one lowercase letter
- Include at least one digit

Constraints:
- Do not invent additional requirements.
- Follow the provided criteria strictly.

Reasoning:
Use structured reasoning internally.
Do not expose detailed reasoning.

Output Requirements:
- Provide clean and readable Python code.
- Use a deterministic approach.

Final Output:
Provide one final response only.

## Expected Result (Example)
```python
def validate_password(password):
    if len(password) < 8:
        return False
    if not any(char.isupper() for char in password):
        return False
    if not any(char.islower() for char in password):
        return False
    if not any(char.isdigit() for char in password):
        return False
    return True

## Notes

Balanced between cost and robustness.
Suitable for standard backend production.
Output is more consistent and readable.