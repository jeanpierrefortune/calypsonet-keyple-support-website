---
title: Calypso Analyzer Tool Tutorial
type: book
toc: true
weight: 1
---

This tutorial guides you through the use of the CNA Tool Card Analyzer App Suite, a set of two command-line tools for
analyzing and verifying Calypso-compliant smart cards.

**What is the CNA Tool Card Analyzer App Suite?**

The CNA Tool Card Analyzer App Suite consists of two command-line tools:

* **Tool_AnalyzeCardFileStructure:** analyzes the file structure of a Calypso smart card and generates a JSON report
  containing the card's structure and application data.
* **Tool_CheckCardFileStructure:** checks the file structure of a Calypso card against a given JSON file containing the
  expected file structure.

**Why use the CNA Tool Card Analyzer App Suite?**

This suite helps developers and testers:

*   Understand the data stored on a Calypso card.
*   Verify compliance with Calypso specifications.
*   Troubleshoot potential issues.
*   Compare card structure against a predefined template.


## Prerequisites

* **Java:** ensure you have a Java Runtime Environment (JRE) installed on your system. You can download it
  from [www.java.com](www.java.com).
* **PC/SC card reader:** a contactless PC/SC compliant card reader is required to interact with the Calypso card.

## Download the Apps

1. Go to the [releases page](https://github.com/calypsonet/calypso-card-analyzer/releases) to download the latest
   version of the application suite.
2.  Download the executable JAR files:
    *   `Tool_AnalyzeCardFileStructure-x.y.z.jar`
    *   `Tool_CheckCardFileStructure-x.y.z.jar`

## Run the Apps

### Analyze a Card (Tool_AnalyzeCardFileStructure)

1. Open a terminal or command prompt.
2. Navigate to the directory containing `Tool_AnalyzeCardFileStructure-x.y.z.jar`.
3. Place your Calypso card on the reader.
4. Execute the following command:

```bash
java -jar Tool_AnalyzeCardFileStructure-x.y.z.jar [readerNameRegex]
```

* `readerNameRegex` (optional): a regular expression to filter the card readers. If not provided, a default regex (
  `.*(ASK.*|Identiv.*2|ACS ACR122U|SCR3310).*`) is used.

5. The analysis results will be displayed in the terminal and JSON file containing the card structure will be saved.

### Check a card structure (Tool_CheckCardFileStructure)

1. Open a terminal or command prompt.
2. Navigate to the directory containing `Tool_CheckCardFileStructure-x.y.z.jar`.
3. **Obtain a JSON file defining the expected card structure:**
    * You can use a pre-defined JSON file from the `card_profiles` directory in the GitHub repository. The file names
      indicate the type of product they correspond to.
     * Alternatively, you can create your own JSON file defining the expected structure.
4. Place your Calypso card on the reader and keep it still.
5. Execute the following command:

```bash
java -jar Tool_CheckCardFileStructure-x.y.z.jar <path-to-json-file> [readerNameRegex] 
```

*   `<path-to-json-file>`: **(Required)** The path to the JSON file containing the expected card structure. This argument should be replaced with the actual path to your JSON file (e.g., `card_profiles/my_card_profile.json`).
*   `readerNameRegex` (optional): a regular expression to filter the card readers. If not provided, a default regex (`.*(ASK.*|Identiv.*2|ACS ACR122U|SCR3310).*`) is used.

6.  The tool will compare the card's structure with the provided JSON file and display any differences.

## Troubleshooting

* **Card not found:** ensure your card reader is correctly connected and installed, and that the card is presented
  correctly.
* **Java not found:** ensure Java is installed and that its directory is added to your system's PATH environment variable.
* **Error messages:** carefully read any error messages displayed in the terminal for clues on how to resolve the issue.


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
