# Package Managers for Installing Applications

## Overview
Previously, you learned about Linux distributions and that different distributions derive from different sources, such as Debian or Red Hat Enterprise Linux distribution. You were also introduced to package managers, and learned that Linux applications are commonly distributed through package managers. In this reading, you’ll apply this knowledge to learn more about package managers.

## Introduction to Package Managers
- **Package**: A piece of software that can be combined with other packages to form an application. Some packages may be large enough to form applications on their own.
  - **Dependencies**: Supplemental files used to run an application.
- **Package Manager**: A tool that helps users install, manage, and remove packages or applications. Linux uses multiple package managers.

  > **Note**: It’s important to use the most recent version of a package when possible. The most recent version has the most up-to-date bug fixes and security patches. These help keep your system more secure.

## Types of Package Managers
Many commonly used Linux distributions are derived from the same parent distribution. For example, KALI LINUX ™, Ubuntu, and Parrot all come from Debian. CentOS comes from Red Hat.

### Debian-derived Distributions
- **dpkg**: A package manager for Debian-based distributions.
  - **File Extension**: `.deb`
  - **Example**: `Package_Version-Release_Architecture.deb`

### Red Hat-derived Distributions
- **Red Hat Package Manager (RPM)**: A package manager for Red Hat-based distributions.
  - **File Extension**: `.rpm`
  - **Example**: `Package-Version-Release_Architecture.rpm`

## Package Management Tools
In addition to package managers like RPM and dpkg, there are also package management tools that allow you to easily work with packages through the shell. Package management tools are sometimes utilized instead of package managers because they allow users to more easily perform basic tasks, such as installing a new package.

### Advanced Package Tool (APT)
- **Used With**: Debian-derived distributions.
- **Function**: Manages, searches, and installs packages from the command-line interface.

### Yellowdog Updater Modified (YUM)
- **Used With**: Red Hat-derived distributions.
- **Function**: Manages, searches, and installs packages from the command-line interface. Works with `.rpm` files.

## Key Takeaways
- **Packages**: Pieces of software that can be combined to form applications. Managed using package managers.
- **Package Managers**: Tools to install, manage, and remove packages. Different package managers are used for different Linux distributions.
  - **Debian-derived Distributions**: Use `dpkg` and tools like `APT`.
  - **Red Hat-derived Distributions**: Use `RPM` and tools like `YUM`.
- **Package Management Tools**: Facilitate working with packages through the shell, allowing for easy management, searching, and installation of packages.

Understanding package managers and their corresponding tools is crucial for efficiently managing software on Linux systems, ensuring systems are secure and up-to-date.