# Abstract

- COBAudit identifies candidates for web services
- COBStrip extracts code required to fulfill the service
- COBWrap wraps the code extracted and converts it to an executable component
- COBLink connects the wrapped component to the web by generating a WSDL interface


# Rationale

- 240 billion lines of COBOL in German legacy systems
- Redevelopment would cost more than annual state budget
- Reengineering would cost nearly 1 trillion €
- Redevelopment would require requirement recovery
    + Architecture recoverable but not requirement content
    + Must be recollected from end-users
- Focus has moved from transformation to integration
- Estimation methods
    + COCOMO
    + Function-Point
    + Data-Point
- Renders it possible to integrate existing programs as steps in new business processes
- Business processes must be revised to satisfy customer demands
- Large financial service providers must move towards SOA
    + Cuts costs by eliminating redundancy
    + Increases quality of service
    + Must be done gradually without interrupting ongoing operations
    + Must be done with existing software


# Migration vs integration

- Migration
    + Moving of a software system from one environment to another
    + Porting to another platform
    + Transforming code from one language to another
    + Transferring data from one database to another
    + Moving everything to a new OS or middleware
        * Programs
        * Data
        * User interfaces
- Integration
    + Use of existing software components in a new environment without physically moving them into that environment
    + Called upon remotely to provide functionality
    + Function results integrated via network
- Case study
    + Integration
    + Existing mainframe transactions being integrated into SOA
    + Moving from MFS masks to WSDL interface


# Goals

- Main goals
    + Measure sizes/complexities/qualities of candidate IMS/COBOL programs to assess extent of work
    + Assess the feasibility of reusing components as web services
    + Determine if it is possible to extract code from existing COBOL-IMS-DC programs for reuse
    + Demonstrate programs can be wrapped to work without IMS-DC TP monitor
    + Test whether the components can be accessed as web services within IBM WebSphere
- COBRedo automatic reengineering tool
- Complexity metrics
    + Chapin's data complexity
    + Elshof's data flow complexity
    + Card's data access complexity
    + Henry's interface complexity
        * Relation of module interactions to number of modules
    + McCabe's control flow complexity
        * Relation between edges and nodes of a graph
    + McClure's decisional complexity
    + Sneed's branching complexity
    + Halstead's language complexity
        * Relation between operands and operators, and references to them
- SoftAudit normalises complexity measurements
- Quality characteristics
    + Modularity
    + Portability
    + Reusability
    + Convertibility
    + Flexibility
    + Testability
    + Conformity
    + Maintainability
- Web services have priorities
    + Modularity
        * High cohesion
        * Low coupling
    + Reusability
        * Code blocks should contain no IO operations
        * No direct branches into other blocks
    + Flexibility
        * Data independence
        * No hard-coded data
- Code stripping
    + Select paths through a program by blending out unused data and statements
    + Generates multiple instances of the same program
    + Each instance is a separate web service
    + Each instance corresponds to a particular business rule
    + COBStrip
        * Data slicing
        * Several passes required for different business rules from same program
        * Requires human interaction (for verification)
- WSDL wrapping
    + COBWrap
        * Replaces IO with calls to wrapper module
        * Moves IO data from Linkage to Working-Storage
        * Fully automated
    + COBLink
        * Generates wrapper modules to link to wrapped program
        * Creates WSDL schema for web service request (from Linkage)
        * Creates corresponding COBOL module for translating request into input parameters of program
        * Creates WSDL schema for web service response (from Linkage)
        * Creates corresponding COBOL module for transferring output parameters of program into WSDL response


# Results

- 
