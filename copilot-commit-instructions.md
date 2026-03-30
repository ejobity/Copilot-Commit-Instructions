# Commit Message Rules

- **Format**:
  Generate commit messages following this exact structure:
  1. Header: `<gitmoji> <type>[<scope>]: <subject>`
  2. (Blank Line)
  3. Body: `<detailed-description>`

- **Types**:
  Use lowercase types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, or `revert`.

- **Type Selection (Required)**:
  - Choose the commit type from the actual purpose of the change.
  - Do not default to `feat`.
  - Use `feat` only when the main purpose is a new feature or capability.
  - Use `fix` when the main purpose is correcting broken behavior, a bug, a regression, or an error.
  - If a commit contains multiple kinds of changes, choose the type that matches the primary reason the change exists.
  - Supporting work should not change the type. Example: tests added for a bug fix should still use `fix`.

- **Commit Type Decision Order**:
  1. If the commit reverts a previous commit, use `revert`.
  2. If the main goal is fixing broken behavior, use `fix`.
  3. If the main goal is adding a new capability, use `feat`.
  4. If the main goal is restructuring code without intended behavior change, use `refactor`.
  5. If the main goal is improving speed or efficiency, use `perf`.
  6. If the main goal is adding or updating automated tests, use `test`.
  7. If the main goal is documentation only, use `docs`.
  8. If the main goal is formatting or presentation only, use `style`.
  9. If the main goal is tooling, maintenance, or housekeeping, use `chore`.
  10. If the main goal is build output, packaging, or bundling, use `build`.
  11. If the main goal is CI workflow or pipeline changes, use `ci`.

- **Gitmoji Map**:
  - `feat` -> `✨`
  - `fix` -> `🐛`
  - `docs` -> `📝`
  - `style` -> `🎨`
  - `refactor` -> `♻️`
  - `perf` -> `⚡`
  - `test` -> `✅`
  - `build` -> `📦`
  - `ci` -> `👷`
  - `chore` -> `🧹`
  - `revert` -> `⏪`

- **Common Classification Examples**:
  - Broken UI, wrong totals, failed validation, missing state update, regression, crash -> `🐛 fix`
  - New toggle, new page section, new workflow, new endpoint -> `✨ feat`
  - Internal cleanup without intended behavior change -> `♻️ refactor`
  - Test-only changes -> `✅ test`
  - Docs or guidance updates -> `📝 docs`
  - Formatting, spacing, alignment, or CSS-only polish -> `🎨 style`
  - Maintenance work, config cleanup, dependency chores -> `🧹 chore`
  - CI workflow updates -> `👷 ci`
  - Build or packaging changes -> `📦 build`

- **Mood & Tense**:
  Use the imperative, present tense (for example, `add` instead of `added` or `adds`).

- **Subject Line (Header)**:
  - Start with the Gitmoji that matches the chosen type.
  - Keep the total subject line under 50 characters.
  - Do not end the subject with a period.
  - Do not mention specific file names.
  - Focus on the outcome, not implementation details.

- **Body (Detailed Description)**:
  - Separate from the subject with a blank line.
  - Explain the **WHY** and **CONTEXT** rather than only the how.
  - Use the following logical flow:
    1. **Action Summary**: What was changed.
    2. **Context/Rationale**: Why was this change necessary?
    3. **Solution Details**: How does this solve the problem?
    4. **Impact**: How does this affect the rest of the system?
  - Use bullet points (`*`) for lists.
  - If behavior changed, prefer explaining before/after behavior in the body.
  - **Breaking Changes**: Explicitly state `BREAKING CHANGE:` followed by a migration hint if applicable.

- **Exclusions**:
  - Never include the file path or file name in the subject line.
  - Avoid generic words like `updated` or `fixed` without specific context.
  - Never use `✨ feat` for a bug fix.
  - Never choose the Gitmoji first and force the type to match it. Choose the type first, then apply the mapped Gitmoji.
