# Contributing to ask

Thank you for your interest in contributing!

## How to Contribute

1. Fork the repository on GitHub.
2. Clone your fork:
```bash
   git clone https://github.com/your-username/ask.git
```
3. Create a new branch for your change:
```bash
   git checkout -b feature/your-feature-name
```
4. Make your changes. Keep the script POSIX-compatible where possible.
5. Test your changes manually with at least one piped input and one argument-based call.
6. Commit with a clear, descriptive message:
```bash
   git commit -m "Add timeout flag support"
```
7. Push and open a Pull Request against the `main` branch.

## Code Style

- Use `shellcheck` to lint your changes before submitting.
- Keep functions small and well-commented.
- Avoid adding new dependencies beyond `curl` and `jq`.

## Reporting Issues

Open a GitHub Issue with a clear description and a minimal reproduction case.