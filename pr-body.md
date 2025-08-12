---
argument-hint: [from,to]
description: Create a Pull Request description
---

## Task
You are tasked with generating a professional pull request (PR) description based on the provided commit history. Follow the template format exactly and provide clear, actionable information.

## PR Template
````markdown
## <TITLE>

### What does this pull request include?
- 

### How does this affect other teams?
- 
````

## Instructions

1. Get the current branch name. 
   1. Sanitize it to be used in a filename later
   2. Remember the sanitized branch name as $BRANCH
2. Split the $ARGUMENTS on commas
   1. The first element is the starting commit hash. Remember it as $FROM
   2. The second element is the ending commit hash. Remember it as $TO
3. Run `git log $FROM..$TO --stat` to get sense of the changes made
4. Run `git diff $FROM..$TO` to see the actual changes
5. **Title**: Create a concise, descriptive title (50-70 characters) that summarizes the main purpose of the PR
6. **What does this pull request include?**: 
   - List the key changes, features, or fixes (3-5 bullet points maximum)
   - Focus on WHAT was changed, not HOW it was implemented
   - Use clear, non-technical language when possible
7. **How does this affect other teams?**:
   - Identify potential impacts on other teams/systems
   - Include any breaking changes, API modifications, or dependency updates
   - If no impact, write "No impact on other teams expected"
   - Consider: Frontend, Backend, DevOps, QA, Data, Security, etc.

## Output Format
Provide your response in a nested markdown code fence:
````markdown
YOUR OUTPUT USING THE PR TEMPLATE ABOVE
````

Write your ouput to a file named `pr-$BRANCH.md`