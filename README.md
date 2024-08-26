# Malware Scanning Tool - Binary Static Analysis

## Overview

This tool is a comprehensive malware scanner designed to analyze executable files and JAR files for potential security threats. It combines signature-based scanning using ClamAV with behavioral analysis through decompilation and pattern matching. The tool utilizes custom Semgrep rules, which were created based on extensive analysis of various malicious scripts, providing a unique and tailored approach to detecting potential threats.

## Features

- Signature-based scanning using ClamAV
- Decompilation of executables using Ghidra
- Decompilation of JAR files using JD-CLI
- Pattern matching on decompiled code using Semgrep with custom-developed rules
- Supports both executable and JAR file scanning
- Command-line interface with help manual

## Prerequisites

Before using this tool, ensure you have the following software installed on your system:

1. Python 3.6 or higher
2. ClamAV
3. Ghidra
4. JD-CLI (Java Decompiler)
5. Semgrep

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/azizElb444/Binary_Scan_Tool.git
   cd Binary_Scan_Tool
   ```

2. Ensure all prerequisites are installed and properly configured.

3. Update the paths in the script to match your system configuration:
   - Ghidra project directory
   - JD-CLI jar file location
   - Semgrep rule files

## Usage

The tool can be used to scan either C executable files or JAR/WAR files.

### Scanning a C Executable

```
python malware_scan.py -exec /path/to/executable
```

### Scanning a JAR/WAR File

```
python malware_scan.py -jar /path/to/jarfile.jar
```

### Viewing Help

```
python malware_scan.py -h
```

## Output

The tool will provide console output during the scanning process. Additionally, it generates a JSON report (`malware-scan.json`) with detailed findings from the Semgrep analysis.

## Contributing

Contributions to improve the tool are welcome. Please feel free to submit pull requests or open issues to discuss potential enhancements.



