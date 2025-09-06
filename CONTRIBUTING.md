# Contributing to AI vector Forge

First off, thank you for considering contributing! This project is a collaborative space for creating and remixing SVGs, and we welcome all contributions.

## Core Principles

Before you start, please familiarize yourself with our core principles:

1.  **Show, Don't Tell**: We believe in providing real, working examples. Please don't add empty or placeholder files. Every new workshop should contain a real, first-draft SVG.
2.  **No Fluff**: Keep descriptions and documentation clear, concise, and technical.
3.  **Self-Contained**: Every SVG must be a single file with no external dependencies or JavaScript. All CSS must be inline within a `<style>` tag.
4.  **Accessible**: All SVGs must include `<title>` and `<desc>` tags for accessibility.
5.  **Remixable**: Write clean, commented code so that others can easily understand and build upon your work.

## How to Add a New SVG

All SVGs in this project are organized into "workshops" within different "namespaces".

### 1. Choose a Namespace

First, decide which namespace your SVG belongs to. The current namespaces are:

- `/logos`: For logos for projects, brands, etc.
- `/gallery`: For demo seeds, examples, and artistic pieces designed to be remixed.

### 2. Create Your Workshop

1.  Inside the namespace directory (e.g., `/logos`), create a new directory for your workshop. The directory name should be the name of your SVG (e.g., `my-new-logo`).
2.  Inside your new workshop directory (`/logos/my-new-logo/`), create your SVG file. **The file name must match the directory name** (e.g., `my-new-logo.svg`).
3.  Create a `README.md` file inside your workshop directory. This README should include a preview of your SVG and a brief description.
4.  (Optional) You can also include an `AGENTS.md` file if you have specific instructions for AI assistants working on your SVG, or a folder with source materials (e.g. `/logos/my-new-logo/sources/`).

### 3. Submitting Your Contribution

Once your workshop is ready, please submit a Pull Request. We will review it and merge it as soon as possible.

Thank you for helping to grow the forge!
