# Domain-Driven Design Modelling Process 


![](./images/ddd_starter_modelling_process_colored.png)


The [Domain-Driven Design Starter Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process) is a process for learning and applying DDD in practice. It covers eight steps from aligning with the business model to coding the domain model. It is flexible and iterative, and suitable for beginners who want to master DDD.

1. **Align:**
    * Gain a deep understanding of the business domain, its complexities, and objectives.
    * Proposed Tools: [Business Model Canvas](https://www.strategyzer.com/library/the-business-model-canvas),[User Story Mapping](https://jpattonassociates.com/story-mapping/).
2. **Discover:**
    * Collaborate with domain experts to explore and uncover key concepts, behaviours, and relationships.
    * Tools: [Domain Storytelling](https://domainstorytelling.org/), [Example Mapping](https://cucumber.io/blog/bdd/example-mapping-introduction/), [EventStorming](https://github.com/SAP/curated-resources-for-domain-driven-design/blob/main/detailedinfo/eventstorming.md), [User Journey Mapping](https://boagworld.com/audio/customer-journey-mapping/), Iteration on [User Story Mapping](https://jpattonassociates.com/story-mapping/).
3. **Decompose:**
    * Divide the system into Bounded Contexts representing specific subdomains.
    * Tools: [Business Capability Modelling](https://www.slideshare.net/trondhr/from-capabilities-to-services-modelling-for-businessit-alignment-v2), [Design Heuristics](https://www.dddheuristics.com/), [EventStorming with sub-domains](https://www.eventstorming.com/), [Independent Service Heuristics](https://github.com/TeamTopologies/Independent-Service-Heuristics), [Visualizing Sociotechnical Architecture with Context Maps](https://speakerdeck.com/mploed/visualizing-sociotechnical-architectures-with-context-maps).
4. **Strategise:**
    * Identify and prioritize core domains within sub-domains, making informed decisions on resource allocation and build vs. buy vs. outsource choices.
    * Tools: [Core Domain Charts](https://github.com/ddd-crew/core-domain-charts), [Purpose Alignment Model](https://www.informit.com/articles/article.aspx?p=1384195&seqNum=2), [Wardley Mapping](https://learnwardleymapping.com/), [revisiting previously made design decisions](https://vladikk.com/2018/01/26/revisiting-the-basics-of-ddd/).
5. **Connect:**
    * Connect sub-domains in a loosely coupled architecture, considering interactions and continually reassessing design through practical use-case application.
    * Tools: [Domain Message Flow](https://github.com/ddd-crew/domain-message-flow-modelling), [BPMN](https://en.wikipedia.org/wiki/Business_Process_Model_and_Notation), [Process Modelling with EventStorming](https://www.eventstorming.com/), [Sequence Diagram](https://en.wikipedia.org/wiki/Sequence_diagram).
6. **Organize:**
    * Organize teams to align with context boundaries, enabling efficient collaboration and maximizing autonomy.
    * Tools: [Dynamic Reteaming](https://leanpub.com/dynamicreteaming), ["Pioneers, Settlers & Town Planners" Pattern](https://wardleypedia.org/mediawiki/index.php/Pioneers_settlers_town_planners), [Team Topologies](https://teamtopologies.com/), [Visualizing Sociotechnical Architecture with Context Maps](https://speakerdeck.com/mploed/visualizing-sociotechnical-architectures-with-context-maps).
7. **Define:**
    * Define roles and responsibilities of each Bounded Context, make explicit design decisions, and consider technical limitations.
    * Tools: [Bounded Context Canvas](https://github.com/ddd-crew/bounded-context-canvas), [C4 System Context Diagram](https://c4model.com/#SystemContextDiagram), [TAM Block Diagram](https://wiki.one.int.sap/wiki/display/Modeling/Using+TAM), applying product standards.
8. **Code:**
    * Implement the domain model aligned with the domain, fostering better understanding, and minimizing misunderstandings.
    * Tools: [Aggregate Design Canvas](https://github.com/ddd-crew/aggregate-design-canvas), [C4 Component Diagrams](https://c4model.com/#ComponentDiagram), [Design-Level EventStorming](https://www.eventstorming.com/), [Event Modelling](https://eventmodeling.org/posts/what-is-event-modeling/), Hexagonal Architecture, [Mob Programming](https://mobprogramming.org/), [Model Exploration Whirlpool](https://www.domainlanguage.com/ddd/whirlpool/), [Onion Architecture](https://jeffreypalermo.com/2008/07/the-onion-architecture-part-1/), [UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language).
