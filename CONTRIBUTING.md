# Contributing to CP-Sentinel

We welcome contributions to CP-Sentinel! To ensure the project remains clean, consistent, and easy to navigate, we adhere to the following Git conventions. Please take a moment to review them before you begin.

## Core Principle: Atomic Commits

Every commit should be **atomic**—it must represent a single, complete, and indivisible logical change.

- **Do one thing:** A commit should fix one bug, add one feature, or refactor one specific piece of code.
- **Don't mix concerns:** Do not mix bug fixes with feature development or style changes in the same commit.
- **Keep it self-contained:** The project should be in a consistent, working state after every commit.

This practice keeps the project history clean, simplifies code reviews, and makes it easier to identify the source of bugs.

## Branch Naming Convention

Branch names should be descriptive and follow a consistent format to clearly indicate their purpose.

**Format:** `<type>/<short-description>`

- **`<type>`:** The category of work being done.
  - `feature`: For developing a new feature.
  - `fix`: For fixing a bug.
  - `chore`: For maintenance, dependency updates, or other routine tasks.
  - `docs`: For changes to documentation.
  - `refactor`: For code refactoring that doesn't change external behavior.
- **`<short-description>`:** A few words in `kebab-case` describing the change.

**Examples:**
- `feature/user-authentication`
- `fix/login-form-validation`
- `chore/update-react-version`

## Commit Message Format

We follow the **Conventional Commits** specification for our commit messages. This creates a clear and explicit history that is easy for both humans and automation tools to read.

**Format:**
```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

- **`<type>`:** Must be one of the following:
  - `feat`: A new feature.
  - `fix`: A bug fix.
  - `chore`: Routine tasks, build process changes.
  - `docs`: Documentation changes.
  - `style`: Code style changes (e.g., formatting).
  - `refactor`: Code changes that neither fix a bug nor add a feature.
  - `test`: Adding or correcting tests.
- **`<scope>` (optional):** The part of the codebase the commit affects (e.g., `api`, `frontend`, `db`).
- **`<subject>`:** A concise, imperative-mood description of the change (e.g., "Add login endpoint" not "Added...").
- **`<body>` (optional):** A more detailed explanation of the "why" and "how" of the change.
- **`<footer>` (optional):** Used for referencing issue numbers (e.g., `Closes: #42`).

**Example:**
```
feat(api): Add user authentication endpoint

Implement JWT-based authentication for the /api/login route.
The endpoint validates user credentials and returns a signed token.

Closes: #123
```

## Pull Request (PR) Process

When you are ready to merge your changes, please open a Pull Request.

- **Use the PR Template:** Your PR description will be pre-filled with a template. Please fill it out completely to provide context for reviewers.
- **Clear Title:** Write a clear and descriptive title that follows the commit message format.
- **Link Issues:** If your PR resolves an existing issue, be sure to link it in the description (e.g., `Closes #123`).
