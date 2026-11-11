# Contributing 贡献指南

This is how Team 6907 works on code. It applies to every repository in this
organization that does not ship its own `CONTRIBUTING.md`.

## Before you start 开始之前

- Pick an issue, or open one that describes what you want to change and why.
- If you are not a team member, fork the repository and open a pull request
  from your fork. Small fixes and questions are welcome.

## Branches 分支

- The default branch is `main`. Do not push to it directly; open a pull request.
- Feature branches are named after the issue: `<issue#>-short-description`,
  for example `42-fix-intake-current-limit`.
- Event branches are named `event_<name>`. After the event the tip is tagged
  `event_<name>_final` and the branch is merged back into `main`.
- Branches are deleted once they are merged.

## Pull requests 拉取请求

- One topic per pull request. Keep it small enough to review in one sitting.
- Fill in the pull request template: what changed, why, and how it was tested
  (simulation, real robot, or not tested).
- Link the issue (`Closes #42`).
- Robot code must at least build (`./gradlew build`) and run in simulation.
- Ask a software lead for review, and merge only after approval.

## Commit style 提交信息

- Write a short imperative summary in English, about 72 characters or fewer:
  `fix: clamp turret angle before sending setpoint`.
- Prefixes such as `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `build:`
  and `chore:` are encouraged.
- Explain the reason in the body when it is not obvious from the diff.
- Automatic `Update at '<timestamp>'` commits belong on event branches only.

## Formatting 代码格式

- Java projects use Spotless. Run `./gradlew spotlessApply` before you commit
  and make sure `./gradlew spotlessCheck` passes.
- Keep upstream copyright and license headers (WPILib, AdvantageKit / Team
  6328, Team 254 and others) exactly as they are. Do not configure a Spotless
  `licenseHeader()` step that overwrites them.
- Other languages: use the formatter and linter configured in the repository.

## What does not belong in git 不要提交的内容

- **Credentials.** No passwords, API keys or tokens, ever. Read them from
  environment variables and commit only placeholder files such as
  `.dev.vars.example`. If one slips through, follow [SECURITY.md](SECURITY.md).
- **Large binaries.** CAD exports (`.glb`), videos and model weights go into
  Release assets or a separate assets repository, not into git history.
- Build output, IDE settings and local logs. Check `.gitignore` first.

## Questions 有问题？

Ask a software lead, or write to [contact@team6907.org](mailto:contact@team6907.org).
