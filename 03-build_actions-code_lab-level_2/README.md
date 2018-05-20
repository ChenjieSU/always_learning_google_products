# always_learning_google_assistant/02-google_code_lab

This subdirectory contains a README.md file, and maybe more, reflecting things learned from the Google Code Labs.

## Resources and Glossary

- For resources, see `../build_actions-code_lab-level_1/README.md`
- For a glossary, see `../GLOSSARY.md`

Good to know!

## Steps Taken

### 2.2: Install the Firebase command-line interface

#### 2.2.1: Upgrade Npm and Node

Need to upgrade my installations of npm and node:
**Note:** Node.js includes npm, but after installing or upgrading node will probably have to upgrade npm.

```
### ****** Before ******
$ npm -v
3.5.2      ## Current stable version: 6.0.1
$ node -v
v4.2.6     ## Current stable version: 10.1.0 and 8.11.2 (LTS)
$ sudo npm install n -g
.......................
$ sudo n stable
.......................
   installed : v10.0.0
i $ which n
/usr/local/bin/n
$ sudo n stable
$ node -v
v10.0.0
$ sudo n latest
.......................
   installed : v10.1.0
$ sudo npm install -g npm
$
### ****** After ******
$ node -v
v10.1.0
$ npm -v
6.0.1
```

References:

- https://stackoverflow.com/questions/10075990/upgrading-node-js-to-latest-version
- https://stackoverflow.com/questions/6237295/how-can-i-update-node-js-and-npm-to-the-next-versions

#### 2.2.2: Install Firebase CLI Tools

```
$ sudo npm -g install firebase-tools
.......................
$ firebase --version
3.18.4
$ firebase login
.......................
✔  Success! Logged in as tomwhartung@gmail.com
$
```

### 2.3. Set up for Local Development

#### 2.3.1: Download your base files (clone repo)

```
$ git clone https://github.com/actions-on-google/codelabs-nodejs
.......................
$ cd codelabs-nodejs/
$ mv ./level1-complete ./level2      ## For clarity
```

#### 2.3.2: Set up your project and agent (disable inline editor)

- Dialogflow console -> Fulfillment -> Inline Editor -> Disabled

#### 2.3.3: Deploy the fulfillment

Get the project id from:

- Actions console -> Gear icon -> Project Settings

**Project ID** is: `actions-codelab-f5fa4`

Install dependencies and deploy:

```
$ cd 03-build_actions-code_lab-level_2/codelabs-nodejs
$ cd level2/functions/
$ sudo npm install
.......................
$ sudo firebase deploy --project actions-codelab-f5fa4
.......................
✔  Deploy complete!
Project Console: https://console.firebase.google.com/project/actions-codelab-f5fa4/overview
$
```

#### 2.3.4: Retrieve the deployment URL

Dialogflow needs the URL of the cloud function.

URL for the firebase console: https://console.firebase.google.com/

- Firebase console -> actions-codelab
- Develop -> functions
- Dashboard tab -> Event column -> dialogflowFirebaseFulfillment
- URL: https://us-central1-actions-codelab-f5fa4.cloudfunctions.net/dialogflowFirebaseFulfillment

#### 2.3.5: Set the deployment URL in Dialogflow

- Dialogflow console -> Fulfillment
- Webhook: enable
- Paste the URL from 2.3.4
- Save (at bottom of page)

#### 2.3.6: Verify your project is correctly set up

- Dialogflow console -> Integrations -> Google Assistant
- Ensure Auto-preview changes is enabled
- Actions on Google console -> Simulator
- Enter "Talk to my test app" then "fuchsia"

### 2.4: Add a deep link to your Action

### 2.4.1: Add intent for deep linking and implicit invocation

Google uses training phrases, invoking a deep link as appropriate.

- Dialogflow console -> Integrations
- Google assistant -> Integration Settings link (near the bottom of the popup window)
- Discovery -> Implicit Invocations -> Add intent -> "favorite color"

### 2.4.2: Test your deep link

- Actions console -> Simulator
- Enter "Talk to my test app about blue"

### 2.4.3: Define a custom fallback intent

This can handle unexpected utterances, such as "Talk to my test app about bananas."

- Dialogflow console -> Intents -> Create Intent button (at top)
- Name: 'Unrecognized Deep Link'
  - Note: this name is case-sensitive
- Under Contexts, Add **input** context: "google_assistant_welcome"
  - Under Contexts, Add **output** context: Click on the "X" to remove the auto-populated "google_assistant_welcome"
- Under Training phrases, add "banana", "trumpet", and "booze"
  - Double-click on "banana", "trumpet" and "booze", and assign them to filter "@sys.any"
  - In general, we do not want to use "@sys.any", but we are making an exception this time
- Under Responses, add "Sorry, I am not sure about $any . What's your favorite color?" as a Text response
- Click Save (at top of page)

### 2.4.4: Test your custom fallback intent

- Actions console -> Simulator -> "Talk to my test app about banana"

### 2.5: Personalize your responses with helper intents

#### 2.5.1 Get user information using permission helper intent

- Dialogflow console -> Intents -> Default Welcome Intent
- Under Fulfillment (at the bottom) -> Enable webhook call for this intent
- Save

- Intents -> Create Intent
- Set Name to: "actions_intent_PERMISSION"
- Under Fulfillment (at the bottom) -> Enable webhook call for this intent
- Save

```
$ cd level2/functions   ## if necessary
$ vi index.js           ## update as described in the code lab
```

#### 2.5.2 Customize responses with user information

```
$ cat >> index.js       ## append code as described in the code lab
$ vi index.js           ## update as described in the code lab
$ firebase deploy --project actions-codelab-f5fa4
.......................
✔  functions[dialogflowFirebaseFulfillment]: Successful update operation.
✔  Deploy complete!
Project Console: https://console.firebase.google.com/project/actions-codelab-f5fa4/overview
```

#### 2.5.3 Test your code

- Actions console -> Simulator
- Type "Talk to my test app"
- This didn't work for me, rats
- Reviewed all steps and code, tried again, and it still didn't work for me, hmm

### 2.6: Add audio effects with SSML






