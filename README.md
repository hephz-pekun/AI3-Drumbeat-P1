# AI3-Drumbeat-P1
Contribution [#1]: [UI: add a svg icon for the crash cymbal]
Contribution Number: [1]
Student: Iyanuoluwa Hephzibah Olanipekun
Issue: [https://github.com/Babali42/DrumBeatRepo/issues/511]
Status: [Phase II] [In Progress]

Why I Chose This Issue
[This issue interests me because it is a mix of creativity and coding. I love that it matches my skills as it requires yet puts me out of my comfort zone as it's not in python language. It is on an easier level so I will focus more on learning the proper procedure of Open-source contribution]

Understanding the Issue
Problem Description
[The programs has different genre of beats. The Rock Variation Pattern contains a crash cymbal sound that is correctly configured using MIDI note 49. However, when displayed in the user interface, no corresponding SVG icon is shown for the crash cymbal. The UI therefore displays a missing or default icon instead of a proper crash cymbal image.]

Expected Behavior
[It is expected that a crash cymbal SVG icon should appear in the UI whenever MIDI note 49 is used in the Rock Variation Pattern.]

Current Behavior
[Currently, the crash cymbal sound works correctly, but the UI does not display a dedicated icon because no SVG asset is mapped to the crash cymbal instrument.]

Affected Components
[These parts of the codebase are involved?
src/assets/beats/rock/variation.json,
src/app/ui/pipes/drum-image.pipe.spec.ts,
SVG asset directory containing drum instrument icons, and
Drum image mapping logic used by the UI]

Reproduction Process
Environment Setup
[There was no challenge in setting up your local development environment. However, I was challenged in knowing exactly files tto change, since they was a lot of files in codebase. This was solved when the instructor (Daniel) gave shorthands to type in url to filter through. Kind of like 'Ctrl + F']

### Steps to Reproduce
Steps to Reproduce
[Step 1 - Run the application locally.
Step 2 - Open the Rock Variation Pattern.
Step 3 - Locate the note using MIDI value 49.
Step 4 - Observe that no crash cymbal icon is rendered.
Step 5 - Compare with other drum instruments that do display.]
[Observed result]
Reproduction Evidence
Commit showing reproduction: [https://github.com/hephz-pekun/AI3-Drumbeat-P1/commits/main/README.md]
Screenshots/logs: [If applicable]
My findings: [I discovered that the issue is not related to MIDI configuration. After reviewing the issue description, MIDI note 49 is already configured correctly. The root cause appears to be that the frontend UI lacks a dedicated SVG image for the crash cymbal, or the icon is not mapped correctly within the drum image pipe. The provided issue specifically points to adding a crash cymbal SVG from the SVG Repo drum assets and updating the image mapping/tests.]
Solution Approach
Analysis
[Your analysis of the root cause is that The UI relies on SVG assets and instrument-to-image mappings. While MIDI note 49 is recognized correctly, the crash cymbal has no associated SVG icon available to the frontend, causing a fallback or missing-image state. cd4]

Proposed Solution
[Here's my proposed solution:
Locate the existing drum SVG assets.
Download or create an appropriate crash cymbal SVG icon.
Add the SVG to the project's asset directory.
Update the drum image mapping so MIDI note 49 resolves to the new crash cymbal icon.
Update the relevant test in:
src/app/ui/pipes/drum-image.pipe.spec.ts
Verify the icon appears correctly in the Rock Variation Pattern UI.]

Implementation Plan
Using UMPIRE framework (adapted):

Understand: [The crash cymbal (MIDI note 49) functions correctly but lacks a corresponding SVG icon in the UI, resulting in a missing instrument image.]

Match: [Other drum instruments already have SVG assets and mapping logic. The crash cymbal should follow the same pattern as the existing drum icons]

Plan: [Step-by-step implementation plan] 
1. [Find where drum SVG assets are stored.]
2. [Add a crash cymbal SVG asset.]
3. [Update drum-image mapping logic.]
4. [Update/add unit tests for MIDI note 49.]
5. [Run tests and manually verify the UI.]

Implement: [https://github.com/hephz-pekun/AI3-Drumbeat-P1/commits/main/README.md]

Review: [Self-review checklist - does it follow the project's contribution guidelines?]

Evaluate: [I will verify by checking that:
Crash cymbal icon displays correctly.
Existing tests continue to pass.
New crash cymbal test passes.
Rock Variation Pattern shows the correct instrument image.]

Testing Strategy
Unit Tests
[ ] Test case 1: [Description]
[ ] Test case 2: [Description]
[ ] Test case 3: [Description]
Integration Tests
[ ] Integration scenario 1
[ ] Integration scenario 2
Manual Testing
[What you tested manually and results]

Implementation Notes
Week [O] Progress
[Nothinging built, just selected the preferred issue to contribute to]

Week [Y] Progress
[Continue documenting as you work]

Code Changes
Files modified: [None yet]
Key commits: [Links to important commits]
Approach decisions: [Why you chose certain approaches]
Pull Request
PR Link: [GitHub PR URL when submitted]

PR Description: [Draft or final PR description - much of the content above can be adapted]

Maintainer Feedback: - [Date]: [Summary of feedback received] - [Date]: [How you addressed it]

Status: [Awaiting review / Iterating / Approved / Merged]

Learnings & Reflections
Technical Skills Gained
[What you learned technically]

Challenges Overcome
[What was hard and how you solved it]

What I'd Do Differently Next Time
[Reflection on your process]

Resources Used
[Link to helpful documentation]
[Tutorial or Stack Overflow post that helped]
[GitHub issues or discussions that helped]
