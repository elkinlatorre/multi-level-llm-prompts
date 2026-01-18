# Example: High-Level Prompt

## Scenario
Generate a robust, deterministic Python function for password validation.  
Requirements:
- Minimum 8 characters
- At least one uppercase, one lowercase, and one digit
- Fully auditable and maintainable

## Prompt
Metadata:
- Prompt Version: 1.0
- Determinism Level: High

Role Definition:
You are an AI system acting as a senior backend engineer.

Objective:
Primary Objective:
Design a robust and deterministic Python function that validates password security.

Success Criteria:
- The function enforces all stated password rules.
- The implementation is readable and maintainable.
- No additional rules are assumed.

Context:
- Domain: Secure backend systems
- Target Audience: Software engineers
- Operating Environment: API-based LLM usage

Input Specification:
Input Data:
Password validation rules:
- Minimum length: 8
- At least one uppercase letter
- At least one lowercase letter
- At least one digit

Data Constraints:
Allowed Actions:
- Generate Python code
- Apply standard string validation techniques

Forbidden Actions:
- Adding extra password rules
- Providing explanations outside the code

Reasoning Configuration:
- Reasoning Strategy: structured
- Reasoning Visibility: hidden
- Exploration Depth: medium
- Alternative Reasoning Paths: not required

Process Instructions:
1. Validate the requirements.
2. Ensure no assumptions are added.
3. Generate the function.
4. Self-check against success criteria.

Output Requirements:
- Output Format: Python code
- Tone: Technical
- Length: Minimal but complete

Self-Validation:
Confirm that all success criteria are satisfied.

Final Output:
Produce one final refined output only.

## Expected Result (Example)
```python
def validate_password_secure(password):
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

Maximum control and determinism.
Suitable for critical systems and production pipelines.
Highly auditable, minimal chance of variation.