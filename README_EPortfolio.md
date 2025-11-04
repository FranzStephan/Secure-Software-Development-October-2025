# Secure Software Development E-Portfolio

This e-portfolio documents my progress throughout the Secure Software Development module at the University of Essex Online (October 2025 Cohort). It includes reflections, diagrams, practical work, reading notes, and evidence of collaboration and skill development.

---

## Module Focus

This module explores:

• Secure software architecture  
• Identifying and mitigating vulnerabilities  
• OWASP Top 10 risks  
• Secure coding and design principles  
• Practical GitHub portfolio creation

The e-portfolio shows both academic and hands-on learning progress.

---

## Group Assignment Team

Team Name: **WAECHTER**  
Focus: Secure design proposal for a Copyright Management Enclave application  

My role: Contribution to design planning and UML modelling activities during Unit 1.

---

## Tools Used

• Visual Paradigm  
• GitHub  
• Markdown  
• OWASP Top 10 resources  
• ISO/IEC 27000 terminology

---

## Unit 1: Introduction and Secure Software Design

### Overview of Learning Focus

Unit 1 introduced secure software development concepts and how poor design decisions can introduce vulnerabilities early in the lifecycle. We reviewed core security principles, explored UML behaviour modelling, and examined key OWASP Top 10 risks affecting web applications.

Security must be planned from the beginning of a project by clearly defining authentication, authorisation, and data control rules before implementation.

---

### Secure UML Modelling Task (Discussion Activity)

As part of the discussion activity, I created a UML Activity Diagram that demonstrates a **Broken Access Control** vulnerability. In this flawed scenario, a system successfully authenticates the user but fails to enforce authorisation, allowing access to protected information.


<img width="672" height="769" alt="Screenshot from 2025-10-27 09-44-18" src="https://github.com/user-attachments/assets/e21db391-a6a1-4c88-bc2d-bdd74be8e110" />

Fellow Peer Feedback for my diagram :" 	
Franz, thank you for this well-structured analysis of OWASP A01:2021. Your identification of the critical gap between authentication and authorisation is precisely where many real-world breaches occur, and your use of UML Activity Diagrams to model this vulnerability demonstrates strong understanding of secure design principles.

What I appreciate about your flowchart:

Your diagram effectively illustrates the sequence of the vulnerability materialising. The clear visual separation between the authentication decision point and the subsequent missing authorisation check makes the flaw immediately apparent. The inclusion of "Log security event 6" after returning 401 Unauthorized shows good practice in maintaining audit trails (ISO, 2018). Additionally, your use of standardised UML notation with proper swim-lane structure and decision nodes enhances readability and professional rigour (Booch et al., 2005).

Suggested improvements:

While your diagram successfully shows the "False" path from the authorisation check leading to protected data return, I would suggest explicitly labelling the "True" path to clarify what happens when authorisation is correctly enforced. Currently, both paths appear to converge at the end state, which may confuse readers about the secure versus insecure outcomes.

Furthermore, consider adding a security logging step after the failed authorisation check (similar to your authentication logging), as OWASP (2021) emphasises that detecting and responding to access control failures requires comprehensive logging. A note indicating where the authorisation logic should retrieve permission data from role-based access control (RBAC) tables, attribute-based policies, or ownership validation, would strengthen the diagram's practical application (Buelta, 2022).

Finally, you might enhance the "Process request metadata" step by showing what specific metadata elements (user roles, resource identifiers, permissions) are extracted, making the authorisation decision point more traceable during implementation."


In my initial post, I explained the vulnerability and recommended UML models for secure design. I also provided peer responses, suggesting improvements to classmates regarding validation placement and threat prevention.

---

### Reading and Learning Completed

• Buelta (2022) on architecture patterns and modular design  
• Velepucha and Flores (2023) on microservices design challenges  
• ISO/IEC 27000 Section 3 terminology on access control and accountability  
• OWASP Top 10 2021 guidance on major security failure categories  
• Lecturecast content introducing UML for secure design

These sources helped strengthen my understanding of secure system flows and how system boundaries must be enforced at the design stage.

---

### Group Project Work (Team WAECHTER)

I contributed to early planning:

• Brainstorming initial approach to our secure application  
• Listing required security-critical components  
• Task splitting and planning communication  
• Mapping connections to OWASP and ISO requirements  
• Agreement to begin UML modelling in Unit 2

---

### Reflection: What I Learned

This unit taught me that secure systems fail when authentication and authorisation are confused. A user may authenticate successfully but still have no right to certain information.

UML modelling helped reveal exactly where checks must happen. This visual method is useful to identify risks early. I also learned how to use GitHub for publishing academic evidence. It was slightly confusing at first, but I am now comfortable uploading and editing files.

Unit 1 established a strong foundation for secure software engineering and prepared me for continued architectural development in later units.

---

### References

Booch, G., Rumbaugh, J. and Jacobson, I. (2005) *The Unified Modeling Language User Guide*. 2nd edn. Boston: Addison-Wesley.

