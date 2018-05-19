# always_learning_google_assistant/02-google_code_lab

This subdirectory contains a README.md file, and maybe more, reflecting things learned from the Google Code Labs.

## Resources and Glossary

See `../build_actions-code_lab-level_1/README.md`

Good to know!

## Steps Taken

### 2.2: Install the Firebase command-line interface

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


