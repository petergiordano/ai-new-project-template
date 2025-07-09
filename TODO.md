# TODO.md

## Jules Recommendations 
feat: Enhance user onboarding in Claude commands

Implemented two recommendations to improve user onboarding:

1. Visual Progress Checklist in /start-coding:
   - Added a checklist to the output of `/start-coding.md` when a new project needs its foundation documents.
   - This checklist visually outlines the 5 (+1 optional) phases of project initialization (Roadmap, VibeTesting, etc.), helping users understand the scope of this initial multi-step interview process.

2. State Explanations in /orient:
   - Added brief, parenthetical explanations to each status message in `/orient.md`.
   - These explanations clarify the file-based logic and evidence (e.g., presence/absence of specific files or directories) used by the script to determine the current project stage.
   - This makes the system's state detection more transparent to the user.

These changes aim to make the initial user experience smoother and the system's behavior more understandable.