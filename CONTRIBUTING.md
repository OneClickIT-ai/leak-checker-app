# Contributing to Database Leak Checker

Thank you for your interest in contributing to the Database Leak Checker project! We welcome contributions from developers, security researchers, and the open-source community. This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Submitting Pull Requests](#submitting-pull-requests)
- [Development Guidelines](#development-guidelines)
- [Communication](#communication)

## Code of Conduct

By participating in this project, you agree to uphold our community standards of respect, professionalism, and collaboration. We are committed to providing a welcoming and inclusive environment for all contributors.

### Our Standards

- **Be respectful**: Treat all contributors with respect and professionalism
- **Be welcoming**: Welcome new contributors and help them get started
- **Be constructive**: Provide helpful feedback and engage in productive discussions
- **Be honest**: Share accurate information and acknowledge when you're unsure
- **Be responsible**: Take ownership of your contributions and their impact

### Unacceptable Behavior

- Harassment, discrimination, or offensive comments
- Trolling, insulting remarks, or personal attacks
- Publishing others' private information without consent
- Any conduct that could be considered unprofessional

**Enforcement**: Violations may result in temporary or permanent ban from the project. Report issues to ritacsolutions@gmail.com.

## Getting Started

### Prerequisites

Before contributing, ensure you have:

- Git installed on your system
- A modern web browser
- Basic understanding of HTML, CSS, and JavaScript
- A GitHub account
- A LeakCheck.io API key (for testing)

### Fork and Clone

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/leak-checker-app.git
   cd leak-checker-app
   ```
3. **Add upstream remote**:
   ```bash
   git remote add upstream https://github.com/ritacsolutionsllc/leak-checker-app.git
   ```

## How to Contribute

### Reporting Bugs

Found a bug? Help us fix it!

**Before submitting a bug report:**

- Check if the bug has already been reported in Issues
- Verify the bug exists in the latest version
- Test in multiple browsers if possible

**How to submit a good bug report:**

1. Use the GitHub issue tracker
2. Use a clear, descriptive title
3. Include steps to reproduce
4. Provide screenshots if applicable
5. Include browser version and OS
6. Include console error messages

**Bug Report Template:**

```markdown
**Description**
A clear description of the bug.

**Steps to Reproduce**
1. Go to '...'
2. Click on '...'
3. Enter '...'
4. See error

**Expected Behavior**
What should happen.

**Actual Behavior**
What actually happens.

**Environment**
- Browser: [e.g., Chrome 120]
- OS: [e.g., Windows 11]
```

### Suggesting Enhancements

Have ideas for improvements? We'd love to hear them!

**How to suggest an enhancement:**

1. Open a GitHub issue with label `enhancement`
2. Use a clear, descriptive title
3. Explain the problem your enhancement solves
4. Describe your proposed solution
5. Provide examples or mockups if possible

### Submitting Pull Requests

Ready to contribute code? Follow these steps:

#### 1. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

**Branch Naming Convention:**

- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring
- `style/` - UI/CSS changes

#### 2. Make Your Changes

- Write clean, readable code
- Follow the Code Style guidelines
- Test your changes thoroughly
- Update documentation if needed

#### 3. Commit Your Changes

```bash
git add .
git commit -m "feat: add new feature"
```

**Commit Message Format:**

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Code style
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Tests

#### 4. Sync with Upstream

```bash
git fetch upstream
git rebase upstream/main
```

#### 5. Push to Your Fork

```bash
git push origin feature/your-feature-name
```

#### 6. Create Pull Request

1. Go to your fork on GitHub
2. Click "Compare & pull request"
3. Fill out the PR template with:
   - Clear description of changes
   - Related issue number
   - Screenshots for UI changes
   - Testing performed
4. Wait for review and address feedback

## Development Guidelines

### Code Style

#### JavaScript

```javascript
// Use descriptive variable names
const searchResults = [];

// Use camelCase
function performSearch(query, queryType) {
    // code
}

// Use const/let
const API_KEY = 'key';
let resultCount = 0;

// Handle errors
try {
    await performSearch(query);
} catch (error) {
    console.error('Error:', error.message);
}
```

#### HTML/CSS

```html
<!-- Use semantic HTML -->
<section class="search-container">
    <form id="searchForm">
        <input type="text" placeholder="Search">
        <button type="submit">Submit</button>
    </form>
</section>
```

### Testing

Before submitting a PR:

- [ ] Test with valid inputs
- [ ] Test with invalid inputs
- [ ] Test different query types
- [ ] Test API error scenarios
- [ ] Test in Chrome, Firefox, Edge
- [ ] Check responsive design
- [ ] Verify no console errors

## Communication

### Response Times

- Bug reports: 3-5 business days
- Feature requests: 5-7 business days
- Pull requests: 3-5 business days
- Security issues: 24-48 hours

## Recognition

Contributors will be:
- Listed in the Contributors section
- Mentioned in release notes
- Credited in GitHub profile

---

**Thank you for contributing!** 🛡️
