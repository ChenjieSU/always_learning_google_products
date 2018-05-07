# always_learning_ga

This repo is for learning how to program the Google Assistant.

## GDG Denver Virtual Hackathon

### Bechdel Test

- Docs out of sync, got confused quickly, with the welcome intent.

### Tom's Trivia

- This is looking better than the dialogflow attempt.

### Founding Fathers Trivia

- Cleaned up copy of Tom's trivia with some additional questions and better images.

### Quick Personality Type Quiz

- Single-word mini-description for each type come from http://www.personalityperfect.com/16-personality-types/ .
- Doesn't work very well, but I feel like I'm getting the hang of things

### Founding Fathers Flash Cards

- Basing these on info used in the Trivia game
- Trying to invoke this got hosed because it kept hearing 'flashcards' instead of flash cards' and I tried to rename it
  then tried to delete it and that messed up the ability to properly invoke the new project.  Seriously.
  The old one is scheduled for full deletion in a month, on 5/29.
- Cleared up the issue with the two projects but still unable to invoke the app
- Getting "Founding fathers flashcards isn't responding right now. Try again soon."
- Debug tab shows: "agentToAssistantJson": "Service unavailable",
- Log tab shows: "App returned an HTTP error. State: URL_UNREACHABLE"
- Retry from scratch with a new project name: Founding Fathers Factoids

Deleted both flash cards projects on 2018-05-07:

- Project ID: founding-fathers-flash-cards, Project number: 
- "BAD FF Flashcards FUBARED" - Project ID: founding-fathers-flashcards, Project number: 502900007029

Projects are "now shut down and scheduled to be deletion after 6/6/18."
See emails to main google account sent on 2018-05-07.

#### Tips for Deleting GA Projects

**Note:** Unable to delete via the gear icon on the project's page in actions on google (despite having done it that way before).
(Get "Authentication failure.")

**To delete:**
Follow this process (as of 2018-05-07):

1. Access project page, make sure name won't be used (e.g., use "OLD" or "BAD" or "FUBARED" in name,  and all invocations)
2. Gear icon on project page -> Permissions -> (New Page)
3. Google Cloud Platform/IAM & Admin menu -> Gear icon (Settings) -> Shut down

### Founding Fathers Facts

- Re-using same data created (copied from the trivia game) for Founding Fathers Flash Cards

## Submissions

### Video Links:

- founding_fathers_trivia - https://youtu.be/81rzIDTGAjc
- quick_personality_quiz - https://www.youtube.com/watch?v=vVE4BRQ9_zk

