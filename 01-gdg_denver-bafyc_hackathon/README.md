# always_learning_google_assistant/01-gdg_denver-bafyc_hackathon

This repo is for learning how to program the Google Assistant.

This directory is about the GDG Denver Build Actions for Your Community (BAFYC) virtual hackathon.

## GDG Denver (BAFYC) Virtual Hackathon

### Bechdel Test

- Docs out of sync, got confused quickly, with the welcome intent
- Need to give this a shot later

### Tom's Trivia - **Deleted 2018-05-17**

- This is looking better than the dialogflow attempt.

### Founding Fathers Trivia

- Cleaned up copy of Tom's trivia with some additional questions and better images.

### Quick Personality Type Quiz

- Single-word mini-description for each type come from http://www.personalityperfect.com/16-personality-types/ .
- Doesn't work very well, but I feel like I'm getting the hang of things

### Founding Fathers Flash Cards - **Deleted 2018-05-07**

- Basing these on info used in the Trivia game
- Trying to invoke this got hosed because it kept hearing 'flashcards' instead of flash cards' and I tried to rename it
  then tried to delete it and that messed up the ability to properly invoke the new project.  Seriously.
  The old one is scheduled for full deletion in a month, on 5/29.
- Cleared up the issue with the two projects but still unable to invoke the app
- Getting "Founding fathers flashcards isn't responding right now. Try again soon."
- Debug tab shows: "agentToAssistantJson": "Service unavailable",
- Log tab shows: "App returned an HTTP error. State: URL_UNREACHABLE"
- Retry from scratch with a new project name: Founding Fathers Facts

Now unable to invoke these two projects, GA confuses flash cards with flashcards (it keeps hearing just the one word).

As mentioned above, getting "Founding fathers flashcards isn't responding right now. Try again soon."

Hopefully, once a month has passed and these two are deleted, they will have fixed the bug(s), and I can run the
**Founding Fathers Facts** app.

#### Deleting Flash Cards GA Projects

Deleted both "flash cards" projects on 2018-05-07:

- "OLD FF Flash Cards FUBARED" - Project ID: founding-fathers-flash-cards, Project number: 31227001949
- "BAD FF Flashcards FUBARED" - Project ID: founding-fathers-flashcards, Project number: 502900007029

To get the project number, use Gear icon on project page -> Permissions -> Google Cloud Platform/IAM & Admin menu -> Gear icon (Settings)

Projects are **"now shut down and scheduled to be deletion after 6/6/18."**
See starred emails to main google account from "Platform Notifications" sent on 2018-05-07.

#### Tips for Deleting GA Projects

**Note:** Unable to delete via the gear icon on the project's page in actions on google (despite having done it that way before).
(Get "Authentication failure.")

**To delete:**
Follow this process (as of 2018-05-07):

1. Access project page: Gear icon on project page -> Project
1. Change the name to make sure name won't be used - e.g., use "OLD" or "BAD" or "FUBARED" in name
1.   and all invocations
1. Gear icon on project page -> Permissions -> (New Page)
1. Google Cloud Platform/IAM & Admin menu -> Gear icon (Settings) -> Shut down

**Note:** As of 2018-05-17 the interface has changed a bit.

**See the "Final Cleanup" section below for current info on deleting projects.**

### Founding Fathers Facts

- Re-using same data created (copied from the trivia game) for Founding Fathers Flash Cards

## Submissions

### Video Links:

- founding_fathers_trivia - https://youtu.be/81rzIDTGAjc
- quick_personality_quiz - https://www.youtube.com/watch?v=vVE4BRQ9_zk

## Final Cleanup - Deleted These Projects on 2018-05-17:

Moving on to try the tutorial examples at Google code labs.  For details, see the directory ../02-google_code_lab .

### Tom's Silly Name - NOT mentioned above

- Project ID: bafyc-tom-s-silly-name
- Project number: 764283451047
- No invocations
- Gear icon -> Project Settings: Changed name to "OLD Tom's Silly Name DELETED"
- Gear icon -> Project Settings: This now has a DELETE PROJECT button ...
  - ... but it doesn't work, get the following error:
  - "This project cannot be deleted because it is connected to a Dialogflow agent. Please delete the agent in Dialogflow first."
  - This is probably due to the fact that I did not use templates for this one
  - It is unclear how to delete the agent ...
- Gear icon -> Permissions -> New page, showing the top option, "IAM"
  - IAM - probably Identity and Access Management
  - List shows a "Dialogflow API Client" - not an "agent," but possibly what they are talking about - with a trash can icon
  - Other options: Service accounts - has an option to delete the Dialogflow Integrations
- Trying Gear icon -> Permissions -> Top option on new page: "IAM"
  - Deleting the entry for which Role = "Dialogflow API Client"
- Back to actions on google -> Gear icon -> Project settings -> DELETE PROJECT button ...
  - ... still get the same error:
  - "This project cannot be deleted because it is connected to a Dialogflow agent. Please delete the agent in Dialogflow first."
- Trying Gear icon -> Permissions -> Settings option -> SHUT DOWN (top of page)
  - This is what we did before
  - Now get this in a popup: "Project Service The project has a lien against it.  Tracking number: 2412696064732306085"
  - Looking at solution here: https://stackoverflow.com/questions/47337549/google-cloud-platform-not-allowing-project-shut-down-due-to-lien?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa
  - Log into console.dialogflow.com - Log on using google account (tomwhartung@gmail.com)
  - Gear icon -> opens to "General" tab
  - At the bottom: "Danger Zone," "Delete Agent," "DELETE THIS AGENT" button -> clicking it now.
  - Deleted agent from my list, which can be seen by clicking on the agent name -> View all agents
- Back to Actions console -> Gear Icon -> Project settings -> DELETE PROJECT
  - Still getting this error:
    "This project cannot be deleted because it is connected to a Dialogflow agent. Please delete the agent in Dialogflow first.
  - Yikes, maybe I should not have deleted the entry for which Role = "Dialogflow API Client" (above)??
- Trying Actions console -> Gear icon -> Gear icon Services -> SHUT DOWN
  - Did not work, same error as before
  - Sent some feedback to google
  - **Leaving this for now.**


### Tom's Trivia - mentioned above

- No invocations
- Gear icon -> Project Settings: Changed name to

