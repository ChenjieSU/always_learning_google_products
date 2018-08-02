
# material_design/01-code_labs/mdc_112-web-material_mdc_with_web_frameworks/README.md

## References

Web 112

- https://codelabs.developers.google.com/codelabs/mdc-112-web/

## Steps and Comments

### Step 1

- Goal: Build a React Component, which uses MDC Web as a foundation
  - Build a custom Adapter to use the Foundation logic to achieve a Material Design React Component

#### Foundation, Adapter, Component

- Every package in MDC Web comes with a Component, Foundation, and Adapter
- Foundation: the business logic implementing Material Design
  - Foundation has an Adapter
- Adapter: an interface, implemented and used to interact with the DOM structure
- Component: implements the Adapter and provides proxy methods for the Foundation
  - Component has a Foundation

Note:

> The principles learned in this codelab can be applied to any **JavaScript** framework.

In this case, we are using React.

### Step 2

```
sudo npm install
sudo npm start
more App.js
cat TopAppBar.js
```

Access in browser: http://localhost:8080/

- Runs ok but pretty ugly

### Step 3

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

