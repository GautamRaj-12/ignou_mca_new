# UNIT 4: SOFTWARE QUALITY AND SECURITY


## INTRODUCTION  
Software quality assurance is a series of activities undertaken throughout the software engineering process. It comprises the entire gamut of the software engineering life cycle. The objective of the software quality assurance process is to produce high-quality software that meets customer requirements through a process of applying various procedures and standards. The objective of security engineering is to ensure that the software developed is secure.

## SOFTWARE QUALITY
Quality is defined as conformance to the stated and implied needs of the customer. Quality also refers to the measurable characteristics of a software product that can be compared based on a given set of standards. In the same way, software quality can be defined as conformance to explicitly stated and implicitly stated functional requirements. Here, the explicitly stated functional requirement can be derived from the requirements stated by the customer, which are generally documented in some form. Implicit requirements are requirements that are not stated explicitly but are intended. Implicit functional requirements are standards which a software development company adheres to during the development process. Implicit functional requirements also include the requirements of good maintainability.

### Attributes of Quality
- **Auditability**: The ability of software being tested against conformance to standard.
- **Compatibility**: The ability of two or more systems or components to perform their required functions while sharing the same hardware or software environment.
- **Completeness**: The degree to which all of the software’s required functions and design constraints are present and fully developed in the requirements specification, design document, and code.
- **Consistency**: The degree of uniformity, standardization, and freedom from contradiction among the documents or parts of a system or component.
- **Correctness**: The degree to which a system or component is free from faults in its specification, design, and implementation. The degree to which software, documentation, or other items meet specified requirements.
- **Feasibility**: The degree to which the requirements, design, or plans for a system or component can be implemented under existing constraints.
- **Modularity**: The degree to which a system or computer program is composed of discrete components such that a change to one component has minimal impact on other components.
- **Predictability**: The degree to which the functionality and performance of the software are determinable for a specified set of inputs.
- **Robustness**: The degree to which a system or component can function correctly in the presence of invalid inputs or stressful environmental conditions.
- **Structuredness**: The degree to which the System Design Document (SDD) and code possess a definite pattern in their interdependent parts. This implies that the design has proceeded in an orderly and systematic manner (e.g., top-down, bottom-up). The modules are cohesive and the software has minimized coupling between modules.
- **Testability**: The degree to which a system or component facilitates the establishment of test criteria and the performance of tests to determine whether those criteria have been met.
- **Traceability**: The degree to which a relationship can be established between two or more products of the development process. The degree to which each element in a software development product establishes its reason for existing (e.g., the degree to which each element in a bubble chart references the requirement that it satisfies). For example, the system’s functionality must be traceable to user requirements.
- **Understandability**: The degree to which the meaning of the SRS, SDD, and code are clear and understandable to the reader.
- **Verifiability**: The degree to which the SRS, SDD, and code have been written to facilitate verification and testing.

### Causes of Error in Software
- Misinterpretation of customers’ requirements/communication
- Incomplete/erroneous system specification
- Error in logic
- Not following programming/software standards
- Incomplete testing
- Inaccurate documentation/no documentation
- Deviation from specification
- Error in data modeling and representation.

### Measurement of Software Quality (Quality Metrics)
Software quality is a set of characteristics that can be measured in all phases of software development.

#### Defect Metrics
- Number of design changes required
- Number of errors in the code
- Number of bugs during different stages of testing

#### Reliability Metrics
- Measures the mean time to failure (MTTF), which may be defined as the probability of failure during a particular interval of time. This will be discussed in software reliability.

#### Maintainability Metrics
- **Complexity Metrics**: Used to determine the maintainability of software. The complexity of software can be measured from its control flow.
### Important Parameters for Measurement of Software Quality
- To the extent it satisfies user requirements; they form the foundation to measure software quality.
- Use of specific standards for building the software product. Standards could be the organization’s own standards or standards referred to in a contractual agreement.
- Implicit requirements which are not stated by the user but are essential for quality software.

