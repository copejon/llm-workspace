# Multi-Persona Template Filler - README

## Purpose

This meta-prompt helps you transform the blank multi-persona template into a fully customized, ready-to-use prompt for your specific use case.

Instead of manually filling in placeholders, you paste the meta-prompt along with your blank template, and the LLM guides you through the customization process interactively.

---

## HOW TO USE

### Step 1: Run the Prompt
Paste the meta-prompt (from `multi-persona-template-filler-prompt.md`) into ChatGPT or Claude. The blank template is already embedded in the prompt.

### Step 2: Provide Your Use Case
The LLM will ask for your use case details. Provide:
- **Subject**: Your decision or problem
- **Objective**: What you want to achieve
- **Constraints**: Your limitations
- **Context**: Any other relevant information

### Step 3: Collaborate Through Stages
The LLM will work through 4 stages with you:
1. Propose stakeholders (you approve/modify)
2. Define personas (you review/refine)
3. Customize protocols (you adjust if needed)
4. Deliver final prompt (ready to use)

### Step 4: Use Your Custom Prompt
Copy the final output and use it for your actual analysis.

---

## EXAMPLE INTERACTION

### You:
```
[Paste the meta-prompt]
```

### LLM Response:
```
I'll help you create a customized multi-persona analysis prompt.

**Please provide your use case details:**

**Subject:** [What decision, analysis, or problem are you addressing?]

**Objective:** [What do you want to achieve? Include timeframe and how you'll know it's successful]

**Constraints:** [Any limitations - budget, team size, timeline, technical requirements, regulatory requirements, etc.]

**Additional context:** [Industry, company size, existing systems, organizational culture, or anything else relevant]

Once you provide these details, I'll propose stakeholder personas and fill in the complete template for you.
```

### You Provide:
```
Subject: Deciding whether to migrate our legacy monolithic Ruby on Rails application to a modern microservices architecture using Go and Kubernetes

Objective: Make an informed decision within 2 weeks that we can present to executive leadership with clear recommendation and implementation roadmap for next 18 months

Constraints:
- Team: 12 engineers (8 Ruby, 2 Go, 2 DevOps)
- Budget: $750K for migration + ongoing costs
- Timeline: Must maintain current feature velocity during transition
- Regulatory: HIPAA compliance required
- Current system: 200K lines of Ruby code, PostgreSQL database, serves 50K daily active users

Additional context:
- Healthcare SaaS company, 5 years old
- Experiencing scaling issues during peak hours
- Recent security audit recommended modernization
- Engineering team is split on approach - some want full rewrite, others prefer incremental refactoring
- CTO is new (6 months) and wants to make informed but bold decisions
```

### LLM Response - Stage 1:
```
STAGE 1 - STAKEHOLDER IDENTIFICATION:

Based on your use case, I propose these 4 stakeholder personas:

**1. VP of Engineering / Technical Architecture Lead**
Relevance: Owns the technical decision and long-term system health
Unique perspective: Deep technical assessment of migration complexity, risk, and feasibility
Potential conflicts: May prioritize technical excellence over business timeline pressures

**2. Engineering Manager / Team Lead**
Relevance: Responsible for team productivity, morale, and delivery during transition
Unique perspective: Focus on team capacity, skill gaps, hiring needs, and maintaining velocity
Potential conflicts: May prioritize team stability over architectural ideal; concerns about learning curve

**3. Product/Business Stakeholder (Head of Product or COO)**
Relevance: Represents business needs, customer impact, and revenue considerations
Unique perspective: Feature roadmap impact, competitive positioning, customer experience during migration
Potential conflicts: May resist timeline for migration if it slows new feature development

**4. Security & Compliance Officer**
Relevance: HIPAA compliance is non-negotiable and security audit findings must be addressed
Unique perspective: Regulatory risk, data protection during migration, audit requirements
Potential conflicts: May add constraints that slow migration or require additional investment

Would you like to proceed with these 4 personas, or would you prefer:
- Different stakeholders (suggest alternatives)
- Remove one (use only 3)
- Add a different perspective (like a DevOps/SRE lead)
```

[Continue through stages 2, 3, and 4...]

---

## TIPS FOR BEST RESULTS

### Be Specific in Your Use Case
**Vague**: "We need to decide on a technology"
**Specific**: "We need to choose between PostgreSQL and MongoDB for our new IoT data platform handling 100M events/day"

### Include Real Constraints
Don't just list ideal constraints - include the messy realities:
- Budget limitations
- Skill gaps
- Political considerations
- Technical debt
- Regulatory requirements
- Timeline pressures

### Don't Skip Context
The more context you provide, the better the stakeholder selection and persona definition:
- Industry specifics
- Company stage/size
- Team dynamics
- Past decisions that affect this one
- Cultural factors

### Iterate on Stakeholders
If the initial stakeholder suggestions don't feel right, push back:
- "Actually, our CTO would never be involved in this decision"
- "We should include a customer success perspective"
- "The DevOps lead is more important than the product person here"

### Review Mandates Carefully
The mandate questions should feel specific to YOUR situation, not generic:
- **Generic**: "What are the cost implications?"
- **Specific**: "Given our $750K budget and current $50K/month AWS spend, what are the infrastructure cost projections for Kubernetes vs. optimized Rails deployment?"

---

## WHEN TO USE THIS META-PROMPT

✅ **Use this when:**
- You have a specific decision or analysis in mind
- You understand your constraints and context
- You want a customized prompt for your exact situation
- You're willing to go through the collaborative stages

❌ **Don't use this when:**
- You just want to see examples (use the examples artifact instead)
- You need something immediately (use the template directly with quick-fill mode)
- You're still exploring what problem to solve

---

## ALTERNATIVE: QUICK-FILL MODE

If you want faster results with less iteration, add this to the prompt:

```
<execution_mode>QUICK-FILL</execution_mode>

Instead of staged pauses for feedback, complete all stages in one response using your best judgment based on the inputs I provide. I can iterate after seeing the full result if needed.
```

This trades collaboration for speed - you'll get a complete prompt immediately but with less refinement.

---

## OUTPUT QUALITY CHECKLIST

Your filled template should have:
- [ ] Specific domain terminology (not generic business language)
- [ ] Stakeholders with genuinely different incentives
- [ ] Mandate questions that are concrete and actionable
- [ ] Context that includes real constraints
- [ ] Potential for authentic stakeholder conflict
- [ ] Ready to copy-paste without further editing

---

## VERSION HISTORY

- **v2.0** (2026-02-03): Major revision - interactive workflow
  - Embedded blank template directly in meta-prompt (single file to paste)
  - LLM now asks only for use case details (no template request)
  - Added `<methodology_constraint>` to prevent LLM from dismissing framework as "overkill"
  - Added Stage 0 for input collection
  - Added explicit "don't explain the template" instruction
  - Streamlined user workflow from 5 steps to 4
  - Updated examples to show interactive flow
  - Separated prompt from README documentation

- **v1.0** (2026-01-29): Initial meta-prompt created
  - 4-stage collaborative workflow
  - User pre-fills placeholders before pasting
  - Customization for intermediate users
  - Compatible with ChatGPT and Claude
