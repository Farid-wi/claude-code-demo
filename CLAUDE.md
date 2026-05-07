# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository is currently empty and ready for initial development.

## Architecture

To be documented as the codebase develops.

## Development Commands

To be documented once build tools and testing frameworks are configured.

## Workflow

1. First, think through the problem. Read the codebase and write a plan in tasks/todo.md.
2. The plan should be a checklist of todo items.
3. Check in with me before starting work—I'll verify the plan.
4. Then, complete the todos one by one, marking them off as you go.
5. At every step, give me a high-level explanation of what you changed.
6. Keep every change simple and minimal. Avoid big rewrites.
7. **SECURITY REVIEW**: Before finalizing, perform a mandatory security check (see Security Guidelines below).
8. At the end, add a review section in todo.md summarizing the changes.

## Security Guidelines

**MANDATORY**: After writing any code, Claude must perform a security review and confirm:

### Security Checklist
1. **No Sensitive Data in Code**
   - No API keys, tokens, passwords, or secrets in frontend code
   - No credentials hardcoded in any files
   - Check that .gitignore excludes all sensitive files (*.env, *.key, *secret*, etc.)

2. **No Common Vulnerabilities**
   - No XSS (Cross-Site Scripting) vulnerabilities
   - No SQL injection risks
   - No command injection risks
   - No path traversal vulnerabilities
   - Validate and sanitize all user inputs

3. **Frontend Security**
   - No sensitive data exposed in HTML/JavaScript
   - Use HTTPS for all external resources
   - Add Content Security Policy (CSP) headers when applicable
   - Use rel="noopener noreferrer" for external links

4. **Dependencies & Third-Party Code**
   - Review all external libraries for known vulnerabilities
   - Keep dependencies up to date
   - Minimize use of third-party scripts

5. **Authentication & Authorization**
   - Never store passwords in plain text
   - Use secure session management
   - Implement proper access controls

6. **File Security**
   - Ensure .gitignore includes: *.env, *.key, *.pem, *secret*, *credential*, token.txt
   - Verify no sensitive files are tracked by git
   - Remove any accidentally committed secrets immediately

### Security Review Process
When asked to review security or when completing any feature:
1. Read all code files that were created or modified
2. Check for sensitive data exposure
3. Verify .gitignore covers all sensitive file patterns
4. Look for OWASP Top 10 vulnerabilities
5. Document findings in tasks/todo.md
6. Fix any issues immediately before deployment

---

*Note: This file should be updated as the codebase grows to include:*
- *Build, test, and lint commands*
- *High-level architecture and design patterns*
- *Important conventions and workflows specific to this project*
