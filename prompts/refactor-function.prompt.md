# Function Refactoring Prompt Template

Use this template to request function refactoring with specific improvements.

## Template

```
I need help refactoring the following function to improve [IMPROVEMENT_GOALS]. 

**Current Function:**
```[LANGUAGE]
[CURRENT_FUNCTION_CODE]
```

**Context:**
- Purpose: [FUNCTION_PURPOSE]
- Current issues: [SPECIFIC_ISSUES]
- Performance requirements: [PERFORMANCE_NEEDS]
- Constraints: [ANY_CONSTRAINTS]

**Refactoring Goals:**
- [ ] [GOAL_1]
- [ ] [GOAL_2] 
- [ ] [GOAL_3]

**Requirements:**
- Maintain existing functionality and API compatibility
- Include unit tests for the refactored function
- Add proper error handling
- Follow [CODING_STANDARDS] coding standards
- Optimize for [OPTIMIZATION_TARGET]

Please provide:
1. Refactored function with explanations
2. Unit tests covering edge cases
3. Performance comparison if applicable
4. Migration notes for breaking changes
```

## Example Usage

```
I need help refactoring the following function to improve readability, performance, and error handling.

**Current Function:**
```javascript
function processUserData(users) {
    let result = [];
    for (let i = 0; i < users.length; i++) {
        if (users[i].active == true) {
            let user = users[i];
            user.name = user.firstName + " " + user.lastName;
            user.age = new Date().getFullYear() - new Date(user.birthDate).getFullYear();
            if (user.age >= 18) {
                result.push(user);
            }
        }
    }
    return result;
}
```

**Context:**
- Purpose: Filter and process user data for adult active users
- Current issues: Inefficient loops, poor error handling, age calculation bugs
- Performance requirements: Handle 10,000+ user records efficiently
- Constraints: Must maintain existing function signature

**Refactoring Goals:**
- [ ] Improve performance with modern array methods
- [ ] Add proper error handling for invalid data
- [ ] Fix age calculation edge cases
- [ ] Improve code readability and maintainability

**Requirements:**
- Maintain existing functionality and API compatibility
- Include unit tests for the refactored function
- Add proper error handling
- Follow ES6+ coding standards
- Optimize for readability and performance

Please provide:
1. Refactored function with explanations
2. Unit tests covering edge cases
3. Performance comparison if applicable
4. Migration notes for breaking changes
```

## Common Improvement Goals

- **Performance**: Optimize algorithms, reduce complexity, improve memory usage
- **Readability**: Simplify logic, improve naming, add documentation
- **Maintainability**: Reduce coupling, improve modularity, add error handling
- **Security**: Add input validation, fix vulnerabilities, improve data handling
- **Testing**: Make function more testable, add edge case handling
- **Standards**: Follow coding conventions, improve type safety

## Placeholder Reference

- `[IMPROVEMENT_GOALS]`: Main objectives for refactoring
- `[LANGUAGE]`: Programming language (javascript, python, java, etc.)
- `[CURRENT_FUNCTION_CODE]`: The existing function to be refactored
- `[FUNCTION_PURPOSE]`: Brief description of what the function does
- `[SPECIFIC_ISSUES]`: Known problems or inefficiencies
- `[PERFORMANCE_NEEDS]`: Expected performance requirements
- `[ANY_CONSTRAINTS]`: Limitations or requirements to consider
- `[GOAL_1]`, `[GOAL_2]`, `[GOAL_3]`: Specific refactoring objectives
- `[CODING_STANDARDS]`: Team or project coding standards to follow
- `[OPTIMIZATION_TARGET]`: Focus area for optimization (speed, memory, readability, etc.)

## Tips for Effective Refactoring Requests

1. **Be Specific**: Clearly state what aspects need improvement
2. **Provide Context**: Explain the function's role in the larger system
3. **Set Clear Goals**: List measurable objectives for the refactoring
4. **Include Constraints**: Mention any limitations or requirements
5. **Request Tests**: Always ask for comprehensive test coverage
6. **Consider Performance**: Mention if performance is a concern
7. **Specify Standards**: Reference your team's coding conventions