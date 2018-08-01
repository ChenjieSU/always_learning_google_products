
# material_design/01-code_labs/README.md

# References

- Material Design - Web Codelabs: https://material.io/collections/developer-tutorials/#web
- Using webpack: https://webpack.js.org/

# Directories

- Web 101 -> mdc_101-web-material_basics
  - https://codelabs.developers.google.com/codelabs/mdc-101-web/#0

# Steps and Comments

## mdc_101-web-material_basics

### Step 1

- Goal: Text field, Button, and Ripple

### Step 2

```
mkdir github
cd github/
git clone https://github.com/material-components/material-components-web-codelabs
cd material-components-web-codelabs/mdc-101/starter
sudo npm install
cat webpack.config.js
sudo npm start
cat index.html
```

Access in browser: http://localhost:8080/

### Step 3

```
sudo npm install @material/textfield
#### npm install material-components-web   # to install all web components
vi index.html
vi app.scss
vi app.js
vi index.html
sudo npm start
```

Access in browser: http://localhost:8080/

### Step 4

```
sudo npm install @material/button
vi index.html
vi app.scss
vi app.js
sudo npm start
```

Access in browser: http://localhost:8080/

### Step 5

```
cd ../complete/
sudo npm start
cd ..
diff starter/index.html complete/index.html
diff starter/app.scss complete/app.scss
diff starter/app.js complete/app.js
```

