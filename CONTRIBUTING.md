[//]: # ( ---------------------------------------------------------------------- )
[//]: # (+ Authors: 	Ran# <ran.hash@proton.me> )
[//]: # (+ Created: 	2026/05/05 10:11:02.891629 )
[//]: # (+ Revised: 	2026/05/05 17:24:04.969283 )
[//]: # ( ---------------------------------------------------------------------- )

# Contributing

Thank you for your interest in contributing.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Submitting Changes](#submitting-changes)
- [Commit Style](#commit-style)
- [License](#license)

---

## Code of Conduct

Be respectful and constructive. Harassment, discrimination, or bad-faith behaviour will not be tolerated.

---

## Reporting Bugs

Open an issue and include:

- A clear, descriptive title
- Steps to reproduce the problem
- Expected vs actual behaviour
- Environment details (OS, version, etc.) if relevant

---

## Suggesting Features

Open an issue and describe:

- The problem you are trying to solve
- Your proposed solution
- Any alternatives you considered

---

## Submitting Changes

1. Fork the repository
2. Create a branch from `main`: `git checkout -b my-change`
3. Make your changes
4. Commit following the [commit style](#commit-style) below
5. Push your branch and open a pull request against `main`
6. Describe what you changed and why in the PR body

Keep each pull request focused on a single concern. Unrelated changes belong in separate PRs.

---

## Commit Style

Use a bracketed abbreviation as the title and a Conventional Commits body:

```
[A] short description of what was added

feat: add X
fix: correct Y
```

Allowed brackets:

| Bracket | Type       |
|---------|------------|
| `[A]`   | `feat`     |
| `[R]`   | `refactor` |
| `[F]`   | `fix`      |
| `[D]`   | `docs`     |
| `[T]`   | `test`     |
| `[C]`   | `chore`    |
| `[P]`   | `perf`     |
| `[B]`   | `build`    |
| `[S]`   | `style`    |

Rules:

- Title: bracket + short phrase — do not repeat the type word
- Body lines: lowercase, imperative mood
- Breaking changes: `feat!`/`fix!` in the body, or a `BREAKING CHANGE:` footer
- Scope is optional: `fix(module): ...`

---

## License

By contributing, you agree that your work will be released under the same license as this project — the [PayBack License (PBL)](LICENSE).

Free for personal and non-commercial use. Commercial use requires a revenue-share agreement — contact [ran.hash@proton.me](mailto:ran.hash@proton.me).

Contributing does not transfer copyright or ownership. Non-trivial contributions — new features, bug fixes, and substantive code or documentation changes — may entitle you to a revenue share, subject to a quorum vote among existing owners, once you are listed in the [CONTRIBUTORS](CONTRIBUTORS) file.