Buelta, J. (2022) *Python Architecture Patterns: Master API design, event driven structures, and package management in Python*. Birmingham, UK: Packt Publishing.

ISO (2018) *ISO/IEC 27000:2018 Information technology Security techniques Information security management systems Overview and vocabulary*. 5th edn. Geneva: International Organization for Standardization.

OWASP (2021) *OWASP Top 10 2021 The Ten Most Critical Web Application Security Risks*. OWASP Foundation. Available at: https://owasp.org/Top10/ (Accessed: 28 October 2025).

Visual Paradigm (2025) *Visual Paradigm Online*. Available at: https://online.visual-paradigm.com/ (Accessed: 28 October 2025).

---
## Unit 2: UML Modelling to Support Secure System Planning  

### **Overview of Learning Focus**  
Unit 2 built on the secure design concepts from Unit 1 by showing how security activities can be embedded throughout the agile Software Development Life Cycle (SDLC). The focus was on maintaining agility while ensuring traceable and continuous security integration. The required reading by Sharma and Bawa (2020) presented a structured approach to embedding lightweight but effective security tasks into agile workflows.  

### **Key Learning and Activities**  
The Sharma and Bawa (2020) study explained how security gaps arise from fast releases and limited documentation. To close these gaps, the authors proposed selecting high-benefit, low-cost security activities from four well-known security engineering processes (CLASP, Microsoft SDL, Common Criteria, Cigital Touchpoints). These were validated through a systematic literature review, a practitioner survey of 97 participants, and statistical ranking tests.  

The resulting framework maps suitable security actions to each SDLC phase:  
- **Pre-requirement:** initial security education for the team  
- **Requirements:** role matrix, definition agreement, trust boundaries  
- **Design:** secure design principles, assumption documentation, risk analysis  
- **Implementation:** coding rules, authorised security tools, static code analysis  
- **Testing:** dynamic analysis, vulnerability testing, penetration testing  
- **Release:** operational readiness, code signing, incident response planning  

I also reviewed ISO/IEC 27000 terminology (confidentiality, integrity, availability, threat, vulnerability, risk and control) to ensure that agile activities align with internationally recognised definitions.  

### **Reflection: What I Learned**  
This unit confirmed that secure development can coexist with agile practice if security is distributed across iterations rather than postponed until release. Small, repeatable controls such as static analysis in CI pipelines or role-based access checks maintain speed without sacrificing protection.  

Although I did not attend the live seminar, my previous UML experience supported independent study. I used UML to visualise where authentication, authorisation and logging occur, helping to communicate security logic clearly to team members. The reading reinforced that UML acts as a shared language between developers and security specialists.  

### **Reading and Learning Completed**  
- Sharma, A. and Bawa, R. K. (2020) *Identification and Integration of Security Activities for Secure Agile Development.* *International Journal of Information Technology,* 14 (1117-1130).  
- ISO/IEC 27000 series on security terminology and assurance  
- OWASP Top 10 (2025) guidance on common software weaknesses  
- Previous UML modelling practice from Unit 1  

These sources strengthened my understanding of how secure planning and UML modelling support risk visibility throughout the agile SDLC.






## Unit 3: Introduction to Programming Languages

### Overview of Learning Focus

Unit 3 introduced the foundations of programming languages and linked them to secure software design. The unit explored how historical milestones, language paradigms and core concepts such as inheritance, polymorphism and abstraction influence the way modern systems are built and secured.

The focus was on three areas:

- Understanding how programming languages evolved from early machine code and assembly to higher level languages.
- Relating language concepts and paradigms to practical examples in Python.
- Connecting language design, architectural patterns and testing strategies to common security issues.

This unit also prepared the ground for the development team project by introducing design patterns and architectural styles that support secure and maintainable systems.

### Key Learning and Activities

**History and paradigms of programming languages**

- Reviewed early developments, including the work of Alan Turing and Alonzo Church on formal models of computation.
- Traced the evolution from the Small Scale Experimental Machine and EDSAC to business systems such as LEO, then to higher level languages such as Cobol, Fortran, Lisp and ALGOL.
- Outlined how these developments led to modern paradigms, for example imperative, functional and object oriented approaches, and how these paradigms influence language behaviour and typical usage.

![Evolution of Programming Languages](ca7e3629-6569-4c8b-ab19-5c1e8428fef0.png)

This diagram summarises how early languages influenced later ones and how major paradigms emerged over time, shaping the foundation for today’s software ecosystems.

**Understanding the building blocks of programming languages**

Before diving into paradigms and architectures, the unit revisited how computers represent characters and symbols. The ASCII and Unicode standards define how text and control characters are encoded as numerical values, ensuring that languages and systems exchange information consistently.

![ASCII and Unicode Table](e5714264-01f2-46bb-a446-068378b86cd8.png)