## Software Quality Assurance
The aim of the Software Quality Assurance process is to develop a high-quality software product. The purpose of Software Quality Assurance is to provide management with appropriate visibility into the process of the software project and of the products being built. Software Quality Assurance involves reviewing and auditing the software products throughout the development lifecycle to verify that they conform to explicit requirements and implicit requirements such as applicable procedures and standards. Compliance with agreed-upon standards and procedures is evaluated through process monitoring, product evaluation, and audits.

### The Process of Software Quality Assurance
1. Defines the requirements for software-controlled system fault/failure detection, isolation, and recovery.
2. Reviews the software development processes and products for software error prevention and/or controlled change to reduced functionality states.
3. Defines the process for measuring and analyzing defects as well as reliability and maintainability factors.

### Roles in Software Quality Assurance
- **Software Engineers**: Ensure that appropriate methods are applied to develop the software, perform testing of the software product, and participate in formal technical reviews.
- **SQA Group**: Assist the software engineer in developing high-quality products. Plan quality assurance activities and report the results of review.


## Formal Technical Review

### What is Software Review?

Software review acts as a filter for the software engineering process. The primary purposes of any review are:

- Discovering errors in analysis, design, coding, testing, and implementation phases.
- Ensuring procedures are applied uniformly and in a manageable manner.

### Types of Reviews

1. **Informal Technical Review**
   - Informal meetings and desk checking.
  
2. **Formal Technical Review (FTR)**
   - A structured software quality assurance activity through approaches such as walkthroughs and inspections.

### What is Formal Technical Review?

A formal technical review is a software quality assurance activity performed by software engineering practitioners to improve software product quality. The product is scrutinized for completeness, correctness, consistency, technical feasibility, efficiency, and adherence to established standards and guidelines by the client organization.

### Structured Walkthrough

A structured walkthrough is a review of the formal deliverables produced by the project team. Participants typically include end-users, client organization management, development organization management, auditors, and project team members. These reviews are formal with a predefined agenda that may include presentations and overheads.

### Inspection

An inspection is more formal than a structured walkthrough, typically involving 3-8 people. The subject of the inspection is usually a document like a requirements specification or a test plan, and the purpose is to find problems and identify what’s missing, not to suggest rectification. The result of the inspection meeting should be a written report.

### Verification

Verification generally involves reviews to evaluate whether correct methodologies have been followed by checking documents, plans, code, requirements, and specifications. This can be done with checklists, walkthroughs, etc.

### Validation

Validation typically involves actual testing and takes place after verifications are completed.

### Objectives of Formal Technical Review

- To uncover errors in logic or implementation.
- To ensure that the software has been represented according to predefined standards.
- To ensure that software under review meets the requirements.
- To make the project more manageable.

### Conducting an FTR

Each Formal Technical Review (FTR) is conducted as a meeting and requires well-coordinated planning and commitments. For the success of FTR, the following are expected:

- The schedule of the meeting and its agenda reach the members well in advance.
- Members review the material and its distribution.
- The reviewer must review the material in advance.

The meeting should consist of two to five people and should be restricted to no more than 2 hours (preferably). The aim of the review is to review the product/work and the performance of the people. When the product is ready, the producer (developer) informs the project leader about the completion of the product and requests for review. The project leader contacts the review leader for the review. The review leader asks the reviewer to perform an independent review of the product/work before the scheduled FTR.

### Result of FTR

- **Meeting Decision:**
  - Accept the product/work without any modification.
  - Accept the product/work with certain changes.
  - Reject the product/work due to errors.

- **Review Summary Report:**
  - What was reviewed?
  - Who reviewed it?
  - Findings of the review.
  - Conclusion.

### Checklist for Review

**Software Concept and Initiation Phase:**

- Involvement of the SQA team in writing and reviewing the project management plan to assure that processes, procedures, and standards identified in the plan are appropriate, clear, specific, and auditable.
- Have design constraints been taken into account?
- Whether best alternatives have been selected?

**Software Requirements Analysis Phase:**

- During the software requirements phase, review assures that software requirements are complete, testable, and properly expressed as functional, performance, and interface requirements. The output of a software requirement analysis phase is Software Requirements Specification (SRS). SRS forms the major input for review.

- **Compatibility:**
  - Does the interface enable compatibility with external interfaces?
  - Are specified models, algorithms, and numerical techniques compatible?

