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