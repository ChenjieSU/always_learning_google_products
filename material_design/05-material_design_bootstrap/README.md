
# material_design/05-material_design_bootstrap/README.md

I like the look of the new ArtsyVisions.com, and am thinking about using some of these styles on SeeOurMinds.com and Groja.com

Thinking it is a good time to take a look at Material Design for Bootstrap.

## References

- Downloaded from: https://mdbootstrap.com/getting-started/
  - Version: MDB Free 4.5.8
- From the README.txt :
  - Documentation: https://mdbootstrap.com/
  - Getting started: https://mdbootstrap.com/getting-started/
  - Tutorials:
    - MDB-Bootstrap: https://mdbootstrap.com/bootstrap-tutorial/
    - MDB-Wordpress: https://mdbootstrap.com/wordpress-tutorial/
  - Templates: https://mdbootstrap.com/templates/
  - License: https://mdbootstrap.com/license/
  - Support: https://mdbootstrap.com/forums/forum/support/
  - Contact: office@mdbootstrap.com
- Footer docs:
  - https://mdbootstrap.com/components/bootstrap-footer/#basic
- Other links found studying the footer docs:
  - Typography: https://mdbootstrap.com/content/typography/
  - Bootstrap Text Utilities: https://mdbootstrap.com/utilities/bootstrap-text/
  - Bootstrap Forms: https://mdbootstrap.com/components/forms/
  - Bootstrap Inputs: https://mdbootstrap.com/components/inputs/
  - Bootstrap Images: https://mdbootstrap.com/content/bootstrap-images/
  - Bootstrap Embeds: https://mdbootstrap.com/utilities/bootstrap-embeds/
  - Bootstrap Icons: https://mdbootstrap.com/content/icons-list/
  - Bootstrap Position: https://mdbootstrap.com/utilities/bootstrap-position/

## Directories

- `00-downloaded/`
  - Copy of the downloaded code, unchanged
- `01-mdb-quick-start/`
  - MDBoostrap 5 min Quick Start
  - https://mdbootstrap.com/mdb-quick-start/
- `02-landing_page`
  - MDBootstrap Landing Page Tutorial
  - https://mdbootstrap.com/landing-page-lesson-1/

## Details

### `00-downloaded/`

Unzipped downloaded file into `Site` .

### `01-mdb-quick-start/`

Looks worth exploring further.

### `02-landing_page`

#### Lesson 1: Navigation

There are a lot of options available:

- https://mdbootstrap.com/components/navbar/

Tips for optimal background image:

> You can use whatever image you want, but there are a few rules which you should follow.

> Your image should be big enough to keep the quality and as lightweight as possible to not increase a page load time. That's why I recommend you prepare your picture as follows:

> 1. Resolution: 1920px / 1280px
> 2. JPG file format
> 3. Compress the file (you can use COMPRES JPG tool)

#### Lesson 2: Content Part I-A (Mask Content)

- Does not look very good!

#### Lesson 3: Content Part I-B (Mask Content)

- Looks much better!

#### Lesson 4: Content Part II: Best Features

- Not much to comment on

#### Lesson 5: Content Part III: Examples Section

- The mask div needs to be inside the same div as the img tag
- The image needs to be inside an anchor tag to activate the ripple effect when clicking

#### Lesson 6: Content Part IV: Gallery Section

- At this time, I am not planning to use a carousel...

#### Lesson 7: Content Part V-A: Contact Section - Form

- Makes the form look very modernistic

#### Lesson 8: Content Part V-B: Contact Section - Map

- Played around with it a bit to get the lat-long for where I am

#### Lesson 9: Footer

Links to docs from the lesson:

- Footer docs:
  - https://mdbootstrap.com/components/bootstrap-footer/#basic

##### Links Section

- The code in the lesson differs a little bit from the code in the footer docs.

Trying both versions:

- `index-footer_1.html` - version of footer from the lesson
  - contains just one column of links
- `index-footer_2.html` - version of footer from the footer docs link above
  - contains two columns of links

The difference is just the number of columns of links.

- `index.html`
  - Using code from the lesson, and adding code from the footer docs

#### Lesson 9-A: Footer Docs

Getting side-tracked and looking at links to other sections of docs from the footer docs:

- Typography:
  - https://mdbootstrap.com/content/typography/
- Bootstrap Text Utilities:
  - https://mdbootstrap.com/utilities/bootstrap-text/
- Bootstrap Forms:
  - https://mdbootstrap.com/components/forms/
- Bootstrap Inputs:
  - https://mdbootstrap.com/components/inputs/
- Bootstrap Images:
  - https://mdbootstrap.com/content/bootstrap-images/
- Bootstrap Embeds:
  - https://mdbootstrap.com/utilities/bootstrap-embeds/
- Bootstrap Icons:
  - https://mdbootstrap.com/content/icons-list/
- Bootstrap Position:
  - https://mdbootstrap.com/utilities/bootstrap-position/

Adding other code snippets from the lesson to `index.html`:

- Footer text
- Forms and inputs
- Images
- Embeds - skipping for now
- Icons
- Buttons - Pro component
- Social Buttons - Pro component

#### Lesson 10: Navigation - Bells and Whistles

- Some features may not be available in free version

##### Step 1

Replacing the code removes the code for our drop-down menu example.

- This code actually works, taking us to the respective sections
- Drop-down menu example code still exists in `index-footer_1.html` and `index-footer_2.html`

##### Step 2

Implement smooth scrolling:

```
<ul class="navbar-nav mr-auto smooth-scroll">
```

- This doesn't seem to work as hoped, and may be one of the Pro features
  - Or we may just need some javascript...

##### Step 3

Removing code for search form.

- Search form example code still exists in `index-footer_1.html` and `index-footer_2.html`

##### Step 4

Not interested in bells and whistles at this time, so skipping this for now:

> The last improvements we'll add to the Navbar will be transparency and animation.

- I suspect these may be Pro features



