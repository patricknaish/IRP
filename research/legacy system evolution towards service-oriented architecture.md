# Abstract

- Service-Oriented Architecture (SOA) has become popular in recent years
- The majority of legacy systems are still not SOA enabled
- Considerable increase in the complexity of the legacy systems that store this information
- Important to preserve the investment of many years of tuning and debugging of the legacy assets
- Several techniques exist for modernizing legacy systems towards service-oriented architecture.
- Survey of the various approaches to moving legacy systems to the SOA environment


# Introduction

- SOA is architectural construct for flexible connection of separate components in response to changes in business
- Focuses on the exchange of information among major software components
- Focuses on resuability of components
- Separates interface from implementation
- Appealing features
    + Loose coupling
    + Abstraction of logic
    + Agility
    + Flexibility
    + Reusability
    + Autonomy
    + Statelessness
    + Discoverability
    + Reduced costs
- Improves business comunication
- Short-term benefits
    + Improved reliability
    + Reduced hardware costs
    + Leverages existing development skills
    + Moves to standards-based server/applications
    + Provides data bridge between incompatible technoloogies
- Long-term benefits
    + Reduced management costs
    + Collection of unified information taxonomy
- Four categories of approaches to legacy systems
    + _Replacement_ rewrites applications or replaces completely
    + _Redevelopment_ reverse engineers SOA functionality into legacy systems
    + _Wrapping_ provides a new interface to existing components
    + _Migration_ moves the legacy system to the SOA environment while preserving data and functionality


# Comparison Criteria

- Modernisation strategy
- Legacy system type
- Degree of complexity
- Analysis depth
- Process adaptability
- Tool support
- Degree of coverage
- Validation maturity


# Replacement of Legacy Systems

- Not advocated by surveyed papers
- May be useful if business rules well understood and legacy system is dificult to maintain
- May be justified due to costs of other techniques
- Rewriting delivers customised solution that is bespoke to organisation
- Off the shelf systems less risky and faster, but possibly more expensive because of need for modification
- Legacy system can be replaced all at once or incrementally
- Main risks
    + Maintenance of new system without familiarity
    + Lack of guarantee of functionality to the same degree
- Least desirable solution for migration to SOA


# Wrapping

- Adds new interface to legacy components
- Black-box modernisation technique
- Useful where:
    + Legacy code too expensive to rewrite
    + Code small
    + Code reusable
    + Fast solution needed
- Quick and simple
- Does not change fundamental characteristics of legacy applications
- Problems with maintenance remain
- Studying internals of legacy system important

## Techniques

- Legacy code wrapped in XML
    + Offers individual functions as web services
    + Components given WSDL interfaces/SOAP packaging
    + Proxy links services into SOA architecture
- Wrapped in an SOA interface
    + Models an FSA for interactions between client and legacy system
    + Mostly done manually (impractical)
- CelLEST method
    + Interactions are reverse engineered
    + Task-specific segments of interaction wrapped in web-accessible front-ends
        * Middleware collects interaction traces
        * System interface reverse-engineered
        * Task-specific navigation paths analysed to get model of user's tasks of interest
    + Code independence
    + Complex when large number of interactions possible
- Interface wrapping legacy system for web browser
    + Seven-step process
        * Function Mining
        * Function Wrapping
        * XML Schema Creation
        * Server Stub Generation
        * Client Class Generation
        * Server Linking
        * Web Service Binding
    + SoftWrap


# Redevelopment

- Reengineering
- Analysis and adjustment of application to represent in new form
- Various activities
    + Reverse engineering
    + Restructuring
    + Redesigning
    + Reimplementing software
- Three main issues
    + Service identification
    + Service packaging
    + Service deployment
- Identification not easy
- Reengineering particularly useful for legacy systems where
    + Needs to be migrated to distributed environment and can be wrapped/exposed as web service
    + Has embedded reusable and reliable functionality
    + Some components more maintainable than system as a whole
    + Embedded functionality needs to run on multiple platforms
    + Some components can be replaced gradually

## Techniques

- SoSR methodology
    + Architecture-centric
    + Service-oriented
    + Role-specific
    + Model-driven
    + Three service-participants model
    + 4+1 view model
    + RACI charts
- Ubiquitous Web Applications Design Framework (UWA)
    + Transaction Design Model (UWAT+)
    + Requirements elicitation
    + Reverse engineering
    + Forward engineering
- Feature analysis
    + Identify system features
    + Construct feature model
    + Identify implementation in legacy system
    + Domain decomposition
- White-box approach
    + Legacy architecture recovery
    + Creation of evolution plan
        * Architecture selection
        * Definition of evolution cycles
        * Planning of cycles
        * Preliminary feasibility check
    + Plan execution


