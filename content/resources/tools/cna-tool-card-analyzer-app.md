---
title: Calypso Analyzer Tool Tutorial
type: book
toc: true
weight: 1
---

This tutorial guides you through using the CNA Tool Card Analyzer App Suite, a set of command-line tools for analyzing
and verifying Calypso-compliant smart cards.

**What is the CNA Tool Card Analyzer App Suite?**

The CNA Tool Card Analyzer App Suite consists of two command-line tools:

* **Tool_AnalyzeCardFileStructure:** Analyzes the file structure of a Calypso smart card and generates a JSON report
  containing the card's structure and application data.
* **Tool_CheckCardFileStructure:** Checks the file structure of a Calypso card against a given JSON file containing the
  expected file structure.

**Why use the CNA Tool Card Analyzer App Suite?**

This suite helps developers and testers:

*   Understand the data stored on a Calypso card.
*   Verify compliance with Calypso specifications.
*   Troubleshoot potential issues.
*   Compare card structure against a predefined template.


## Prerequisites

* **Java:** Ensure you have Java Runtime Environment (JRE) installed on your system. You can download it
  from [www.java.com](www.java.com).
* **PC/SC card reader:** A contactless PC/SC compliant card reader is required to interact with the Calypso card.

## Downloading the Apps

1. Go to the [releases page](https://github.com/calypsonet/calypso-card-analyzer/releases) to download the latest
   version of the application suite.
2.  Download the executable JAR files:
    *   `Tool_AnalyzeCardFileStructure-x.y.z.jar`
    *   `Tool_CheckCardFileStructure-x.y.z.jar`


## Running the Apps

### Analyzing a Card (Tool_AnalyzeCardFileStructure)

1.  Open a terminal or command prompt.
2.  Navigate to the directory containing `Tool_AnalyzeCardFileStructure-x.y.z.jar`.
3.  Execute the following command:

```bash
java -jar Tool_AnalyzeCardFileStructure-x.y.z.jar
```
4.  Present your Calypso card to the reader when prompted.
5.  The analysis results will be displayed in JSON format in the terminal.

**Saving the results:**

```bash
java -jar Tool_AnalyzeCardFileStructure-x.y.z.jar > analysis_results.json
```


### Checking Card Structure (Tool_CheckCardFileStructure)

1.  Open a terminal or command prompt.
2.  Navigate to the directory containing `Tool_CheckCardFileStructure-x.y.z.jar`.
3.  Prepare a JSON file (`expected_structure.json`) defining the expected card structure.
4.  Execute the following command:

```bash
java -jar Tool_CheckCardFileStructure-x.y.z.jar expected_structure.json
```
5.  Present your Calypso card to the reader when prompted.
6.  The tool will compare the card's structure with the provided JSON file and display any differences.

## Command-line Options

Each tool may support additional command-line options. Use the `-h` or `--help` flag to display the available options
for each tool:

```bash
java -jar Tool_AnalyzeCardFileStructure-x.y.z.jar -h
java -jar Tool_CheckCardFileStructure-x.y.z.jar -h 
```

## Troubleshooting

* **Card not detected:** Ensure your card reader is correctly connected and installed, and that the card is presented
  correctly.
* **Java not found:** Make sure Java is installed and added to your system's PATH environment variable.
* **Error messages:** Carefully read any error messages displayed in the terminal for clues on how to resolve the issue.


## Disclaimer

This software is provided under the terms of the Eclipse Public License 2.0. See the LICENSE file for more information.

## User Requirements and Responsibilities

* **Target Audience:**  Developers, testers, and anyone interested in analyzing or verifying Calypso card data. Basic
  knowledge of smart card technology and command-line interfaces is recommended.
* **Prerequisites:**  Java Runtime Environment, a PC/SC compliant contactless card reader, and necessary drivers.
* **Responsibilities:**
    * Ensure proper handling of the card and responsible use of the analysis data.
    * If you modify the software and distribute it, you must make your source code modifications available under the EPL
      2.0.
    * You must include the original copyright notices and the full text of the EPL 2.0 license with any distribution.
* **Usage:**  The software is available to everyone under the terms of the EPL 2.0. You are free to use, modify, and
  distribute it, even in commercial settings, as long as you comply with the license terms.

This tutorial provides a basic guide for using the CNA Tool Card Analyzer App Suite. For more advanced usage and
detailed information, please refer to the application documentation and the Calypso specifications.
