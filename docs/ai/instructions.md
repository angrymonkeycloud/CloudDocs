
# Angry Monkey Cloud AI Instructions

Managed baseline conventions for AI-assisted work across Angry Monkey projects.

> This page defines the default Angry Monkey Cloud instructions and extends them with documentation and SEO practices for this repository.

## How to Use These Instructions

When using an AI assistant to generate, modify, or review code in this repository, provide the AI with the repository guidance first.

Use the following prompt before starting AI-assisted work:

```text
Follow the Angry Monkey Cloud AI instructions for this repository:

https://github.com/angrymonkeycloud/CloudDocs/blob/main/docs/ai/instructions.md

Use these instructions when generating, modifying, or reviewing code. Apply them as the baseline for C# style, static assets, documentation, SEO, and project precedence rules.
```

If this repository has its own project-specific AI instructions, those instructions take precedence when they conflict with the general Angry Monkey Cloud guidance.

## C# Style

- Prefer explicit types over `var`. Use `var` only when the type is obvious from the right-hand side, the type name is long/generic, or usage is idiomatic and well known, such as Entity Framework Core queries.
- Target the latest C# language features when they improve clarity:
  - Primary constructors.
  - Expression-bodied members for single-expression methods, properties, and constructors.
  - Null-conditional assignment using `?.`.
  - Collection expressions (`[]`, `[.. other]`) where applicable.
  - Pattern matching enhancements (`is` patterns, switch expressions, relational and logical patterns).
  - Target-typed `new()` when the declared type is already explicit on the left-hand side.
- Omit braces for single-statement `if`, `else`, `for`, `foreach`, and `while` bodies. Add braces when the body contains more than one statement.
- Favor readability and consistency with the surrounding file over cleverness.
- Name enums in plural form (for example: `ProjectSDKs`, `OrderStatuses`).

## Static Assets (CSS, JS, Images)

- Never author `.css` files directly. Author `.less` files instead.
- Source static assets (`.less`, `.js`/`.ts`, images) must live under `src/` in a subfolder matching their type (for example: `src/css`, `src/js`, `src/images`).
- Razor isolated styles (`Component.razor` + `Component.razor.less`) compile to a co-located `Component.razor.css` file. Never hand-author the isolated `.razor.css`.
- Generic `.less` files compile into `wwwroot/css`.
- If a source `.less` file does not exist yet, create it under `src/css` first, then compile to `wwwroot/css`.
- Follow the CSS naming convention in [../standards/css-naming-convention.md](../standards/css-naming-convention.md).

## Documentation Authoring Standards

- Write in clear, direct, professional language.
- Use one primary topic per page.
- Keep page names stable once published.
- Add and maintain index pages for each top-level domain.
- Prefer descriptive headings using common search phrases.
- Include examples where implementation can be misinterpreted.

## SEO Requirements for Documentation

- Every page must include a clear H1 that matches user search intent.
- Include a short introductory paragraph that naturally contains target keywords.
- Use meaningful section headings (H2/H3), not generic labels.
- Cross-link related pages to improve discoverability and crawl depth.
- Avoid duplicate pages with overlapping intent.

## Precedence

These are default conventions, applied as a baseline for every project managed by Angry Monkey Cloud. If a project defines its own AI agent instructions (for example in `.github/copilot-instructions.md` or `.github/instructions/`), project-specific instructions take precedence when conflicts exist.
