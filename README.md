# VMware PowerCLI Scripts

**Author:** SMiqautadze

Welcome to the **VMware PowerCLI** repository, a collection of useful PowerCLI scripts for managing and automating VMware environments.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Scripts](#scripts)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains PowerCLI scripts aimed at simplifying tasks and automating operations within VMware environments. These scripts provide solutions for tasks such as VM provisioning, configuration, monitoring, and reporting.

## Prerequisites

- **VMware PowerCLI**: These scripts are built using PowerCLI, so make sure PowerCLI is installed. To install PowerCLI, you can run:
  
  ```powershell
  Install-Module -Name VMware.PowerCLI -Scope CurrentUser
  ```

- **PowerShell**: Ensure you have PowerShell 5.1 or newer installed.

- **VMware Permissions**: Some scripts require specific VMware permissions. Refer to each script's comments to ensure your account has the required privileges.

## Getting Started

1. **Clone the Repository**:
   
   ```bash
   git clone https://github.com/SMiqautadze/VMware-PoerCLI.git
   cd VMware-PoerCLI
   ```

2. **Connect to vCenter**:
   Before running the scripts, connect to your vCenter Server using:

   ```powershell
   Connect-VIServer -Server your_vcenter_server -User your_username -Password your_password
   ```
## Usage

1. **Connecting to vCenter**:
   Start by connecting to the VMware environment with `Connect-VIServer` before running any script.

2. **Executing Scripts**:
   Each script in this repository is self-contained. Review the **Parameters** section for each script above, and execute them by passing the required parameters as shown in the examples.

3. **Exporting Data**:
   Many scripts include options to export output to CSV or text files. Adjust the file paths within each script as necessary.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements, or create issues for bug reports and feature requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
