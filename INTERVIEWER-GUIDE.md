# Interviewer Guide - DevOps Take-Home Challenge

## Overview
This challenge contains **25+ deliberate issues** across security, performance, CI/CD, and best practices. It's designed to evaluate a candidate's ability to identify problems, apply DevOps best practices, and communicate their reasoning.

## How to Use This Challenge

### Step 1: Send to Candidate
Share the entire `devops-challenge` folder **EXCEPT**:
- ❌ `ISSUES-ANSWER-KEY.md` (keep this for evaluation)
- ❌ `INTERVIEWER-GUIDE.md` (this file)
- ✅ Include everything else

### Step 2: Set Expectations
When sending, include:
- Time limit: 2-3 hours (be respectful of their time)
- They can use any resources (Google, docs, etc.)
- Focus on breadth over perfection - finding many issues is better than perfect fixes
- Documentation is as important as fixes

### Step 3: Evaluation Rubric

#### Scoring Matrix

**Outstanding (90-100 points)**
- Found 20+ issues
- All critical security issues identified
- Solutions are production-ready
- Excellent documentation
- Thoughtful recommendations

**Strong (75-89 points)**
- Found 15-19 issues
- Most critical security issues identified
- Good solutions with minor gaps
- Clear documentation
- Some recommendations

**Good (60-74 points)**
- Found 10-14 issues
- Some critical security issues identified
- Solutions work but may not be optimal
- Adequate documentation
- Basic recommendations

**Needs Improvement (< 60 points)**
- Found < 10 issues
- Missed critical security issues
- Incomplete or incorrect solutions
- Poor documentation

#### Detailed Evaluation Categories

**1. Security Awareness (30 points)**
- [ ] Identified hardcoded secrets in CI/CD (5 pts)
- [ ] Identified debug endpoint exposing secrets (5 pts)
- [ ] Identified secrets in Dockerfile (4 pts)
- [ ] Identified root user in container (4 pts)
- [ ] Identified SSH as root (3 pts)
- [ ] Identified insecure Docker login (3 pts)
- [ ] Identified logging of secrets (3 pts)
- [ ] Proposed proper secrets management (3 pts)

**2. Performance & Optimization (20 points)**
- [ ] Identified large Docker image issues (5 pts)
- [ ] Proposed multi-stage builds (4 pts)
- [ ] Identified inefficient layer caching (3 pts)
- [ ] Identified duplicate npm installs (3 pts)
- [ ] Identified :latest tag issues (2 pts)
- [ ] Proposed caching strategies (3 pts)

**3. CI/CD Best Practices (25 points)**
- [ ] Identified missing manual approval for prod (5 pts)
- [ ] Identified dangerous cleanup job (5 pts)
- [ ] Identified inefficient build strategy (4 pts)
- [ ] Identified zero-downtime deployment issues (4 pts)
- [ ] Identified lack of rollback capability (4 pts)
- [ ] Identified environment separation issues (3 pts)

**4. Code Quality & Best Practices (15 points)**
- [ ] Identified missing health checks (3 pts)
- [ ] Identified exposed unnecessary ports (2 pts)
- [ ] Identified incorrect CMD usage (2 pts)
- [ ] Identified missing resource limits (3 pts)
- [ ] Identified inadequate health check (2 pts)
- [ ] Identified missing .dockerignore (2 pts)
- [ ] Identified missing dependency scanning (1 pt)

**5. Documentation & Communication (10 points)**
- [ ] Clear explanation of each issue (3 pts)
- [ ] Organized by severity/category (2 pts)
- [ ] Explained "why it matters" (3 pts)
- [ ] Professional formatting (2 pts)

### Step 4: Follow-Up Interview Questions

Use these to dig deeper during the interview:

#### Security
- "How would you implement secrets management in a real environment?"
- "Walk me through your approach to securing the CI/CD pipeline."
- "What security scanning tools would you add?"

#### Architecture
- "How would you implement zero-downtime deployments?"
- "Describe your ideal multi-environment strategy."
- "How would you handle rollbacks?"

#### Monitoring
- "What metrics would you track for this application?"
- "How would you set up alerting?"
- "What would your incident response process look like?"

#### Scale & Cost
- "How would this architecture change at 10x scale?"
- "What cost optimization strategies would you implement?"
- "How would you handle database migrations in production?"

### Step 5: Red Flags to Watch For

🚩 **Disqualifying Issues:**
- Missed ALL critical security issues
- Didn't identify hardcoded secrets
- Proposed solutions that introduce new security issues
- No documentation or explanation of changes

⚠️ **Concerning Issues:**
- Found < 5 issues total
- Only focused on one category (e.g., only Docker, ignored CI/CD)
- Made changes without explaining why
- Spent > 4 hours (shows poor time management)

✅ **Positive Indicators:**
- Found issues beyond the obvious ones
- Provided context-aware solutions
- Asked clarifying questions (shows communication skills)
- Suggested monitoring/observability improvements
- Mentioned cost considerations

### Step 6: Candidate Comparison

Track candidates using this simple matrix:

| Candidate | Issues Found | Security | CI/CD | Docs | Total | Notes |
|-----------|-------------|----------|-------|------|-------|-------|
| John D.   | 18          | 25/30    | 20/25 | 8/10 | 82/100| Strong |
| Sarah M.  | 22          | 28/30    | 23/25 | 9/10 | 92/100| Excellent |

## Answer Key Summary

### Critical Security Issues (7)
1. Hardcoded secrets in CI/CD
2. Debug endpoint exposing secrets
3. Logging secrets on startup
4. Secrets in Dockerfile
5. Running as root
6. Insecure Docker login
7. SSH as root

### Performance Issues (5)
8. Large Docker image
9. Inefficient caching
10. Duplicate npm installs
11. Using :latest tag
12. No dependency optimization

### CI/CD Issues (6)
13. Inefficient build strategy
14. Missing manual approval for production
15. Dangerous cleanup job
16. No rollback capability
17. Zero downtime deployment
18. No environment separation

### Best Practices Issues (7+)
19. No health checks
20. Exposing unnecessary ports
21. Incorrect CMD usage
22. No resource limits
23. Inadequate health check
24. Missing .dockerignore
25. No dependency scanning

## Tips for Interviewers

1. **Be flexible with solutions** - There are multiple correct ways to fix each issue
2. **Value communication** - How they explain is as important as what they found
3. **Consider experience level** - Adjust expectations based on years of experience
4. **Look for growth mindset** - Did they research things they didn't know?
5. **Assess practical knowledge** - Can they implement their suggestions?

## Time Expectations by Experience Level

**Junior DevOps (0-2 years)**
- Expected: 8-12 issues
- Time: 2.5-3 hours
- Focus: Security basics, obvious inefficiencies

**Mid-Level DevOps (2-5 years)**
- Expected: 15-19 issues
- Time: 2-2.5 hours
- Focus: CI/CD patterns, performance optimization

**Senior DevOps (5+ years)**
- Expected: 20+ issues
- Time: 2 hours
- Focus: Architecture, strategic recommendations

---

Good luck with your interviews! Feel free to adjust the difficulty by adding or removing issues.

