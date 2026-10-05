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
- **Control (A):** The momemt of Misery: "I open StreamLine wanting to relax and watch something, but there are so many options that I spend a long time browsing, comparing and second-guessing instead of actually watching."

What the unchanged experience produces:
Qualitative (M2): I open the app, scroll for like twenty minutes." Despite access to thousands of titles, the user experiences choice overload, repetitive recommendations, ineffective discovery, and ultimately abandons the session without viewing anything. This creates the perception that the service is a "warehouse" of content rather than a trusted guide to great content.
Quantitative (M3): Only 11% of visitors reach a 30+ minute session, down from 19% six months ago. The top of the funnel is holding; the problem is depth of engagement.
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

Screen 2: Feature Core
Spotlight Title Details


Goal

Help the user make a final decision and start playback.

User Story

As an overwhelmed entertainment seeker, I want enough information about a Spotlight recommendation so that I can decide whether it is worth watching.

UI Components
Hero Artwork
Title Information
Title
Content type
Runtime
Existing metadata
Synopsis
Primary CTA
▶ Watch Now

Secondary CTA
+ Add to List


(optional if already available on platform)

User Actions
Start watching
Return to Spotlight rail
Success Criteria

User starts playback.

Screen 3: Success / Confirmation
Playback Started

Instead of creating a new confirmation page, reuse the existing player experience.

Goal

Confirm successful selection.

User Story

As an overwhelmed entertainment seeker, I want to start watching immediately after making a choice so that I feel I made progress rather than continuing to browse.

UI Components
Existing Video Player
Optional Lightweight Confirmation

Displayed for 2-3 seconds:

Now Playing from Spotlight
Great choice.

User Actions
Continue watching
Exit player
Success Criteria

Playback starts successfully.



Variant: Screen 1: Entry Point
Homepage Spotlight Rail
Goal

Get overwhelmed users to stop browsing and consider a much smaller set of options.

User Story

As an overwhelmed entertainment seeker, I want to see a trusted shortlist when I open StreamLine so that I can start choosing immediately.

UI Components
Spotlight Header
SPOTLIGHT
Not sure what to watch? Start here.

Spotlight Rail

10 curated titles

Each card contains:

Artwork
Title
Movie / Series
Existing metadata
CTA

Click title

Success Criteria

User notices Spotlight within a few seconds of entering the app.

Screen 2: Feature Core
Spotlight Title Details
Goal

Help the user make a final decision and start playback.

User Story

As an overwhelmed entertainment seeker, I want enough information about a Spotlight recommendation so that I can decide whether it is worth watching.

UI Components
Hero Artwork
Title Information
Title
Content type
Runtime
Existing metadata
Synopsis
Primary CTA
▶ Watch Now

Secondary CTA
+ Add to List


(optional if already available on platform)

User Actions
Start watching
Return to Spotlight rail
Success Criteria

User starts playback.

Screen 3: Success / Confirmation
Playback Started

Instead of creating a new confirmation page, reuse the existing player experience.

Goal

Confirm successful selection.

User Story

As an overwhelmed entertainment seeker, I want to start watching immediately after making a choice so that I feel I made progress rather than continuing to browse.

UI Components
Existing Video Player
Optional Lightweight Confirmation

Displayed for 2-3 seconds:

Now Playing from Spotlight
Great choice.

User Actions
Continue watching
Exit player
Success Criteria

Playback starts successfully.



Held constant: Screen 1: Entry Point
Homepage Spotlight Rail
Goal

Get overwhelmed users to stop browsing and consider a much smaller set of options.

User Story

As an overwhelmed entertainment seeker, I want to see a trusted shortlist when I open StreamLine so that I can start choosing immediately.

UI Components
Spotlight Header
SPOTLIGHT
Not sure what to watch? Start here.

Spotlight Rail



Each card contains:

Artwork
Title
Movie / Series
Existing metadata
CTA

Click title

Success Criteria

User notices Spotlight within a few seconds of entering the app.

Screen 2: Feature Core
Spotlight Title Details
Goal

Help the user make a final decision and start playback.

User Story

As an overwhelmed entertainment seeker, I want enough information about a Spotlight recommendation so that I can decide whether it is worth watching.

UI Components
Hero Artwork
Title Information
Title
Content type
Runtime
Existing metadata
Synopsis
Primary CTA
▶ Watch Now

Secondary CTA
+ Add to List


(optional if already available on platform)

User Actions
Start watching
Return to Spotlight rail
Success Criteria

User starts playback.

Screen 3: Success / Confirmation
Playback Started

Instead of creating a new confirmation page, reuse the existing player experience.

Goal

Confirm successful selection.

User Story

As an overwhelmed entertainment seeker, I want to start watching immediately after making a choice so that I feel I made progress rather than continuing to browse.

UI Components
Existing Video Player
Optional Lightweight Confirmation

Displayed for 2-3 seconds:

Now Playing from Spotlight
Great choice.

User Actions
Continue watching
Exit player
Success Criteria

Playback starts successfully.




Pressure-test it:
1. Is the variant exactly ONE change, or does it bundle several? Flag anything that breaks attribution.
2. Does the primary metric actually measure whether the persona's moment of misery is resolved?
3. Is the primary metric distinct from the guardrail, or am I conflating them?
4. Given the baseline and MDE, is the sample size and duration realistic, or will this never reach significance?
5. Are my shipping criteria a real decision rule a stakeholder could hold me to? Rewrite anything vague.
- **Held constant (isolation check):** _(not filled in)_

## Hypothesis
> I believe that Spotlight curated rail for The Overwhelmed entertainment seeker will result in Faster time to play, as measured by a 5 change in Median same-session time-to-play within 14 calendar days. We will protect Early abandonment rate: percentage of successful playback starts where the selected title accumulates fewer than five minutes of active viewing before the user exits, excluding technical playback failures. throughout the test.

## Shipping criteria
> We will **ship** if Median same-session time-to-play improves by ≥ 5 at p<0.05 and Early abandonment rate: percentage of successful playback starts where the selected title accumulates fewer than five minutes of active viewing before the user exits, excluding technical playback failures. does not reach Cannot increase more than 1% after 14 calendar days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 calendar days, no results reviewed before this date.