- **Completeness:**
  - Does it include all requirements relating to functionality, performance, system constraints, etc.?
  - Does SRS include all user requirements?
  - Are the time-critical functions defined and identified?
  - Are the requirements consistent with available resources and budget?
  - Does the SRS include requirements for anticipated future changes?

- **Consistency:**
  - Are the requirements consistent with each other? Is the SRS free of contradictions?
  - Does SRS use standard terminology and definitions throughout?
  - Has the impact of the operational environment on the software been specified in the SRS?

- **Correctness:**
  - Does the SRS conform to SRS standards?
  - Does the SRS define the required responses to all expected types of errors and failures?
  - Were the functional requirements analyzed to check if all abnormal situations are covered by system functions?
  - Does SRS reference development standards for preparation?
  - Does the SRS identify external interfaces in terms of input and output mathematical variables?
  - Has the rationale for each requirement been defined?
  - Are the requirements adequate and correctly indicated?
  - Is there justification for the design/implementation constraints?

- **Traceability:**
  - Are the requirements traceable to the top level?
  - Is there traceability from the next higher level of specification?
  - Is SRS traceable forward through successive software development phases like design, coding, and testing?

- **Verifiability and Testability:**
  - Are validation criteria complete?
  - Is there a verification procedure defined for each requirement in the SRS?
  - Are the requirements verifiable?

**Software Design Phase:**

- Reviewers should be able to determine whether or not all design features are consistent with the requirements and the program should meet the requirements. The output of the software design phase is a system design document (SDD) and forms an input for a Formal Technical Review.

- **Completeness:**
  - Whether all the requirements have been addressed in the SDD?
  - Have the software requirements been properly reflected in software architecture?
  - Are algorithms adequate, accurate, and complete?
  - Does the design implement the required program behavior with respect to each program interface?
  - Does the design take into consideration all expected conditions?
  - Does the design specify appropriate behavior in case of an unexpected or improper input and other abnormal conditions?

- **Consistency:**
  - Are standard terminology and definitions used throughout the SDD? Is the style of presentation and the level of detail consistent throughout the document?
  - Does the design configuration ensure the integrity of changes?
  - Is there compatibility of the interfaces?
  - Is the test documentation compatible with the test requirements of the SRS?
  - Are the models, algorithms, and numerical techniques that are specified mathematically compatible?
  - Are input and output formats consistent to the extent possible?
  - Are the designs for similar or related functions consistent?
  - Are the accuracies and units of inputs, database elements, and outputs that are used together in computations or logical decisions compatible?

- **Correctness:**
  - Does the SDD conform to design documentation standards?
  - Does the design perform only that which is specified in the SRS?
  - Whether additional functionality is justified?
  - Is the test documentation current and technically accurate?
  - Is the design logic sound, i.e., will the program do what is intended?
  - Is the design consistent with documented descriptions?
  - Does the design correctly accommodate all inputs, outputs, and database elements?

- **Modifiability:**
  - The modules are organized such that changes in the requirements only require changes to a small number of modules.
  - Functionality is partitioned into programs to maximize internal cohesion of programs and minimize program coupling.
  - Is the design structured so that it comprises relatively small, hierarchically related programs or sets of programs, each performing a particular unique function?
  - Does the design use a logical hierarchical control structure?

- **Traceability:**
  - Is the SDD traceable to requirements in SRS?
  - Does the SDD show mapping and complete coverage of all requirements and design constraints in the SRS?
  - Whether the functions in the SDD which are outside the scope of SRS are defined and identified?

- **Verifiability:**
  - Does the SDD describe each function using well-defined notation so that the SDD can be verified against the SRS?
  - Can the code be verified against the SDD?
  - Are conditions and constraints identified so that test cases can be designed?

### Review of Source Code

The following checklist contains the kinds of questions a reviewer may take up during source code review based on various standards:

- **Completeness:**
  - Is the code complete and precise in implementation?
  - Is the code as per the design documented in the SDD?
  - Are there any unreferenced or undefined variables, constants, or data types?
  - Whether the code follows any coding standard that is referenced?

