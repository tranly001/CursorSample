# Cursor IDE Setup and AI Coding Assistant Integration

## Overview

This repository documents the installation and configuration of Cursor IDE along with AI coding assistant integrations, including Claude Code and Codex.

## Tools Installed

* Cursor IDE
* Claude Code Extension
* Codex Extension
* Git
* GitHub

## Steps Completed

### 1. Installed Cursor IDE

Downloaded and installed Cursor IDE from:

https://cursor.com/

### 2. Installed Claude Code Extension

Initially attempted to install Claude Code through Cursor's Extensions marketplace as instructed.

### 3. Installed Codex Extension

Attempted to locate and install the Codex extension through Cursor's plugin system and logged in successfully after installation.

### 4. Created a Public GitHub Repository

Created a public GitHub repository to document the setup process.

### 5. Opened Repository in Cursor

Cloned/opened the GitHub repository within Cursor IDE.

### 6. Created Documentation

Created this README.md file describing the setup process, challenges encountered, and solutions.

### 7. Committed and Pushed Changes

Committed all changes and pushed the repository to GitHub.

## Issues Encountered and Solutions

### Issue 1: Extensions Tab Missing in Cursor (Windows)

**Problem:**

The instructions referenced an Extensions tab, but the Windows installation of Cursor did not display the expected Extensions panel. Additionally, searching through the available plugins did not show either "Claude Code" or "Codex".

**Solution:**

After researching the issue, I found that Cursor was not automatically detecting Claude Code even though Cursor is based on Visual Studio Code.

I followed a manual installation process using the Claude Code VSIX package.

#### Verify Claude Code Installation

From a terminal:

```bash
claude
```

Then inside Claude Code:

```bash
/doctor
```

This confirmed the installation path:

```text
You are running Claude Code from your local installation (~/.claude/local).
```

#### Manually Install the Claude Code Extension

From a terminal:

```bash
cursor --install-extension ~/.claude/local/node_modules/@anthropic-ai/claude-code/vendor/claude-code.vsix
```

Installation completed successfully.

#### Verify Cursor Detection

After reopening Cursor, I verified the integration by running:

```bash
claude
```

Then:

```bash
/ide
```

Cursor appeared as an available IDE option, confirming that the extension was correctly installed.

### Why the Workaround Was Necessary

The official Claude Code IDE integration process did not properly detect Cursor IDE. Since Cursor is a VS Code-based editor that supports VSIX extensions, manually installing the extension package provided a working solution.

## References

### Official Documentation

https://docs.anthropic.com/en/docs/claude-code/ide-integrations

### Related GitHub Issue

https://github.com/anthropics/claude-code/issues/1279

## Result

Successfully configured Cursor IDE, integrated Claude Code through manual installation, installed Codex, connected the development environment to GitHub, and published the repository documentation.
