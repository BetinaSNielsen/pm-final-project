# A/B Experiment Brief, StreamLine (B2C)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Spotlight curated rail |
| Persona | The Overwhelmed entertainment seeker |
| Expected outcome | Faster time to play |
| Primary success metric | Median same-session time-to-play |
| Baseline rate | 30 min |
| Guardrail metric | Early abandonment rate: percentage of successful playback starts where the selected title accumulates fewer than five minutes of active viewing before the user exits, excluding technical playback failures. |
| Guardrail boundary | Cannot increase more than 1% |
| Second guardrail | % of exposed users who start playback during the same session. |
| Minimum Detectable Effect | 5 |
| Sample size per arm | 733 |
| Traffic split | 50/50 |
| Test duration | 14 calendar days |
| Significance threshold | p<0.05 |

## Control vs. Variant
- **Control (A):** The momemt of Misery: I open StreamLine wanting to relax and watch something, but there are so many options that I spend a long time browsing, comparing and second-guessing instead of actually watching.

Current StreamLine homepage experience - no Spotlight rail.
- **Variant (B):** Goal

Get overwhelmed users to stop browsing and consider a much smaller set of options.

User Story

As an overwhelmed entertainment seeker, I want to see a trusted shortlist when I open StreamLine so that I can start choosing immediately.

UI Components
Spotlight Header
SPOTLIGHT
Not sure what to watch? Start here.

Spotlight Rail

3-5 curated titles

Each card contains:

Artwork
Title
Movie / Series
Existing metadata
CTA

Click title

Success Criteria

Median Time-to-Play improves by at least 5 minutes (30 → 25 min).
p < 0.05.
Playback Start Rate is not lower than control.
Early Abandonment increases by no more than 1 percentage point.
Sample size target is reached.
Data quality checks pass.
- **Held constant (isolation check):** _(not filled in)_

## Hypothesis
> I believe that Spotlight curated rail for The Overwhelmed entertainment seeker will result in Faster time to play, as measured by a 5 change in Median same-session time-to-play within 14 calendar days. We will protect Early abandonment rate: percentage of successful playback starts where the selected title accumulates fewer than five minutes of active viewing before the user exits, excluding technical playback failures. throughout the test.

## Shipping criteria
> We will **ship** if Median same-session time-to-play improves by ≥ 5 at p<0.05 and Early abandonment rate: percentage of successful playback starts where the selected title accumulates fewer than five minutes of active viewing before the user exits, excluding technical playback failures. does not reach Cannot increase more than 1% after 14 calendar days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 calendar days, no results reviewed before this date.
