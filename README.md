# UserPM (User Package Manager)

UserPM is a powerful, user-level package manager for Windows that allows developers and users to install, manage, and update software packages without requiring administrative privileges. It's designed to streamline the process of setting up development environments and prototyping, making it easier to work with various tools and libraries.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Use Cases](#use-cases)
5. [Configuration](#configuration)
6. [Troubleshooting](#troubleshooting)
7. [Contributing](#contributing)
8. [License](#license)

## Features

- User-level installations (no admin rights required)
- Package repository with easy submission process
- Command-line interface for all operations
- Package search functionality
- Install, uninstall, and update packages
- Automatic dependency management
- Custom package format (.upm) for easy distribution
- Environment variable management
- Logging and error handling

## Installation

### Prerequisites

- Windows 7 or later
- Python 3.7 or later
- pip (Python package installer)

### Steps

1. Open a command prompt or PowerShell window.

2. Install UserPM using pip:

   ```
   pip install userpm --user
   ```

3. Add the UserPM installation directory to your PATH:

   ```
   python -m site --user-site
   ```

   Copy the output path and add `\Scripts` to the end. Then add this path to your system's PATH environment variable.

4. Verify the installation by running:

   ```
   userpm --version
   ```

   This should display the version number of UserPM.

## Usage

UserPM provides a command-line interface for all operations. Here are the basic commands:

- Install a package:
  ```
  userpm install <package_name>
  ```

- Uninstall a package:
  ```
  userpm uninstall <package_name>
  ```

- Update a package:
  ```
  userpm update <package_name>
  ```

- Search for packages:
  ```
  userpm search <query>
  ```

- List installed packages:
  ```
  userpm list
  ```

- Update UserPM itself:
  ```
  userpm self-update
  ```

## Use Cases

### 1. Setting Up a Python Development Environment

Imagine you're starting a new Python project and need several tools and libraries. With UserPM, you can quickly set up your environment:

```
userpm install python
userpm install pip
userpm install virtualenv
userpm install pytest
userpm install black
```

These commands will install Python, pip, virtualenv for environment management, pytest for testing, and black for code formatting, all without requiring admin rights.

### 2. Installing Node.js and npm

For web development projects, you might need Node.js and npm:

```
userpm install nodejs
userpm install npm
```

UserPM will handle the installation and automatically add the necessary paths to your user environment variables.

### 3. Setting Up a C++ Development Environment

If you're working on a C++ project, you can easily set up your toolchain:

```
userpm install mingw
userpm install cmake
userpm install boost
```

This will install the MinGW compiler, CMake build system, and the Boost C++ libraries.

### 4. Installing Database Tools

For database work, you might need various clients and tools:

```
userpm install mysql-client
userpm install postgresql
userpm install mongodb
userpm install redis
```

These commands will install clients for MySQL, PostgreSQL, MongoDB, and Redis, allowing you to connect to and work with these databases.

### 5. Setting Up Version Control Tools

For version control, you can easily install Git and related tools:

```
userpm install git
userpm install gitflow
userpm install sourcetree
```

This installs Git, the GitFlow branching model extension, and SourceTree GUI client.

### 6. Installing Text Editors and IDEs

UserPM can help you install your preferred development environments:

```
userpm install vscode
userpm install sublime-text
userpm install notepadplusplus
```

These commands will install Visual Studio Code, Sublime Text, and Notepad++.

### 7. Setting Up a Ruby on Rails Environment

For Ruby on Rails development:

```
userpm install ruby
userpm install rails
userpm install sqlite
```

This installs Ruby, the Rails framework, and SQLite database.

### 8. Installing Build Tools

For various build and automation tasks:

```
userpm install make
userpm install gradle
userpm install maven
userpm install ant
```

These commands install Make, Gradle, Maven, and Ant build tools.

## Configuration

UserPM uses a configuration file located at `~/.userpm/config.yaml`. You can modify this file to change settings such as:

- Repository URL
- Default installation directory
- Logging level and file location

Example configuration:

```yaml
repository:
  url: https://example.com/userpm/repo
settings:
  install_dir: ~/UserPM
  bin: true
logging:
  level: INFO
  file: ~/.userpm/userpm.log
```

## Troubleshooting

If you encounter any issues while using UserPM, try the following:

1. Ensure your PATH is correctly set up.
2. Check the log file at `~/.userpm/userpm.log` for error messages.
3. Verify that you have an active internet connection for package downloads.
4. Run `userpm self-update` to ensure you're using the latest version.

If problems persist, please open an issue on our GitHub repository with a detailed description of the problem and the steps to reproduce it.

## Contributing

We welcome contributions to UserPM! If you'd like to contribute, please:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Write tests for your changes.
4. Ensure all tests pass.
5. Submit a pull request with a clear description of your changes.

For more details, please see our [CONTRIBUTING.md](CONTRIBUTING.md) file.

## License

UserPM is released under the MIT License. See the [LICENSE](LICENSE) file for details.

---

We hope UserPM makes your Windows development experience smoother and more efficient. If you have any questions, suggestions, or feedback, please don't hesitate to reach out or open an issue on our GitHub repository. Happy coding!