# Migration

- Legacy code identified/decoupled/extracted
- UIs reengineered to be compatible with an SOA structure
- Incorporates both redevelopment and wrapping
- Aims to product system with improved SOA-compatible design
- Not always obvious how to distinguish
- Moves entire legacy system/core framework to new environment

## Techniques
- Service-Oriented Migration and Reuse Technique (SMART)
    + Considers specific interactions required by target SOA
    + Considers changes that must be made to legacy components
    + Gathers range of information about
        * Legacy components
        * Target SOA
        * Potential services
- Hierarchical clustering algorithm
    + Used to understand legacy code
    + Used to extract for web service construction
    + Extracts independent services from legacy code
    + Supports service identification and packaging
    + Provides functional legacy code as web services
- Mashup migration strategy
    + Addresses behavioural and architectural aspects of process
    + Six steps
        * Model target enterprise business requirements
        * Analyse existing legacy system
        * Map target enterprise model to legacy components
        * Identify services
        * Design concrete mashup server architecture
        * Define service-level agreements
        * Implement and deploy services
        * Integrates legacy system at presentation layer


# References
- J.Chatarji: Introduction to service-oriented architecture (SOA) (2004) 
- Comella-Dorda, S.,Wallnau, K.C., Seacord, R.C., Robert, J.E.: A survey of black- box modernization approaches for information systems. In: ICSM. (2000) 173–183
- Sneed, H.M.: Integrating legacy software into a service oriented architecture. In: CSMR. (2006) 3–14
- Sneed, H.M.: Wrapping legacy software for reuse in a SOA. Technical report (2005) 5. Canfora, G., Fasolino, A.R., Frattolillo, G., Tramontana, P.: Migrating interactive legacy systems to web services. In: CSMR. (2006) 24–36
- Canfora, G., Fasolino, A.R., Frattolillo, G., Tramontana, P.: A wrapping approach for migrating legacy system interactive functionalities to service oriented architectures. J. Systems and Software 81(4) (2008) 463–480
- Stroulia, E., El-Ramly, M., Sorenson, P.G., Penner, R.: Legacy systems migration in CelLEST. In: ICSE Posters. (2000) 790
- Stroulia, E., El-Ramly, M., Sorenson, P.G.: From legacy to web through interaction modeling. In: ICSM. (2002) 320–329
- Sneed, H.M., Sneed, S.H.: Creating web services from legacy host programs. In: WSE. (2003) 59–65
- Chung, S., Young, P.S., Nelson, J.: Service-oriented software reengineering: Bertie3 as web services. In: ICWS. (2005) 837–838
- Chung, S., An, J.B.C., Davalos, S.: Service-oriented software reengineering: SoSR. In: HICSS-40. (2007) 172c
- Distante, D., Tilley, S.R., Canfora, G.: Towards a holistic approach to redesigning legacy applications for the web with uwat. In: CSMR. (2006) 295–299
- Chen, F., Li, S., Chu, W.C.C.: Feature analysis for service-oriented reengineering. In: APSEC. (2005) 201–208
- Cuadrado, F., Garc´ ıa, B., Due˜ nas, J.C., G., H.A.P.: A case study on software evolution towards service-oriented architecture. In: AINA. (2008) 1399–1404
- Aversano, L., Canfora, G., Cimitile, A., Lucia, A.D.: Migrating legacy systems to the web: An experience report. In: CSMR. (2001) 148–157
- O’Brien, L., Smith, D.B., Lewis, G.A.: Supporting migration to services using software architecture reconstruction. In: STEP. (2005) 81–91
- Lewis, G.A., Morris, E.J., Smith, D.B.: Analyzing the reuse potential of migrating legacy components to a service-oriented architecture. In: CSMR. (2006) 15–23
- Lewis, G.A., Morris, E.J., Smith, D.B., O’Brien, L.: Service-oriented migration and reuse technique (smart). In: STEP. (2005) 222–229
- Smith, D.B.: Migration of legacy assets to service-oriented architecture environ- ments. In: ICSE Companion. (2007) 174–175
- Zhang, Z., Yang, H.: Incubating services in legacy systems for architectural mi- gration. In: APSEC. (2004) 196–203
- Zhang, J., Chung, J.Y., Chang, C.K.: Migration to web services oriented architec- ture: a case study. In: SAC. (2004) 1624–1628
- Cetin, S., Altintas, N.I., Oguztuzun, H., Dogru, A.H., Tufekci, O., Suloglu, S.: Legacy migration to service-oriented computing with mashups. In: ICSEA. (2007) 21c
- Marchetto, A., Ricca, F.: From objects to services: toward a stepwise migration approach for java applications. STTT 11(6) (2009) 427–440
