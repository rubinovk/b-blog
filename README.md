# Octopress blog setup: 
[`http://rubinovk.github.io/b-blog`](http://rubinovk.github.io/b-blog)


## Setup

For project and not for personal blog use
Repo: `https://github.com/rubinovk/b-blog.git` 

In the repo and branch: 
`rake setup_github_pages`
use URL: `git@github.com:rubinovk/b-blog.git` 

[Setup gh-pages/subdir](http://octopress.org/docs/deploying/subdir/) 
`rake set_root_dir[/b-blog]`

Change `Rakefile`: 
`document_root  = "~/website.com/b-blog/"`


### Setup custom theme:

$ cd octopress  
$ git clone git://github.com/macjasp/cleanpress.git .themes/cleanpress  

> update `.themes/cleanpress/source/_includes/custom/fancybox_head.html`
Add {{ root_url }} to path

$ rake install['cleanpress']  
$ rake generate  

### Source and custom dirs

Change favicon in `source`.  
Customizations to navigation and menu at `/octopress/source/_includes/custom`

# Important:

Check in `config.yml`  that  `root: /b-blog`:
If publishing to a subdirectory as in `http://rubinovk.github.io/b-blog` 

Check if `screen.css` in `source` has correct font paths.
If not, update `/octopress/sass/base/_font.scss` with `/b-blog/font/` and screen.css will regenerate correctly!
Backup plan to add in `custom` `head.html`:
`<link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">`

# Check git setup

`.git/config` 

## Preview 

When run `rake preview` load site at: [http://localhost:4000/b-blog](http://localhost:4000/b-blog)

# Links

see [http://kvz.io/blog/2012/09/25/blog-with-octopress/](http://kvz.io/blog/2012/09/25/blog-with-octopress/) for setup

see [http://www.moncefbelyamani.com/how-to-install-and-configure-octopress-on-a-mac/](http://www.moncefbelyamani.com/how-to-install-and-configure-octopress-on-a-mac/)
for customizations

[merging blog and site](http://marcgayle.com/2013/09/21/deploying-octopress-blog-to-an-existing-gh-pages-static-site/) 

