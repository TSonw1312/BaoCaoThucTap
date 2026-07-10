---
title: "Event 2"
date: 2026-06-27
weight: 2
chapter: false
pre: "  4.2.  "
---

# Summary Report: “Practical applications of Artificial Intelligence (AI) in cloud infrastructure”  

### Event Objectives  

- Share best practices in modern application design.
- Introduce Domain-Driven Design (DDD) and event-driven architecture.
- Provide guidance on selecting the right compute services.
- Present AI tools to support the development lifecycle.

### Speakers  

- **Jignesh Shah** – Director, Open Source Databases.
- **Erica Liu** – Sr. GTM Specialist, AppMod.
- **Fabrianne Effendi** – Assc. Specialist SA, Serverless Amazon Web Services.

### Key Highlights  

#### Identifying the drawbacks of legacy application architecture  

- Long product release cycles → Lost revenue/missed opportunities.
- Inefficient operations → Reduced productivity, higher costs.
- Non-compliance with security regulations → Security breaches, loss of reputation.

#### Transitioning to modern application architecture – Microservices  

- Migrating to a modular system — each function is an independent service communicating via events, built on three core pillars:  
  - Queue Management: Handle asynchronous tasks.
  - Caching Strategy: Optimize performance.
  - Message Handling: Flexible inter-service communication.

#### Domain-Driven Design (DDD)  

- Four-step method: Identify domain events → arrange timeline → identify actors → define bounded contexts.
- Bookstore case study: Demonstrates real-world DDD application.
- Context mapping: 7 patterns for integrating bounded contexts.

#### Event-Driven Architecture  

- 3 integration patterns: Publish/Subscribe, Point-to-point, Streaming.
- Benefits: Loose coupling, scalability, resilience.
- Sync vs async comparison: Understanding the trade-offs.

#### Compute Evolution  

- Shared Responsibility Model: EC2 → ECS → Fargate → Lambda.
- Serverless benefits: No server management, auto-scaling, pay-for-value.
- Functions vs Containers: Criteria for appropriate choice.

#### Amazon Q Developer  

- SDLC automation: From planning to maintenance.
- Code transformation: Java upgrade, .NET modernization.
- AWS Transform agents: VMware, Mainframe, .NET migration.

### Key Takeaways  

#### Design Mindset  

- Business-first approach: Always start from the business domain, not the technology.
- Ubiquitous language: Importance of a shared vocabulary between business and tech teams.
- Bounded contexts: Identifying and managing complexity in large systems.

#### Technical Architecture  

- Event storming technique: Practical method for modeling business processes.
- Use event-driven communication instead of synchronous calls.
- Integration patterns: When to use sync, async, pub/sub, streaming.
- Compute spectrum: Criteria for choosing between VM, containers, and serverless.

#### Modernization Strategy  

- Phased approach: No rushing — follow a clear roadmap.
- 7Rs framework: Multiple modernization paths depending on the application.
- ROI measurement: Cost reduction + business agility.

#### Applying to Work  

- Apply DDD to current projects: Event storming sessions with business teams.
- Refactor microservices: Use bounded contexts to define service boundaries.
- Implement event-driven patterns: Replace some sync calls with async messaging.
- Adopt serverless: Pilot AWS Lambda for suitable use cases.
- Try Amazon Q Developer: Integrate into the dev workflow to boost productivity.

### Event Experience  

Attending the “GenAI-powered App-DB Modernization” workshop was highly valuable for a new member like me, offering a clear roadmap of system design and modern tools. Key experiences included:  

#### Learning from highly skilled speakers

- Experts shared valuable best practices, but as someone new to the industry, some advanced concepts like DDD context mapping patterns were initially quite overwhelming for me.
- Real-world case studies helped me realize that building a system must start from business logic (Business-first) and a shared vocabulary (Ubiquitous language), rather than just jumping straight into coding.

#### Hands-on technical exposure

- The event storming technique was very intuitive, making it much easier for a newbie to visualize how complex business processes are modeled into domain events.
- I gained a better understanding of system trade-offs (Sync vs Async, Functions vs Containers), learning that in production, we must choose solutions based on actual efficiency and ROI, not just technology trends.

#### Leveraging modern tools

- I was deeply impressed by Amazon Q Developer, especially its code transformation capabilities. As a new member, the prospect of maintaining legacy systems is daunting, so having an AI tool to assist with modernization gives me much more confidence.

#### Networking and discussions

- The event provided a great opportunity to see how tech teams and business units collaborate, helping me shape a professional mindset right from the start of my career.

#### Lessons learned

- Modernization requires a careful, phased approach with clear ROI measurement instead of rushing the process.
- AI assistants and modern architectures significantly reduce coupling while boosting personal and team productivity.

#### Some event photos

<p align="center">
    <img src="1783684021428_2088812899270591419_2174945698042172265_02d3268fd57a8925c2221899ff70d09d.jpg" width="700">
</p>

<p align="center">
    <img src="1783684021503_2088812899270591419_2174945698042172265_02f85b797bf7aa24e4779e4f6073230.jpg" width="700">
</p>

<p align="center">
    <img src="1783684021573_2088812899270591419_2174945698042172265_ac9fba72ece06904661cf4fb68566bbb.jpg" width="700">
</p>

> Overall, despite the steep learning curve with high-level architecture, the workshop provided me with a solid technical map, clarifying what I need to learn and how to approach system modernization properly.