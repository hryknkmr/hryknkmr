# Activity Semantic Network

匿名化した最近の GitHub 活動から、一般的な技術スタックと品質シグナルを意味ネットワークとして可視化しています。

- Snapshot: `2026-06-06T16:27:27.683102+00:00`
- Scope: recent pull requests and issues authored by this account
- Owners included: `hryknkmr`, `AxonRelay`
- Keep: `SSOT`, `Playwright`, `a11y`, `WCAG`, `axe`, `GitHub Actions` など一般技術語
- Hide: 組織名、個人名、案件名、製品ベンダー固有名、URL、メール、長いID

## Stack Graph (TF-IDF)

```mermaid
graph LR
    docker["Docker (77.67)"]
    playwright["Playwright (67.75)"]
    npm["npm (54.8)"]
    eslint["ESLint (49.54)"]
    github_actions["GitHub Actions (46.19)"]
    pnpm["pnpm (40.03)"]
    dom["DOM (39.14)"]
    dependabot["Dependabot (28.72)"]
    screen_reader["Screen Reader (16.46)"]
    ssot["SSOT (14.36)"]
    biome["Biome (10.77)"]
    aria["ARIA (7.99)"]
    cron["Cron (4.0)"]
    a11y["a11y (4.0)"]
    npm -->|35.33| pnpm
    eslint -->|24.86| pnpm
    playwright -->|24.64| pnpm
    playwright -->|24.43| npm
    eslint -->|22.45| github_actions
    github_actions -->|22.29| npm
    eslint -->|21.57| npm
    eslint -->|18.48| playwright
    github_actions -->|18.48| pnpm
    dependabot -->|15.4| github_actions
    github_actions -->|15.4| playwright
    ssot -->|14.36| npm
    ssot -->|14.36| pnpm
    eslint -->|14.07| ssot
    docker -->|13.98| npm
    dependabot -->|13.05| npm
    dom -->|12.43| docker
    dependabot -->|10.87| docker
```

## Signal Graph

```mermaid
graph LR
    failure["Failure (4)"]
    audit["Audit (3)"]
    regression["Regression (3)"]
    hardening["Hardening (2)"]
    false_positive["False Positive (1)"]
    bug["Bug (1)"]
    timeout["Timeout (1)"]
    audit -->|1| failure
    audit -->|1| hardening
    audit -->|1| regression
    failure -->|1| false_positive
    failure -->|1| hardening
    failure -->|1| timeout
```

## Theme Graph

```mermaid
graph LR
    documentation["documentation (29)"]
    developer_tooling["developer tooling (27)"]
    product_flows["product flows (22)"]
    ci_cd["ci/cd (13)"]
    selectors_and_dom["selectors and dom (13)"]
    e2e_testing["e2e testing (11)"]
    quality_assurance["quality assurance (8)"]
    accessibility["accessibility (6)"]
    payments_and_subscriptions["payments and subscriptions (6)"]
    source_of_truth_alignment["source-of-truth alignment (2)"]
    developer_tooling -->|25| documentation
    developer_tooling -->|15| product_flows
    documentation -->|15| product_flows
    product_flows -->|12| selectors_and_dom
    ci_cd -->|11| developer_tooling
    ci_cd -->|11| documentation
    ci_cd -->|11| product_flows
    documentation -->|10| e2e_testing
    documentation -->|10| selectors_and_dom
    developer_tooling -->|9| e2e_testing
    developer_tooling -->|9| selectors_and_dom
    e2e_testing -->|8| product_flows
    documentation -->|7| quality_assurance
    e2e_testing -->|7| quality_assurance
    ci_cd -->|6| e2e_testing
    developer_tooling -->|6| quality_assurance
    accessibility -->|4| developer_tooling
    accessibility -->|4| documentation
```
