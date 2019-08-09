
# Create markdown based presentation
---
## How to create markdown based presentations
- We will create a markdown based presentation
- We will write the prsentation in markdown
- Use some data to analyse
- Write some text
- Produce slides from there
---

## Start with a github repository
- Create a github repository (say 'foo')
- Add a git submodule to the github repo
- `git init` # initialise a git repository locally
- `git submodule add <foo URL>`
- `cd foo` 
- this will create a directory 'foo' in the current directory
---

## Download the remarkjs.min.js 
- `wget <remarkjs.min.js URL>` javascript file
- you will need to source this file in the html
---
## Prepare a separate html file and store with these settings
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title</title>
    <meta charset="utf-8">
    <style>
      @import url(https://fonts.googleapis.com/css?family=Yanone+Kaffeesatz);
      @import url(https://fonts.googleapis.com/css?family=Droid+Serif:400,700,400italic);
      @import url(https://fonts.googleapis.com/css?family=Ubuntu+Mono:400,700,400italic);

      body { font-family: 'Droid Serif'; }
      h1, h2, h3 {
        font-family: 'Yanone Kaffeesatz';
        font-weight: normal;
      }
      .remark-code, .remark-inline-code { font-family: 'Ubuntu Mono'; }
    </style>
  </head>
  <body>
    <textarea id="source">

class: center, middle



    </textarea>
    <script src="https://remarkjs.com/downloads/remark-latest.min.js">
    </script>
    <script>
      var slideshow = remark.create({
        source: 'markdown.md'
         }
        );
    </script>
  </body>
</html>
```

---
## Now prepare the markdown.md
- Use jupyter nbconvert to convert the ipynb file to markdown
- `jupyter nbconvert --to markdown filename.ipynb`
- This will convert the ipynb to markdown
---
## Use git to upload the files to your repository

```bash
    git checkout -b gh-pages
    git add .
    git commit -m "your message goes here"
    git push origin gh-pages
```
---

## If everything goes alright

[Site published at https://username.github.io/foo/filename.html](https://username.github.io/foo/filename.html)

