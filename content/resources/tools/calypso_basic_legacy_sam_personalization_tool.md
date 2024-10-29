---
title: Calypso Basic Legacy SAM Personalization Tool Tutorial
toc: false
weight: 1
---

This tutorial will guide you through the process of personalizing a **SAM CPP** needed for **Calypso Basic** card keys injection.

### Hardware Requirements

This tool requires two PC/SC contact readers:

* **Target SAM Reader:** This reader holds the virgin **SAM CPP** you want to personalize. The tool reads its data to display its
  current state and then writes the new configuration during personalization.
* **Origin SAM Reader:** This reader contains the **SAM SP** with the desired keys and settings that you want to inject into
  the target **SAM CPP**.

### Installation

1. Download the appropriate installation package for your operating system from
   the [download page](https://keyple-support.calypsonet.org/tools/download/):
    * **Windows:** `.msi` package
    * **macOS:** `.dmg` package
    * **Linux:** `.deb` package
2. **Windows:** Double-click the `.msi` package to start the installation process.
3. **macOS:**  Open the `.dmg` file and drag the application to the Applications folder.
4. **Linux:** Use your distribution's package manager to install the `.deb` package.
5. **Important note:** Currently, the installer does not automatically create a shortcut in the Start Menu (Windows) or
   Applications menu (macOS). If you want quick access, you will need to create a shortcut manually.

### Launching the Tool

1. Once the installation is complete, you can find the executable in the installation directory. The default location
   varies depending on your operating system:
    * **Windows:** `C:\\Program Files\\cna-tool-basic-legacysam-perso-app\\`
    * **macOS:** `/Applications/cna-tool-basic-legacysam-perso-app/`
    * **Linux:** `/opt/cna-tool-basic-legacysam-perso-app/` (or in your user's home directory if you installed it
      locally)
2. Double-click the executable to launch the **Calypso Basic Legacy SAM Personalization Tool**.
3. The tool will open with the SAM Dump tab selected.

### Application interface

The application window has a top menu and three tabs:

#### Settings menu entry

1. Select the Settings menu.
2. Select the Target SAM Reader name from the drop-down list. This is where your blank SAM should be inserted.
3. Select the Origin SAM Reader name from the drop-down list. This SAM contains the data you want to transfer to the target SAM.
4. Enter the Origin SAM Unlock Value in the text field, if required.

#### Tabs
* **SAM Dump:** Shows the detailed information and parameters of the SAM inserted in the target SAM reader. This allows you to view the SAM's current state before and after personalization.
* **SAM Personalization:** Allows you to configure and execute the personalization process. You can choose which parameters to transfer, and inject them into a blank target SAM. You can also export/import the personalization settings.
* **Application Info:** Displays logs and events related to the application and SAM readers, which can be useful for
  troubleshooting.

### Creating a SAM CPP

1. Select the SAM Personalization tab.
2. Insert a virgin SAM in the target SAM reader.
3. Insert the SAM SP in the origin SAM reader.
4. Set the parameters such as
   * parameter version and owner data (informative)
   * system keys KVC
   * work keys KIF and KVC
   * Lock parameters
5. Click the "Execute" button to inject the parameters and keys into the blank SAM. The tool will personalize your SAM
   by writing the parameters and transferring the keys from the origin SAM to the target SAM.

### Refreshing Reader Detection

If you connect or disconnect SAM readers while the application is running, you might need to switch between the tabs (
SAM Dump, SAM Personalization, Application Info) for the application to recognize the changes.

### Screenshots

Installation
![Installation](/media/calypso_basic_legacy_sam_personalization_tool/install-dialog.png)

Settings
![Settings](/media/calypso_basic_legacy_sam_personalization_tool/settings-dialog.png)

SAM dump
![SAM dump](/media/calypso_basic_legacy_sam_personalization_tool/dump-tab.png)

SAM personalization
![SAM personalization](/media/calypso_basic_legacy_sam_personalization_tool/personalization-tab.png)

Application info
![Application info](/media/calypso_basic_legacy_sam_personalization_tool/info-and-logs-tab.png)

### Disclaimer

This tool is provided by CNA for its members. Only active CNA members are authorized to use this tool. A member is not
authorized to distribute this tool to other parties.

## User Expectations

* **Target Audience:** This tool is designed for users familiar with SAM personalization and the Calypso system. Basic
  knowledge of smart card technology and security concepts is assumed.
* **Prerequisites:** Users should have the necessary hardware (SAM readers) and software (drivers) installed and
  configured correctly.
* **Responsibilities:** Users are responsible for ensuring the correct selection of target and origin SAMs, as well as
  the proper handling of unlock values and other sensitive information.
* **Usage:** The tool is intended for authorized personnel only. Any misuse or unauthorized distribution is strictly
  prohibited.