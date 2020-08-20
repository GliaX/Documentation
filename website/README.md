This website was created with [Docusaurus](https://docusaurus.io/).<br>
For help on using Github see [here](https://guides.github.com/activities/hello-world/); specifically, look at making commits and pull requests.

# What's In This Document

* [Get Started in 5 Minutes](#get-started-in-5-minutes)
* [Directory Structure](#directory-structure)
* [Editing Content](#editing-content)
* [Adding Content](#adding-content)
* [Full Documentation](#full-documentation)

# Get Started in 5 Minutes

1. Make sure all the dependencies for the website are installed:

```sh
# Install dependencies
$ yarn
```
2. Run your dev server:

```sh
# Start the site
$ yarn start
```
*Downloading Node/Yarn for Docusaurus installation is only necessary when making big changes to the docusaurus website (e.g. creating categories). 
Editing content can be done through GitHub.*


## Directory Structure

The project file structure should look something like this

```
Documentation/
  docs/
    assets/       (<-- where pictures are stored)
    category/     (<-- tabs)
       doc-1.md   (<-- pages)
       doc-2.md
       doc-3.md
  website/
    core/
    node_modules/
    pages/
    static/
      css/
      img/
    package.json
    sidebar.json
    siteConfig.js
```
*When editing content for the docusaurus using Github, only the `docs/ files`, and website/ `sidebar.json` and `siteConfig.js` are used.* <br><br>

# Editing Content

## Editing an existing docs page

Edit docs by navigating to `docs/` and editing the corresponding document:

`docs/category/doc-to-be-edited.md`

```markdown
---
id: page-needs-edit     (<-- the id will be how this page gets referred to in other files)
title: This Doc Needs To Be Edited    (<-- the title appears in the sidebar and as the title of each page)
---

Content of the page appears below the header. For easy formatting, these files use markdown.
```

For help on using markdown, see the [Guide to Markdown](https://guides.github.com/features/mastering-markdown/). <br>
You can use the _preview changes_ tab when editing pages to see your changes before committing them. 

For more information about docs, click [here](https://docusaurus.io/docs/en/navigation)

## Editing an existing blog post

Edit blog posts by navigating to `website/blog` and editing the corresponding post:

`website/blog/post-to-be-edited.md`
```markdown
---
id: post-needs-edit
title: This Blog Post Needs To Be Edited
---

Edit me...
```

For more information about blog posts, click [here](https://docusaurus.io/docs/en/adding-blog)<br><br>

# Adding Content

## Adding a new docs page to an existing sidebar

1. Create the doc as a new markdown file in `/docs/category`, example `docs/category/newly-created-doc.md`:

```md
---
id: newly-created-doc
title: This Doc Needs To Be Edited
---

My new content here..
```

1. Refer to that doc's ID in an existing sidebar in `website/sidebar.json`:

```javascript
// Add newly-created-doc to the Getting Started category of docs
{
  "docs": {
    "Getting Started": [
      "category/quick-start",
      "category/newly-created-doc"   // new doc here
    ],
    ...
  },
  ...
}
```
By adding your .md (markdown) file to the sidebar you are allowing users to find the page; otherwise, the page will have been created but there isn't a way to access it. <br>
For more information about adding new docs, click [here](https://docusaurus.io/docs/en/navigation)

## Adding Pictures

1. Upload the picture to the docs/assets/media folder. 

1. Add the picture to a page by adding `![alt title](assets/media/pic-name.jpg)`
```md
---
id: existing-doc
title: This Doc Needs a Pic
---

![alt title](assets/media/pic-name.jpg)
Content with picture above
```

## Adding a new blog post

1. Make sure there is a header link to your blog in `website/siteConfig.js`:

`website/siteConfig.js`
```javascript
headerLinks: [
    ...
    { blog: true, label: 'Blog' },
    ...
]
```

2. Create the blog post with the format `YYYY-MM-DD-My-Blog-Post-Title.md` in `website/blog`:

`website/blog/2018-05-21-New-Blog-Post.md`

```markdown
---
author: Frank Li
authorURL: https://twitter.com/foobarbaz
authorFBID: 503283835
title: New Blog Post
---

Lorem Ipsum...
```

For more information about blog posts, click [here](https://docusaurus.io/docs/en/adding-blog)

## Adding items to your site's top navigation bar

1. Add links to docs, custom pages or external links by editing the headerLinks field of `website/siteConfig.js`:

`website/siteConfig.js`
```javascript
{
  headerLinks: [
    ...
    /* you can add docs */
    { doc: 'my-examples', label: 'Examples' },
    /* you can add custom pages */
    { page: 'help', label: 'Help' },
    /* you can add external links */
    { href: 'https://github.com/facebook/Docusaurus', label: 'GitHub' },
    ...
  ],
  ...
}
```

For more information about the navigation bar, click [here](https://docusaurus.io/docs/en/navigation)

## Adding custom pages

1. Docusaurus uses React components to build pages. The components are saved as .js files in `website/pages/en`:
1. If you want your page to show up in your navigation header, you will need to update `website/siteConfig.js` to add to the `headerLinks` element:

`website/siteConfig.js`
```javascript
{
  headerLinks: [
    ...
    { page: 'my-new-custom-page', label: 'My New Custom Page' },
    ...
  ],
  ...
}
```

For more information about custom pages, click [here](https://docusaurus.io/docs/en/custom-pages).

# Full Documentation

Full documentation can be found on the [docusaurus website](https://docusaurus.io/).
