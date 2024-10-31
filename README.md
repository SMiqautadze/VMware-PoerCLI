Here's a README file for the repository based on best practices for PowerCLI scripts, assuming that the repository contains a variety of PowerCLI scripts and modules.

---

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

3. **Run Scripts**:
   Execute each script as needed. Refer to each script's documentation and usage notes below.

## Scripts

### 1. VM Creation (`Create-VM.ps1`)
   - **Description**: Automates the creation of a new virtual machine.
   - **Parameters**:
     - `-VMName`: Name of the virtual machine.
     - `-ResourcePool`: Resource pool to deploy the VM to.
     - `-Datastore`: Datastore where the VM files will reside.
     - `-Template`: Template to use for the VM creation.
   - **Example**:
     ```powershell
     .\Create-VM.ps1 -VMName "NewVM" -ResourcePool "ProdPool" -Datastore "Datastore01" -Template "WindowsTemplate"
     ```

### 2. VM Reporting (`VM-Report.ps1`)
   - **Description**: Generates a report of VMs and their resource utilization.
   - **Parameters**: None.
   - **Example**:
     ```powershell
     .\VM-Report.ps1
     ```

### 3. Event Auditing (`Audit-UserEvents.ps1`)
   - **Description**: Retrieves events for a specific user within vCenter.
   - **Parameters**:
     - `-UserName`: Specify the username to audit.
   - **Example**:
     ```powershell
     .\Audit-UserEvents.ps1 -UserName "Domain\User"
     ```

### 4. VM Snapshots (`Manage-Snapshots.ps1`)
   - **Description**: Manages snapshots for VMs, including creating, deleting, and reporting snapshots.
   - **Parameters**:
     - `-Action`: Action to perform (`Create`, `Delete`, `Report`).
     - `-VMName`: Target VM for snapshot action.
   - **Example**:
     ```powershell
     .\Manage-Snapshots.ps1 -Action "Create" -VMName "MyVM"
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

---

Let me know if you'd like more details on specific scripts or any additional sections for the README.
