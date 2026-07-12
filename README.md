# Quality Rater Audit — A Claude Skill

A Claude skill that audits a webpage or piece of content the way Google's own human search quality raters do — using the actual framework from Google's Search Quality Rater Guidelines (the 182-page "General Guidelines" document, Sept 2025 edition), not a generic E-E-A-T checklist.

## What it does

Given a URL or a piece of content, the skill walks through the full rating process:

- **Classifies page purpose** and splits the page into Main Content, Supplementary Content, and Ads/Monetization
- **Determines YMYL status** (Your Money or Your Life) across Health/Safety, Financial Security, Government/Civics, and other high-stakes categories — and raises the accuracy bar accordingly
- **Assesses Main Content quality**: effort, originality, skill/execution, and factual accuracy against established consensus
- **Runs independent reputation research** via web search — news coverage, reviews, complaints, awards — rather than trusting a site's own "About" page
- **Scores E-E-A-T** (Experience, Expertise, Authoritativeness, Trust), with Trust treated as the anchor and conflicts of interest explicitly flagged
- **Checks for disqualifying red flags**, including the newer spam-abuse patterns Google added in 2024–2025: expired domain abuse, site reputation abuse, and scaled content abuse
- **Assigns an overall Page Quality rating** — Lowest / Low / Medium / High / Highest — with a specific, evidence-based rationale
- **Outputs a structured, downloadable report** with prioritized, concrete recommendations for improving the page

## Why it's useful

Most "E-E-A-T audits" are surface-level — a bulleted checklist with no real methodology behind it. This skill applies Google's actual rater process, including the parts most tools skip: verifying reputation independently instead of taking a site's word for it, and treating factual accuracy on YMYL topics as a hard constraint that reputation can't override. In testing, it correctly caught a factual safety error on a well-reputed university page and held the rating down despite the source's credibility — which is exactly the kind of judgment the real guidelines are designed to produce.

## Use cases

- Pre-publish content review before a page goes live
- Diagnosing why a page underperforms in organic search or AI Overviews despite "good" content
- Competitor benchmarking on E-E-A-T and page quality
- YMYL content review (health, finance, legal, safety) where accuracy stakes are highest

## How to install

1. Download `quality-rater-audit.skill` from this repo
2. In Claude, go to Settings → Capabilities → Skills (requires Pro, Max, Team, or Enterprise with code execution enabled)
3. Upload the file
4. Ask Claude to audit a URL or piece of content against the Search Quality Rater Guidelines

## Disclaimer

This is Claude's own analysis using a framework based on Google's publicly available guidelines. It is not an official Google rating and does not guarantee search or AI-visibility performance.

---

Built with ❤️ by Ilias Galiotos. Happy SEO!
```