Recognising how encoding evolved from ASCII to Unicode clarified why programming languages need strict definitions for character sets, escape sequences and data representation. It also connected to software security, since encoding errors often cause vulnerabilities like injection or buffer overflow exploits.

**Core language concepts with Python**

- Revisited key object oriented concepts including encapsulation, inheritance, polymorphism and abstraction.
- Used Python examples to show how these concepts improve modularity, reusability and clarity of security relevant logic.
- Discussed how poor use of these concepts can create tightly coupled code that is difficult to test or harden.

**Architectural patterns and web server structures**

Drawing on the core text, the unit introduced architectural patterns that appear in secure Python systems:

- **The Twelve Factor App methodology**, highlighting configuration management, environment separation and logging as practical security controls.
- **Web server structures** based on a request response model, including LAMP style architectures.
- Examined a concrete stack using nginx as a reverse proxy, uWSGI as an application gateway and Django plus Django REST Framework as Python workers that implement business and security logic.
- Considered how static content should be served efficiently, including the use of external storage and content delivery networks to improve performance and resilience.
- Discussed how careful configuration of proxies and headers supports monitoring, error handling and secure deployment.

**Event driven and asynchronous structures**

The unit then extended the architectural focus to event driven systems:

- Introduced basic event driven structures and the fire and forget model where tasks are queued and processed asynchronously.
- Described how message buses and queues such as RabbitMQ, Redis or Kafka decouple publishers from subscribers.
- Used Celery and Celery Flower as examples of Python tooling for asynchronous and scheduled tasks, workload distribution and monitoring.
- Explored advanced event driven structures, including streaming events, pipelines and feedback loops that can drive scaling decisions or quota enforcement.
- Emphasised the implications of these designs for observability, error handling and security boundaries.

**Programming challenges, security issues and testing**

- Reviewed common language related vulnerabilities, for example unsafe memory handling and buffer overflows, and contrasted them with higher level risks in Python based systems.
- Completed an activity on buffer overflow concepts to reinforce the link between low level implementation details and security failures.
- Introduced design patterns as reusable solutions to recurring design problems and discussed when applying a pattern improves security, testability and maintainability.
- Summarised key testing strategies and when to apply them in the context of language features and architectural choices.

**Team activity and assessment work**

- Contributed to the development team project by working on the Unit 3 design document, applying architectural patterns and language concepts to a realistic system scenario.
- Completed a peer review of another team member’s design document, using the rubric to evaluate clarity, architectural reasoning and attention to security and testing.

### Reflection: What I Learned

This unit helped me connect abstract programming language theory with practical secure system design.

The historical overview clarified that modern languages and frameworks are not isolated technologies, but the result of decades of experimentation with different models of computation and abstraction. Understanding where paradigms such as object orientation and functional programming came from makes it easier to judge when a particular style is suitable for a problem and where its limitations lie.

The architectural material extended my previous knowledge of Python from simple scripts to full stack web applications. Seeing how nginx, uWSGI and Django fit together in a layered web architecture made the responsibilities of each component more concrete. It also highlighted where security controls should be placed, for example rate limiting and TLS termination at the reverse proxy, input validation and authentication in the application layer, and strict separation of static content.

The event driven sections were particularly valuable from a security and reliability perspective. They showed how asynchronous tasks and message queues can keep web interfaces responsive, but also how they introduce new risks such as message loss, inconsistent state or unmonitored background failures. The examples with Celery reinforced the need for strong observability, idempotent task design and clear ownership of shared data.

The buffer overflow activity reminded me that many critical vulnerabilities arise from language level assumptions. Even though Python abstracts away memory management, integration with native libraries or poorly validated input can still expose low level weaknesses. This underlined the importance of choosing appropriate languages and patterns for security critical components.

Working on the design document and peer review turned these ideas into practice. Writing my part of the design forced me to justify specific architectural decisions, for example whether an event driven approach or a traditional request response model was more appropriate for a feature. The peer review exercise improved my ability to critique design choices constructively, including questioning whether patterns and testing strategies were selected with security in mind or just copied by habit.

Overall, Unit 3 strengthened my understanding of how programming languages, architectural patterns and testing strategies interact. It confirmed that secure software development depends not only on coding standards, but also on the deeper design decisions that shape how code is structured, executed and tested.

### Reading and Learning Completed

**Core text**

- Buelta, J. (2022) *Python Architecture Patterns: Master API Design, Event Driven Structures, and Package Management in Python*. Birmingham, UK, Packt Publishing Ltd.  
  - Part II, Architectural Patterns section, including chapters on The Twelve Factor App methodology, Web server structures, Event driven structures and Microservices versus monolith.

**Additional articles and resources**

- Unit 3 online materials on programming language history, paradigms and core concepts.
- Unit 3 lecturecast: Programming Languages and Testing.
- Activity material on buffer overflows and language level vulnerabilities.

These readings and activities deepened my understanding of how programming language design, architectural patterns and testing approaches combine to support secure, scalable systems.

