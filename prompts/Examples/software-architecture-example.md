# Multi-Persona Analysis Example: Software Architecture Decision

## Use Case
This example demonstrates how to use the multi-persona framework for a real-world software architecture decision.

---

## The Prompt (Ready to Use)

```xml
<multi_persona_analysis>

<context>
Subject: Choosing between microservices vs monolithic architecture for a growing SaaS platform
Objective: Make an informed architectural decision for next 3 years
Constraints: Team of 8 engineers, $500K budget, 6-month timeline, existing PostgreSQL database
</context>

<personas>

<persona id="1">
<role>Lead Software Architect</role>
<focus>System scalability, maintainability, technical debt, deployment complexity</focus>
<mandate>
Analyze this architectural choice considering:
- Long-term system evolution and scaling requirements
- Team's technical capabilities and learning curve
- Infrastructure and operational complexity
- Code maintainability and testing strategies
</mandate>
</persona>

<persona id="2">
<role>Engineering Manager/Team Lead</role>
<focus>Team velocity, hiring, onboarding, developer experience, delivery predictability</focus>
<mandate>
Analyze this architectural choice considering:
- Impact on team productivity and morale
- Hiring and onboarding complexity
- Sprint planning and delivery predictability
- Burnout risk and operational burden
</mandate>
</persona>

<persona id="3">
<role>Product/Business Stakeholder</role>
<focus>Time-to-market, feature velocity, cost efficiency, business risk</focus>
<mandate>
Analyze this architectural choice considering:
- Speed of feature delivery to customers
- Cost implications (infrastructure, personnel)
- Business agility and pivoting capability
- Competitive positioning and market response time
</mandate>
</persona>

</personas>

<interaction_protocol>
1. Each persona presents independent analysis
2. Identify alignment and tensions between perspectives
3. Discuss trade-offs and negotiate priorities
4. Synthesize balanced recommendation
</interaction_protocol>

<output_format>
For each persona:
- **Position Statement**: Core perspective in 2-3 sentences
- **Detailed Analysis**: Key considerations, concerns, and insights
- **Recommendations**: Specific actionable suggestions

Then provide:
- **Cross-Persona Dialogue**: Where perspectives align/conflict
- **Synthesized Recommendation**: Integrated final guidance balancing all viewpoints
</output_format>

<quality_controls>
- Maintain authentic stakeholder tensions
- Avoid premature consensus
- Ground in real-world constraints
- Acknowledge uncertainty explicitly
</quality_controls>

</multi_persona_analysis>
```

---

## How to Use This Example

### Step 1: Customize the Context
Modify the `<context>` section to match your actual situation:
- **Subject**: Your specific architectural decision
- **Objective**: What you're trying to achieve and timeline
- **Constraints**: Budget, team size, technical limitations, deadlines

### Step 2: Adjust or Replace Personas
The three personas provided (Architect, Engineering Manager, Product Stakeholder) work for most software decisions, but you can swap them:

**Alternative Persona Options:**
- DevOps/SRE Engineer (operational concerns)
- Security Engineer (security and compliance)
- CTO/Technical Executive (strategic alignment)
- Customer Success Lead (user impact)
- Data Engineer (data architecture implications)

### Step 3: Paste into Your LLM
Copy the entire prompt and paste it into ChatGPT or Claude. The LLM will respond with analysis from each perspective.

### Step 4: Iterate if Needed
After receiving the initial analysis, you can:
- Ask specific personas to elaborate
- Request deeper exploration of tensions
- Add new constraints or information
- Challenge assumptions

---

## Expected Output Structure

When you run this prompt, you should receive:

### Persona 1: Lead Software Architect
**Position Statement**: [2-3 sentence summary]
**Detailed Analysis**: [Technical considerations]
**Recommendations**: [Specific technical guidance]

### Persona 2: Engineering Manager
**Position Statement**: [2-3 sentence summary]
**Detailed Analysis**: [Team and productivity considerations]
**Recommendations**: [Team-focused guidance]

### Persona 3: Product/Business Stakeholder
**Position Statement**: [2-3 sentence summary]
**Detailed Analysis**: [Business and market considerations]
**Recommendations**: [Business-focused guidance]

### Cross-Persona Dialogue
[Where perspectives align and where they conflict]

### Synthesized Recommendation
[Integrated decision guidance that balances all viewpoints]

---

## Customization Examples

### Example 1: Add Security Focus
Add a fourth persona:
```xml
<persona id="4">
<role>Security Engineer</role>
<focus>Attack surface, compliance, data protection, security operations</focus>
<mandate>
Analyze this architectural choice considering:
- Security boundaries and isolation
- Compliance requirements (GDPR, SOC2, etc.)
- Incident response and containment
- Authentication and authorization complexity
</mandate>
</persona>
```

### Example 2: Modify Constraints
Update the context for a different scenario:
```xml
<context>
Subject: Choosing between microservices vs monolithic architecture for a growing SaaS platform
Objective: Make an informed architectural decision for next 3 years
Constraints: Team of 25 engineers across 3 time zones, $2M budget, 12-month timeline, existing MongoDB cluster, HIPAA compliance required
</context>
```

### Example 3: Different Architecture Decision
Change the subject entirely:
```xml
<context>
Subject: Selecting cloud provider (AWS vs GCP vs Azure) for machine learning platform
Objective: Choose optimal cloud infrastructure for next 5 years
Constraints: Team of 12 ML engineers, $1.5M annual budget, existing Python/PyTorch stack, EU data residency requirements
</context>
```

---

## Tips for Best Results

1. **Be Specific in Context**: The more specific your constraints, the more actionable the recommendations
2. **Choose Genuinely Different Personas**: Ensure your personas have different success metrics
3. **Don't Rush Synthesis**: Let the tensions surface before forcing a decision
4. **Follow Up**: Ask personas to respond to each other's concerns
5. **Real-World Test**: Use actual constraints from your situation, not hypotheticals

---

## Common Variations

### Quick Decision Mode
Add this to interaction_protocol:
```
Time limit: Each persona has 100 words maximum. Synthesis must include a clear GO/NO-GO decision.
```

### Deep Exploration Mode
Add this to interaction_protocol:
```
After initial analysis, each persona must respond to the others' concerns with specific rebuttals or agreements. Minimum 3 rounds of dialogue before synthesis.
```

### Risk-Focused Mode
Add this to each mandate:
```
Explicitly identify the top 3 risks from your perspective and rate their severity (1-10).
```

---

## Real-World Application

This example has been used successfully for:
- Microservices vs monolith decisions
- Cloud provider selection
- Database technology choices
- Frontend framework selection
- CI/CD pipeline architecture
- API design patterns
- Authentication/authorization strategies
- Caching strategy decisions
- Deployment architecture

---

**Ready to use!** Copy the prompt above and start getting multi-perspective analysis on your architecture decisions.
