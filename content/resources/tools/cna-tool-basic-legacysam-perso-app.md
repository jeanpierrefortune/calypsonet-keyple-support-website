---
title: Calypso Basic Legacy SAM Personalization Tool Tutorial
type: book
toc: true
weight: 1
---

This tutorial will guide you through the process of personalizing a **SAM CPP** needed for Calypso Basic card key
injection.

### Hardware Requirements

This tool requires two PC/SC contact readers:

* **Target SAM Reader:** This reader holds the virgin **SAM CPP** you want to personalize.
* **Origin SAM Reader:** This reader contains the **SAM SP** with the desired keys and settings.

### Installation

1. Download the appropriate installation package for your operating system from
   the [download page](https://keyple-support.calypsonet.org/tools/download/):
    * **Windows:** `.msi` package
    * **macOS:** `.dmg` package
    * **Linux:** `.deb` package
2. **Windows:** Double-click the `.msi` package to start the installation.
3. **macOS:** Open the `.dmg` file and drag the application to the Applications folder.
4. **Linux:** Use your distribution's package manager to install the `.deb` package.
5. **Important note:** The installer does not automatically create a shortcut in the Start Menu (Windows) or
   Applications menu (macOS). You need to create one manually.

### Launching the Tool

1. After installation, find the executable in the installation directory:
    * **Windows:** `C:\\Program Files\\cna-tool-basic-legacysam-perso-app\\`
    * **macOS:** `/Applications/cna-tool-basic-legacysam-perso-app/`
    * **Linux:** `/opt/cna-tool-basic-legacysam-perso-app/` (or your user's home directory)
2. Double-click the executable to launch the Calypso Basic Legacy SAM Personalization Tool.

### Application Interface

The application window has a top menu and three tabs:

#### Settings Menu

1. Click the **Settings** menu.
2. Select the **Target SAM Reader** name. This is where you will insert your blank SAM.
3. Select the **Origin SAM Reader** name. This SAM contains the data you want to transfer to the target SAM.
4. Enter the **Origin SAM Unlock Value** if required.

#### Tabs

* **SAM Dump:** Shows the detailed information and parameters of the SAM inserted in the target SAM reader.
* **SAM Personalization:** Configure and execute the personalization process.
* **Application Info:** View logs and events related to the application and SAM readers. Useful for troubleshooting.

### Personalizing a SAM CPP

1. Select the **SAM Personalization** tab.
2. Insert a virgin SAM in the target SAM reader.
3. Insert the SAM SP in the origin SAM reader.
4. Set the parameters:
    * Parameter version and owner data (informative)
    * System keys KVC
    * Work keys KIF and KVC
    * Lock parameters
5. Click **Execute** to personalize your SAM.

### Refreshing Reader Detection

If you connect or disconnect SAM readers while the application is running, you might need to switch between the tabs (
SAM Dump, SAM Personalization, Application Info) for the application to recognize the changes.

### Screenshots

Installation
![Installation](/media/cna-tool-basic-legacysam-perso-app/install-dialog.png)

Settings
![Settings](/media/cna-tool-basic-legacysam-perso-app/settings-dialog.png)

SAM dump
![SAM dump](/media/cna-tool-basic-legacysam-perso-app/dump-tab.png)

SAM personalization
![SAM personalization](/media/cna-tool-basic-legacysam-perso-app/personalization-tab.png)

Application info
![Application info](/media/cna-tool-basic-legacysam-perso-app/info-and-logs-tab.png)

### Disclaimer

This tool is provided by CNA for its members. Only active CNA members are authorized to use this tool. A member is not
authorized to distribute this tool to other parties.

## User Requirements and Responsibilities

* **Target Audience:** Users familiar with SAM personalization and the Calypso system.
* **Prerequisites:** Necessary hardware (SAM readers) and software (drivers) installed and configured correctly.
* **Responsibilities:** Ensure the correct selection of target and origin SAMs, and the proper handling of unlock values
  and other sensitive information.
* **Usage:** Authorized personnel only. Misuse or unauthorized distribution is strictly prohibited.