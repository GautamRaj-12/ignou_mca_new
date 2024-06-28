<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [Software Testing and Debugging](#software-testing-and-debugging)
  - [Software Testing](#software-testing)
    - [Testing](#testing)
    - [Validation and Verification](#validation-and-verification)
    - [Importance of Software Testing](#importance-of-software-testing)
    - [Debugging](#debugging)
    - [Basic Terms in Testing](#basic-terms-in-testing)
    - [Test Cases](#test-cases)
    - [Testing Laws](#testing-laws)
    - [Input Domain](#input-domain)
  - [Black Box and White Box Testing](#black-box-and-white-box-testing)
    - [Black Box Testing](#black-box-testing)
      - [Methods for Black box testing strategies](#methods-for-black-box-testing-strategies)
    - [White Box Testng](#white-box-testng)
      - [White Box Testing Strategies](#white-box-testing-strategies)
  - [Testing Activities](#testing-activities)
  - [Levels of Testing](#levels-of-testing)
    - [Unit Testing](#unit-testing)
    - [Integration Testing](#integration-testing)
    - [System Testing](#system-testing)
    - [Acceptance Testing](#acceptance-testing)
  - [Debugging](#debugging-1)
    - [Characteristics of Bugs](#characteristics-of-bugs)
    - [Life Cycle of a Debugging Task](#life-cycle-of-a-debugging-task)
  - [Debugging Approaches](#debugging-approaches)
  - [Testing Tools](#testing-tools)
  - [Examples of Commercial Software Testing Tools](#examples-of-commercial-software-testing-tools)
    - [Rational Test RealTime Unit Testing](#rational-test-realtime-unit-testing)
    - [AQtest](#aqtest)
    - [csUnit](#csunit)
    - [Sahi](#sahi)

<!-- TOC end -->

<!-- TOC --><a name="software-testing-and-debugging"></a>
# Software Testing and Debugging

<!-- TOC --><a name="software-testing"></a>
## Software Testing

<!-- TOC --><a name="testing"></a>
### Testing
- **Definition**: Executing a program to understand its behavior.
- **Goals**:
  - Identify failures
  - Evaluate response time or throughput
  - Measure mean time to failure
  - Assess speed and accuracy of user tasks
  - Validate system/component behavior under specified conditions

<!-- TOC --><a name="validation-and-verification"></a>
### Validation and Verification
- **Validation**: Ensuring the system meets its requirements.
  - "Are we building the correct system?"
- **Verification**: Ensuring the system is built correctly according to specifications.
  - "Are we building the system correctly?"

<!-- TOC --><a name="importance-of-software-testing"></a>
### Importance of Software Testing
- Ensures software meets non-functional requirements:
  - Correctness
  - Performance
  - Robustness
  - Usability
  - Reliability
  - Installability

<!-- TOC --><a name="debugging"></a>
### Debugging
- **Definition**: The process of locating and fixing errors in a program.
- **Steps**:
  - Determine the nature and location of the error.
  - Fix the error.
  
<!-- TOC --><a name="basic-terms-in-testing"></a>
### Basic Terms in Testing
- **Failure**: Deviation of a program's observed behavior from its specification or intended behavior.
- **Fault**: An incorrect step, process, or data definition in a program. Often referred to as a "bug."
- **Error**: The difference between a computed, observed, or measured value and the correct value.

<!-- TOC --><a name="test-cases"></a>
### Test Cases
- Consist of:
  - A set of test inputs
  - Expected results
  - Execution conditions or environments

<!-- TOC --><a name="testing-laws"></a>
### Testing Laws
- Testing can only show the presence of errors, not their absence.
- Combining different verification and validation methods outperforms using a single method.
- Developers should not test their own code.
- Approximately 80% of errors are found in 20% of the code.
- Partition testing is better than random testing.
- The adequacy of a test suite for coverage criteria can only be defined intuitively.

<!-- TOC --><a name="input-domain"></a>
### Input Domain
- **Sources for Input Domain**:
  - Software requirements specification (black box testing)
  - Design and externally accessible program variables (white box testing)
- **Inputs in White Box Testing**:
  - Parameters
  - User-entered inputs
  - File inputs
  - Constants and precomputed values
- **Example**:
  ```c
  #define PI 3.14159
  double circumference(double radius) {
      return 2 * PI * radius;
  }
  ```

<!-- TOC --><a name="black-box-and-white-box-testing"></a>
## Black Box and White Box Testing

<!-- TOC --><a name="black-box-testing"></a>
### Black Box Testing
- It is also known as ***functional testing***.
- The sole purpose of black box testing is to test the application or software from its functionality point of view.
- In this testing, software is tested to check whether the software is achieving all the specified requirements or not.
- The tester is not conerned about the logic of the program. The internal details of the program are not known to the tester.

**Example**:
- Software for purchasing books online
  - User should be able to log in on the website
  - User should be able to see books catalogue
  - Users should be able to place an order.
  - User should be able to make the payment.
  - User should be able to logout.

<!-- TOC --><a name="methods-for-black-box-testing-strategies"></a>
#### Methods for Black box testing strategies
- **Boundary Value Analysis**
  - BVA is a software testing technique that validates how software will respond to inputs at or around the edge of input boundaries.
  - **Test Case Selection Guidelines for Boundary Value Analysis**
      1. If an input condition specifies a range of values, then construct valid test cases for the ends of the range, and invalid input test cases for input points just beyond the ends of the range.
      2. If an input condition specifies a number of values, construct test cases for the minimum and maximum values; and one beneath and beyond these values.
      3. If an output condition specifies a range of values, then construct valid test cases for the ends of the output range, and invalid input test cases for situations just beyond the ends of the output range.
      4. If an output condition specifies a number of values, construct test cases for the minimum and maximum values; and one beneath and beyond these values.
      5. If the input or output of a program is an ordered set (e.g., a sequential file, linear list, table), focus attention on the first and last elements of the set.
  - **Example**: BVA for Triangle Program
      1. Given sides (A; B; C) for a scalene triangle, the sum of any two sides is greater than the third and so, we have boundary conditions A + B > C, B + C > A and A+ C > B.
      2. Given sides (A; B; C) for an isosceles triangle two sides must be equal and so we have boundary conditions A = B, B = C or A = C.
      3. Continuing in the same way for an equilateral triangle the sides must all be of equal length and we have only one boundary where A = B = C.
      4. For right-angled triangles, we must have A^2+B^2 = C^2
  - **Test Cases for Triangle Classification**

      | Test Case | x   | y   | z   | Expected Output         |
      |-----------|-----|-----|-----|-------------------------|
      | 1         | 100 | 100 | 100 | Equilateral triangle    |
      | 2         | 50  | 3   | 50  | Isosceles triangle      |
      | 3         | 40  | 50  | 40  | Equilateral triangle    |
      | 4         | 3   | 4   | 5   | Right-angled triangle   |
      | 5         | 10  | 10  | 10  | Equilateral triangle    |
      | 6         | 2   | 2   | 5   | Isosceles triangle      |
      | 7         | 100 | 50  | 100 | Scalene triangle        |
      | 8         | 1   | 2   | 3   | Non-triangle            |
      | 9         | 2   | 3   | 4   | Scalene triangle        |
      | 10        | 1   | 3   | 1   | Isosceles triangle      |

- **Equivalence Partitioning**
  - Equivalence Partitioning is a method for selecting test cases based on a partitioning of the input domain into classes of data from which test cases can be derived.
  - An ***Equivalence Class*** is a set of inputs that the program treats identically when the program is tested. In other words, a test input taken from an equivalence class is representative of all of the test inputs taken from that class.
  - **Example**:EP for Triangle Program
    1. **Scalene Triangle**:
       - Valid Partitions:
         - A, B, and C are all different lengths and satisfy A + B > C, B + C > A, A + C > B.
       - Invalid Partitions:
         - Any two sides' sum is not greater than the third side.

    2. **Isosceles Triangle**:
       - Valid Partitions:
         - Two sides are of equal length and the third side satisfies the triangle inequality.
       - Invalid Partitions:
         - Two sides are of equal length but the third side does not satisfy the triangle inequality.
         - All three sides are different.

    3. **Equilateral Triangle**:
       - Valid Partitions:
         - All three sides are of equal length.
       - Invalid Partitions:
         - Any two or all three sides are of different lengths.

    4. **Right-Angled Triangle**:
       - Valid Partitions:
         - The sides satisfy the Pythagorean theorem (A² + B² = C²).
       - Invalid Partitions:
         - The sides do not satisfy the Pythagorean theorem.
  - **Test Cases for Equivalent Partitioning**

    | Equivalence Class  | Test Inputs          | Expected Outputs   |
    |--------------------|----------------------|---------------------|
    | ECscalene          | f(3, 5, 7), ...      | "Scalene"           |
    | ECisosceles        | f(2, 3, 3), ...      | "Isosceles"         |
    | ECequilateral      | f(7, 7, 7), ...      | "Equilateral"       |
    | ECright angled     | f(3, 4, 5), ...      | "Right Angled"      |
    | ECnon_triangle     | f(1, 1, 3), ...      | "Not a Triangle"    |
    | ECinvalid1         | f(-1, 2, 3), (0, 1, 3), ... | "Error Value"  |
    | ECinvalid2         | f(1, -2, 3), (1, 0, 3), ... | "Error Value"  |
    | ECinvalid3         | f(1, 2, -3), (1, 2, 0), ... | "Error Value" |

<!-- TOC --><a name="white-box-testng"></a>
### White Box Testng
- It is also known as ***structural testing***.
- Its goal is to test the internal code of the software. It tests the program at the level of source codde.
- Here the tester has the knowledge of actual source code of the software and what is tested is the inner structure of the program.
- It is the deep and detailed instruction of the logic and structure of the source code of an application or program.

**Example**:
- Login on Website
  - Check if the login screen is clearly visible to user or not.
  - Check if user is able to enter username and password in the provided place.
  - Check if the user is properly logged in
  - Check if proper error message is displayed

<!-- TOC --><a name="white-box-testing-strategies"></a>
#### White Box Testing Strategies
- **Coverage Based Testing**
  - **Statement Coverage (Node Coverage):** Ensure every statement in the program is executed at least once.
  - **Branch Coverage (Decision Coverage):** Ensure every possible path of each branch (if statements, loops, etc.) is taken at least once.
  - **Decision/Condition Coverage:** Ensure each condition in a decision is evaluated to both true and false.
  - **Multiple Condition Coverage:** Ensure all possible combinations of condition outcomes within each decision are exercised.
  - **Path Coverage:** Ensure every possible path through the program is executed at least once.

  - **Example**
    ```
    void main(void) {
        int x1, x2, x3;
        scanf("%d %d %d", &x1, &x2, &x3);
        if ((x1 > 1) && (x2 == 0))
            x3 = x3 / x1;
        if ((x1 == 2) || (x3 > 1))
            x3 = x3 + 1;
        while (x1 >= 2)
            x1 = x1 - 2;
        printf("%d %d %d", x1, x2, x3);
    }
    ```
  - **Test Cases for coverage criteria**

    | Coverage Criteria    | Test Inputs (x1, x2, x3)               | Execution Paths             |
    |----------------------|----------------------------------------|-----------------------------|
    | Statement Coverage   | (2, 0, 3)                              | ABCDEFGF                    |
    | Branch Coverage      | (2, 0, 3), (1, 1, 1)                   | ABCDEFGF, ABDF              |
    | Condition Coverage   | (1, 0, 3), (2, 1, 1)                   | ABDEF, ABDFGF               |
    | Decision/Condition   | (2, 0, 4), (1, 1, 1)                   | ABCDEFGF, ABDF              |
    | Multiple Condition   | (2, 0, 4), (2, 1, 1), (1, 0, 2), (1, 1, 1) | ABCDEFGF, ABDEFGF, ABDEF, ABDF |
    | Path Coverage        | (2, 0, 4), (2, 1, 1), (1, 0, 2), (4, 0, 0) | ABCDEFGF, ABDFGF, ABDEF, ABCDFGFGF |

- **Cyclomatic Complexity**
  - Cyclomatic complexity is a metric used to measure the complexity of a program. It is calculated using the control flow graph (CFG) of the program. The formula is:
  - `V(G)=E−N+2`, where V(G) is the cyclomatic complexity, E is the number of edges in the CFG, N is the number of nodes in the CFG
  - **Example**
   ```
   int sample(int a, int b) {
    while (a != b) {
        if (a > b)
            a = a - b;
        else
            b = b - a;
    }
    return a;
  }
   ```
  - The CFG for this program has 6 edges and 5 nodes, so the cyclomatic complexity is:
    - V(G)=6−5+2=3

- **Mutation Testing**
  - Mutation testing involves creating multiple copies of a program, each with a small modification (mutation). These modified programs (mutants) are then tested to see if the test cases can detect the changes. If a test case detects a change, the mutant is "killed"; otherwise, it is "live."
  - **Example**
    ```
    main(argc, argv)
    int argc;
    char *argv[];
    {
        int c = 0;
        if (atoi(argv[1]) < 3) {
            printf("Got less than 3\n");
            if (atoi(argv[2]) > 5)
                c = 2;
        } else {
            printf("Got more than 3\n");
        }
        exit(0);
    }
    ```
  - **Test Cases**
    | Test Case | Input | Output            |
    |-----------|-------|-------------------|
    | 1         | 2 4   | Got less than 3   |
    | 2         | 4 4   | Got more than 3   |
    | 3         | 4 6   | Got more than 3   |
    | 4         | 2 6   | Got less than 3   |
    | 5         | 4     | Got more than 3   |
  
  - **Mutant 1**
    - Change `if(atoi(argv[2]) > 5)` to `if(atoi(argv[2]) <= 5)`

  - **Mutant 2**
    - Change `if(atoi(argv[1]) < 3)` to `if(atoi(argv[1]) >= 3)`

  - **Mutant 3**
    - Change `int c = 0` to `int c = 3`

The ratio of killed mutants to total mutants indicates the effectiveness of the test suite.

<!-- TOC --><a name="testing-activities"></a>
## Testing Activities

Although testing varies between organizations, there is a cycle to testing:

- **Requirements Analysis**
  - Testing begins in the requirements phase of the software development life cycle (SDLC).

- **Design Analysis**
  - During the design phase, testers work with developers.
  - Determine what aspects of a design are testable and under what parameters.

- **Test Planning**
  - Includes Test Strategy and Test Plan(s).

- **Test Development**
  - Develop Test Procedures, Test Scenarios, Test Cases, and Test Scripts.

- **Test Execution**
  - Testers execute the software based on plans and tests.
  - Report any errors found to the development team.

- **Test Reporting**
  - Generate metrics and final reports on the test effort.
  - Determine if the software is ready for release.

- **Retesting the Defects**
  - Retest defects to check if they are eliminated.

<!-- TOC --><a name="levels-of-testing"></a>
## Levels of Testing

Mainly, software goes through three levels of testing:
- **Unit Testing**
- **Integration Testing**
- **System Testing**

<!-- TOC --><a name="unit-testing"></a>
### Unit Testing
- Verifies that a particular segment of source code works properly.
- Developers write test cases for all functions or methods.
- Isolate each part of the program to show that individual parts are correct.
- Will not catch every error (e.g., integration errors, performance problems).

<!-- TOC --><a name="integration-testing"></a>
### Integration Testing
- Combines and tests individual software modules as a group.
- Follows unit testing and precedes system testing.
- Verifies functional, performance, and reliability requirements placed on major design items.

<!-- TOC --><a name="system-testing"></a>
### System Testing
- Conducted on a complete, integrated system.
- Evaluates the system's compliance with its specified requirements.
- Tests the entire system against the Software Requirements Specification (SRS).
- Tends to be investigatory, focusing on design, behavior, and customer expectations.

<!-- TOC --><a name="acceptance-testing"></a>
### Acceptance Testing
- Conducted by customers to check whether the software meets all requirements.
- Tests may range from a few weeks to several months.

<!-- TOC --><a name="debugging-1"></a>
## Debugging

Debugging occurs as a consequence of successful testing.

<!-- TOC --><a name="characteristics-of-bugs"></a>
### Characteristics of Bugs
1. The symptom and the cause may be geographically remote.
2. The symptom may disappear temporarily when another error is corrected.
3. The symptom may be caused by non-errors (e.g., round-off inaccuracies).
4. The symptom may be caused by human error.
5. The symptom may be a result of timing problems.
6. Difficult to reproduce input conditions.
7. The symptom may be intermittent.
8. The symptom may be due to causes distributed across multiple tasks/processors.

<!-- TOC --><a name="life-cycle-of-a-debugging-task"></a>
### Life Cycle of a Debugging Task

- **Defect Identification/Confirmation**
  - Identify a problem in the system and create a defect report.
  - Assign defect to a software engineer.
  - Analyze the defect report:
    - What is the expected/desired behavior?
    - What is the actual behavior?
    - Is this a defect in the system?
    - Can the defect be reproduced?

- **Defect Analysis**
  - Understand the root cause of the problem.
  - Debug by starting a debugging tool and following the program step-by-step.

- **Defect Resolution**
  - Once the root cause is identified, make an appropriate change to fix it.

<!-- TOC --><a name="debugging-approaches"></a>
## Debugging Approaches
- **Brute Force**
  - Memory dumps, run-time traces, WRITE statements.
- **Backtracking**
  - Trace source code backward from the symptom to the error.
- **Cause Elimination**
  - Identify possible causes and conduct tests to eliminate them.

<!-- TOC --><a name="testing-tools"></a>
## Testing Tools

Different categories of tools used for testing:

- **Data Acquisition**
  - Tools that acquire data for testing.
- **Static Measurement**
  - Analyze source code without executing test cases.
- **Dynamic Measurement**
  - Analyze source code during execution.
- **Simulation**
  - Simulate functions of hardware or other externals.
- **Test Management**
  - Assist in planning, development, and control of testing.
- **Cross-Functional Tools**
  - Tools that cross the bounds of preceding categories.

<!-- TOC --><a name="examples-of-commercial-software-testing-tools"></a>
## Examples of Commercial Software Testing Tools

<!-- TOC --><a name="rational-test-realtime-unit-testing"></a>
### Rational Test RealTime Unit Testing
- **Kind of Tool**
  - Automates C, C++ software component testing.
- **Organization**
  - IBM Rational Software
- **Description**
  - Performs black-box/functional testing.
  - Integrated with native development environments (Unix and Windows).
- **Platforms**
  - Available for most development and target systems including Windows and Unix.

<!-- TOC --><a name="aqtest"></a>
### AQtest
- **Kind of Tool**
  - Automated support for functional, unit, and regression testing.
- **Organization**
  - AutomatedQA Corp.
- **Description**
  - Automates and manages functional tests, unit tests, and regression tests.
  - Supports white-box testing and external tests.
- **Platforms**
  - Windows 95, 98, NT, or 2000.

<!-- TOC --><a name="csunit"></a>
### csUnit
- **Kind of Tool**
  - Unit Testing framework for Microsoft .NET (freeware).
- **Organization**
  - csUnit.org
- **Description**
  - Targets test-driven development using .NET languages.
- **Platforms**
  - Microsoft Windows

<!-- TOC --><a name="sahi"></a>
### Sahi
- **Description**
  - Automation and testing tool for web applications.
  - Developed in Java and JavaScript.
  - Uses simple JavaScript to execute events on the browser.
  - Features in-browser controls, text-based scripts, Ant support, and multi-threaded playback.
  - Runs as a proxy server.
- **Platforms**
  - OS independent. Needs at least JDK1.4.