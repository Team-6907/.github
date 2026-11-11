# Contributing

## Workflow

1. Open or pick an issue.
2. Branch from `main` as `<issue#>-short-description`.
3. Open a pull request, link the issue, and ask a software lead for review.
4. Merge after approval. The branch is deleted on merge.

Event work happens on `event_<name>`. After the event the tip is tagged `event_<name>_final` and merged back into `main`.

## Code

- Robot code builds with `./gradlew build` and runs in simulation before review.
- Java is formatted with `./gradlew spotlessApply`.
- Commit summaries are short and imperative: `fix: clamp turret angle before sending setpoint`.
- Upstream copyright headers stay as written.
- Secrets live in environment variables. CAD models, videos and model weights go in Release assets.

Questions go to a software lead or [contact@team6907.org](mailto:contact@team6907.org).