- **Consistency:**
  - Is the code consistent with the SDD?
  - Are the nomenclature of variables and functions uniform throughout?

- **Correctness:**
  - Does the code conform to specified coding standards?
  - Are all variables properly specified and used?
  - Does the code avoid recursion?
  - Does the code protect against detectable runtime errors?
  - Are all comments accurate and sufficient?
  - Is the code free of unintended infinite loops?

- **Modifiability:**
  - Is the program documentation sufficient to facilitate future changes?
  - Does the code refer to constants symbolically to facilitate change?
  - Is the code written in a language with well-defined syntax and semantics?
  - Are the references or data dictionaries included to show variable and constant access by the program?
  - Does the code avoid relying on defaults provided by the programming language?

- **Traceability:**
  - Is the code traceable to the design document and the requirements specification?
  - Does the code reference documentation or databases to show variable and constant access?

- **Verifiability:**
  - Does the code allow for easy testing and validation?
  - Does the code have sufficient comments and documentation to understand its logic and structure?

### Software Testing and Implementation Phase
  - Whether all deliverable items are tested.
  - Whether test plans are consistent and sufficient to test the functionality of the systems.
  - Whether non-conformance reporting and corrective action has been initiated?.
  - Whether boundary value is being tested.
  - Whether all tests are run according to test plans and procedures and any non conformances are reported and resolved?
  - Are the test reports complete and correct?
  - Has it been certified that testing is complete and software including documentation are ready for delivery?

### Installation phase
  - **Completeness**
    - Are the components necessary for installation of a program in this installation medium ?
    - Whether adequate information for installing the program, including the system requirements for running the program available.
    - Is there more than one operating environment?
    - Are installation procedures for different running environments available?
    - Are the installation procedures clearly understandable?

## Software Reliability

### What is Software Reliability?

Unlike hardware reliability, software reliability is more challenging to measure. In the software engineering environment, software reliability is defined as the probability that software will provide failure-free operation in a fixed environment for a fixed interval of time.

Software reliability is typically measured per unit of time, whereas the probability of failure is generally time-independent. These two measures can be easily related if the frequency of input executions per unit of time is known. Mean-Time-To-Failure (MTTF) is the average interval of time between failures, also referred to as Mean-Time-Before-Failure.

### Challenges in Software Reliability Estimation

The greatest challenge in the field of software reliability estimation is the accuracy of operational profiles. Without accurate profiles, estimates are almost certainly wrong. An operational profile is the probability density function (over the entire input space) representing how inputs are selected during the software's lifetime. Operational profiles are essentially "guesses" about future inputs.

### Definitions of Software Reliability

#### IEEE Definition
The probability that software will not cause the failure of a system for a specified time under specified conditions. This probability is a function of the inputs to and use of the system in the software. The inputs determine whether existing faults, if any, are encountered.

#### General Definition
The ability of a program to perform its required functions accurately and reproducibly under stated conditions for a specified period of time.

### Software Reliability Models

Several models have been developed to determine software defects/failures, describing defect/failure occurrence as a function of time, allowing the definition of reliability. These models are based on certain assumptions:

- Failures are independent of each other, i.e., one failure has no impact on other failures.
- Inputs are random samples.
- Failure intervals are independent, and all software failures are observed.
- Time between failures is exponentially distributed.

The following formula gives the cumulative number of defects observed at a time \( t \):

\[ D(t) = T_d (1 - e^{-bct}) \]

Where:
- \( D(t) \) = Cumulative number of defects observed at time \( t \)
- \( T_d \) = Total number of defects
- \( b \) and \( c \) are constants depending on historical data of similar software

Mean Time to Failure (MTTF) can be found as:

\[ MTTF(t) = \frac{e^{bct}}{cT_d} \]

## Software Quality Standards

Software standards help an organization adopt a uniform approach in designing, developing, and maintaining software. Several standards for software quality and software quality assurance exist. Once an organization decides to establish a software quality assurance process, standards may be followed to establish and operate different software development activities and support activities.

### SEI-CMM and CMMI

