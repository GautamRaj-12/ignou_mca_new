<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [Web Software Engineering](#web-software-engineering)
  - [Introduction](#introduction)
  - [Different Characteristics](#different-characteristics)
    - [Characteristics of a Web Application](#characteristics-of-a-web-application)
    - [Development, Testing, and Deployment](#development-testing-and-deployment)
      - [Development](#development)
      - [Testing](#testing)
      - [Deployment](#deployment)
    - [Usage of Web Applications](#usage-of-web-applications)
    - [Maintaining Web Applications](#maintaining-web-applications)
    - [Designing Web Applications](#designing-web-applications)
  - [Issues of Management of Web Based Projects](#issues-of-management-of-web-based-projects)
    - [Review of Good Software Development Practices](#review-of-good-software-development-practices)
    - [Organisation of Web Application Teams](#organisation-of-web-application-teams)
    - [Development and Maintenance Issues](#development-and-maintenance-issues)
  - [Metrics](#metrics)
  - [Analysis](#analysis)
  - [Design and Construction](#design-and-construction)
  - [Reviews and Testing](#reviews-and-testing)
  - [Check Your Progress 1](#check-your-progress-1)
  - [Check Your Progress 2](#check-your-progress-2)

<!-- TOC end -->

<!-- TOC --><a name="web-software-engineering"></a>
# Web Software Engineering

<!-- TOC --><a name="introduction"></a>
## Introduction

The demand for web software applications has risen dramatically in the Internet age, where services are delivered over networks. These applications must support concurrent access by multiple users. Competitive pressures require rapid development cycles, often deploying new applications within weeks.

<!-- TOC --><a name="different-characteristics"></a>
## Different Characteristics

<!-- TOC --><a name="characteristics-of-a-web-application"></a>
### Characteristics of a Web Application

Web applications are structured in layers, unlike monolithic applications. They typically separate client-side (browser interface) and server-side (business logic and data storage) components. This layered approach allows for flexibility in design, maintenance, and usage:

- **Layered Architecture:** Facilitates independent development and updates of different application layers (presentation, business logic, data).
- **Types of Web Applications:** Include static content, dynamic content updated frequently, interactive sites, portals, e-commerce platforms, and search engines.

<!-- TOC --><a name="development-testing-and-deployment"></a>
### Development, Testing, and Deployment

<!-- TOC --><a name="development"></a>
#### Development
- **Network Considerations:** Web applications must handle communication over networks, which introduces complexities like variable network speeds, reliability issues, and different user environments.
- **Scalability:** Due to potential high user traffic, scalability in terms of hardware and architecture is crucial to accommodate growth without compromising performance.

<!-- TOC --><a name="testing"></a>
#### Testing
- **Challenges:** Testing web applications requires simulating real-world internet conditions, which can be difficult in controlled test environments. Issues include browser and platform compatibility, performance under load, and ensuring reliability across diverse user scenarios.
- **Tools:** Automated testing tools help simulate user interactions and measure response times under various conditions.

<!-- TOC --><a name="deployment"></a>
#### Deployment
- **Public Access:** Unlike traditional applications, web applications are accessible to a large, often global, user base immediately upon deployment. This necessitates robust scalability planning and real-world user testing to ensure reliability and performance under typical usage scenarios.

<!-- TOC --><a name="usage-of-web-applications"></a>
### Usage of Web Applications

- **User Base:** Web applications cater to diverse users with varying technical expertise. They must be intuitive, responsive, and capable of handling interruptions gracefully (e.g., network failures).
- **Internationalization:** Many web applications serve users worldwide, necessitating support for multiple languages and cultural considerations.
- **User Expectations:** Users demand fast response times and intuitive interfaces. Poor usability or performance issues can lead to quick abandonment of the application.

<!-- TOC --><a name="maintaining-web-applications"></a>
### Maintaining Web Applications

- **Content Updates:** Web applications often require frequent updates to content, business rules, and user interfaces to stay relevant and competitive.
- **Usability and Design:** User expectations for visually appealing and easy-to-use interfaces require ongoing maintenance and updates.

<!-- TOC --><a name="designing-web-applications"></a>
### Designing Web Applications

- **Modularity:** Designing web applications involves creating modular components that are reusable and adaptable, facilitating easier maintenance and updates.
- **User Interface:** Interface design is critical, accommodating users with varying abilities and ensuring accessibility across different devices and platforms.
- **Web Services:** Integration with external web services enhances functionality and reusability but introduces challenges in security and reliability.

<!-- TOC --><a name="issues-of-management-of-web-based-projects"></a>
## Issues of Management of Web Based Projects

<!-- TOC --><a name="review-of-good-software-development-practices"></a>
### Review of Good Software Development Practices

- **Managing Requirements:**
  - Clear understanding of customer requirements is crucial.
  - Regular communication to align developer and customer perspectives.

- **Managing the Project:**
  - Proper planning and proactive risk management are essential.
  - Project plan should include background, stakeholder info, estimates, methodology, monitoring, and schedule.
  - Subordinate plans include Configuration Management, Quality Assurance, Quality Control, Risk Management, Training, Metrics, and Defect Prevention.

- **Measurements:**
  - Essential for objective project assessment and control.
  - Often overlooked in software engineering but critical for project management.

- **Risk Management:**
  - Identify and manage project risks proactively.
  - Prioritize significant risks and adapt risk management plans as project evolves.

<!-- TOC --><a name="organisation-of-web-application-teams"></a>
### Organisation of Web Application Teams

- **Webmaster:**
  - Role similar to an administrator, responsible for daily site maintenance and health.
  - **Activities:**
    - Gather user feedback (bugs, suggestions, questions).
    - Ensure proper access control and security (authentication, server maintenance).
    - Obtain usage metrics:
      - Number of hits by IP address.
      - Number of registered visitors.
      - Frequency distribution of pages visited.
      - Bandwidth utilization.
      - Number and type of errors.
    - Ensure change control procedures are followed.
    - Archive old content and keep newer content prominent.

- **Application Support Team:**
  - Involved in maintenance, often by the same organization that developed the site.
  - **Activities:**
    - Remove bugs and cosmetic issues.
    - Update the user interface.
    - Alter business rules.
    - Introduce new features and disable/remove old ones.
  - **Team Members:**
    - Designers (graphic artists).
    - Programmers.
    - Database specialists.
    - Testers.

- **Content Development Team:**
  - Frequent changes needed to retain user interest.
  - **Activities:**
    - Update content (e.g., news sites updating every few minutes).
    - Add articles and papers of interest.
  - **Team Members:**
    - Researchers.
    - Authors.
    - Domain experts.
    - Full-time members or freelance contributors.
  - **Content Formats:**
    - Word processor files with images, graphs, tables.
    - Audio files, slide presentations, video clips.

- **Web Publisher:**
  - Converts content into a web-compatible format (e.g., HTML).
  - Must understand web servers and markup languages.
  - Automated tools for news feeds.

<!-- TOC --><a name="development-and-maintenance-issues"></a>
### Development and Maintenance Issues

- **Configuration Management:**
  - Critical due to frequent changes.
  - **Importance:**
    - Prevents losing control of software.
    - Maintains predictability of changes.
  - **Content Management:**
    - Ensure accurate postings.
    - Prevent incorrect prices or terms.
    - Avoid publishing incomplete content.
  - **Challenges:**
    - Identifying configuration items.
    - Managing short-lived and longer-lasting content.
    - Handling hyperlinks within content.
    - Using tools suitable for constant evolution and network operation.

- **Project Management:**
  - **Challenges:**
    - Hazy and fluid requirement specifications.
    - User-dictated schedules.
    - Coordination of geographically dispersed teams.
    - Ownership and accountability issues.
    - Identifying success metrics.
    - Agile methodologies for analysis, design, and testing.
    - Quality assurance amidst rapid activity.
  - **Strategies:**
    - Recognize iterative life cycle with short iterations.
    - Manage user expectations and negotiate scope.
    - Use groupware and communication tools for distributed teams.
    - Ensure processes are appropriate and simple to follow.

<!-- TOC --><a name="metrics"></a>
## Metrics

- **Measurement in Management**: Essential for understanding progress and standing in endeavors.
- **Software Engineering**: Historically slow to adopt measurement, now increasingly measuring parameters like schedule, effort, defects.
- **Cost Management**: Practices vary; some secretive, others place budget responsibility on project managers.
- **Web Applications Metrics**: Focus on detailed scheduling, effort tracking beyond conventional work hours.
- **Size Measurement**: Preferably done with implementation-independent metrics like function points.
- **Quality Measurement**: Includes defect severity, phase of detection, effort to fix, etc.
- **Other Metrics**: Human resource utilization, code reuse, requirement changes, attrition rate.

<!-- TOC --><a name="analysis"></a>
## Analysis

- **Requirement Analysis**: Critical for clarity; stakeholder involvement crucial to avoid conflicting requirements.
- **User Interaction**: Vital; UI must be simple, visually appealing, accommodating to diverse user backgrounds.
- **Content Management**: Importance of displaying content effectively based on audience characteristics.

<!-- TOC --><a name="design-and-construction"></a>
## Design and Construction

1. **Visual Appeal and Aesthetics:**
   - Domain of a graphic artist.
   - Avoid overuse of sound effects, blinking, and moving images.
   - Prioritize functionality over graphical appeal.

2. **Ease of Data Entry:**
   - Simplify data entry, especially for users unfamiliar with computers.
   - Minimize keyboard entry, use mouse selection from lists.
   - Facilitate easy information requests from the application.

3. **Ease of Obtaining Application Responses:**
   - Ensure results are easy to see and interpret.
   - Provide visual feedback for processing times.
   - Maintain user orientation with context-sensitive help.

4. **Intuitive, Easy Navigation:**
   - Aid navigation with site maps and location indicators.
   - Enable return to the home page with a single click.
   - Provide comprehensive navigation facilities without relying on browser buttons.

5. **Robustness and Error Handling:**
   - Handle erroneous inputs gracefully with discreet error messages.
   - Avoid disconnections or unexplained error pages.

**General Considerations**
   - **Avoid Scrolling:** 
     - Design to prevent scrolling, especially horizontal scrolling, for any screen resolution.
     - Vertical scrolling is preferable if scrolling is necessary.

<!-- TOC --><a name="reviews-and-testing"></a>
## Reviews and Testing

- **Content and Design Review**: Ensures accuracy, usability, and navigability.
- **Testing**: Unit testing at page level; integration testing for overall functionality.
- **Compatibility Testing**: Ensuring compatibility with various browsers, screen resolutions, network speeds.

<!-- TOC --><a name="check-your-progress-1"></a>
## Check Your Progress 1
1. The can bring about much greater flexibility and
simplicity in design, maintenance and usage of web applications.
2. One of the significant characteristics of a Web Application is to have a large
number of users

<!-- TOC --><a name="check-your-progress-2"></a>
## Check Your Progress 2

1. The essence of managing the project is proper _________ and executing according to the plan.
2. The ___________ process must be up to the demands placed on it of keeping control over the software configuration in spite of the many changes that will happen.