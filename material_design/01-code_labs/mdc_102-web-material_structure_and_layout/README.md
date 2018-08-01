
# material_design/01-code_labs/mdc_102-web-material_structure_and_layout/README.md

## References

Web 102

- https://codelabs.developers.google.com/codelabs/mdc-102-web/

## Steps and Comments

### Step 1

- Goal: navigation drawer, image list full of products

### Step 2

Starting fresh, instead of picking up the old code.

```
cd 01-code_labs/github/material-components-web-codelabs/mdc-102/starter
sudo npm install
sudo npm start
```

Access in browser: http://localhost:8080/

### Step 3

```
sudo npm install @material/drawer @material/list
vi home.html
sudo npm start   ## Hmm, get an error
```

Upgrade node from 10.1.0 to 10.8.0:

As root:

```
node -v               # 10.1.0
npm cache clean -f
npm install -g n
n stable
node -v               # 10.8.0
```

Try again:

```
sudo npm start   # Rats, still get an error
cd ../complete
sudo npm start   # No error, hmmm....
```

Try cloning and starting fresh:

```
mv github github-old ; mkdir github
cd github
l
git clone https://github.com/material-components/material-components-web-codelabs
cd material-components-web-codelabs/mdc-102/starter/
sudo npm install
```

That is worse!  Running `npm install in both `starter` and `complete` gives multiple `npm ERR! asyncWrite is not a function` errors.

Try downgrading to the LTS version at https://nodejs.org/en:

```
n 8.11.3
sudo npm install  # no errors
sudo npm start    # no errors
sudo npm install @material/drawer @material/list
cp  ../../../../github-old/material-components-web-codelabs/mdc-102/starter/home.html .
cp  ../../../../github-old/material-components-web-codelabs/mdc-102/starter/app.scss .
sudo npm start
```

Access in browser: http://localhost:8080/

- Runs OK now we have the LTS version of node!


```
```

Access in browser: http://localhost:8080/

### Step 4

```
```

Access in browser: http://localhost:8080/

### Step 5

```
```