The Software Engineering Institute (SEI) developed the Capability Maturity Model (CMM), now called the Capability Maturity Model Integration (CMMI), to help organizations improve software development processes. It is a model of 5 levels of process maturity determining an organization's effectiveness in delivering quality software. Organizations receive CMMI ratings by undergoing assessments by qualified auditors.

- **SEI-CMM Level 1**: Characterized by unorganized chaos, periodic panics, and heroic efforts required by individuals to complete projects successfully. Success depends on individuals and may not be repeatable.
- **SEI-CMM Level 2**: Software project tracking, requirements management, realistic planning, and configuration management processes are in place; successful practices can be repeated.
- **SEI-CMM Level 3**: Standard software development and maintenance processes are integrated throughout an organization; a Software Engineering Process Group oversees software processes, and training programs ensure understanding and compliance.
- **SEI-CMM Level 4**: Metrics track productivity, processes, and products. Project performance is predictable, and quality is consistently high.
- **SEI-CMM Level 5**: Focus on continuous process improvement. The impact of new processes and technologies can be predicted and effectively implemented when required.

### ISO Standards

The International Organization for Standardization (ISO) developed the ISO 9001:2000 standard (replacing the previous set of three standards of 1994) to help organizations establish, operate, maintain, and review a quality management system, assessed by outside auditors. The standard is generic and can be applied to any organization involved in production, manufacturing service, including software services.

ISO certification indicates that the organization follows a well-documented established process. It covers documentation, design, development, production, testing, installation, servicing, and other processes. Table 4.1 lists standards and their corresponding titles.

#### Table 4.1: List of Standards

| Standard | Title |
|----------|-------|
| ISO/IEC 90003 | Software Engineering. Guidelines for the Application of ISO 9001:2000 to Computer Software |
| ISO 9001:2000 | Quality Management Systems - Requirements |
| ISO/IEC 14598-1 | Information Technology - Evaluation of Software Products - General Guide |
| ISO/IEC 9126-1 | Software Engineering - Product Quality - Part 1: Quality Model |
| ISO/IEC 12119 | Information Technology - Software Packages - Quality Requirements and Testing |
| ISO/IEC 12207 | Information Technology - Software Life Cycle Processes |
| ISO/IEC 14102 | Guideline for the Evaluation and Selection of CASE Tools |
| IEC 60880 | Software for Computers in the Safety Systems of Nuclear Power Stations |
| IEEE 730 | Software Quality Assurance Plans |
| IEEE 730.1 | Guide for Software Assurance Planning |
| IEEE 982.1 | Standard Dictionary of Measures to Produce Reliable Software |
| IEEE 1061 | Standard for a Software Quality Metrics Methodology |
| IEEE 1540 | Software Life Cycle Processes - Risk Management |
| IEEE 1028 | Software Review and Audits |
| IEEE 1012 | Software Verification and Validation Plans |

## 4.6 Security Engineering

Security is a crucial aspect of software development. It is essential to analyze software security requirements to ensure the developed software can thwart attacks. Security is vital for social media, mobile applications, IoT applications, and cloud applications.

### Security Requirements Analysis

- Elicit security requirements.
- Develop a security policy.
- Design security measures.
- Perform security checks during the entire software development lifecycle.

### Project Planning for Security

Identifying and analyzing security risks is part of project planning. Steps to create a threat model include:

- Identifying the assets.
- Creating an architecture overview.
- Decomposing an application.
- Identifying the threats.
- Documenting the threats.
- Rating the threats.


### Check Your Progress-1
1. What is auditability?
2. Traceability is the ability to trace design back to what?
3. Software quality is designed into software and can’t be infused after the product is released. Explain.

### Check Your Progress-2
1. The purpose of review is to uncover errors and non conformity during testing
phase. yes or no?
2. The result of a review does not include
  (a) The items that are to be reviewed
  (b) The person who reviews it
  (c) Findings of the review
  (d) Solution to a problem
3. What could become an input for FTR in design phase?

### Check Your Progress-3
1. Success of a project depends on individual effort. At what stage of maturity doesthe
organisation‟s software process can be rated?
1. Why ISO 9001 : 2000 is called generic standard?
2. What is the difference between SEI CMM standards and ISO 9000 : 2000 standards?