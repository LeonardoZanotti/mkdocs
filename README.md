# MkDocs
How to create your website with markdown files and MkDocs.

## Installing MkDocs
In Debian and Ubuntu linux you can just use apt to get the package:
```bash
$ sudo apt install mkdocs
$ mkdocs --version		# show mkdocs version and successful installation
```

Or use pip:
```bash
$ pip install mkdocs
$ mkdocs --version
```

## Creating a project
To create a new mkdocs project, just use:
```bash
$ mkdocs new project-name
$ cd project-name
```

It will create a "project-name" folder, and inside this folder will have a docs folder and a mkdocs.yml configuration file.
```bash
|--docs
|----index.md
|--mkdocs.yml
```
Inside docs, put your markdown files, which will be the site pages.

In mkdocs.yml its possible to configure all the site, the basic configuration looks like:
```bash
site_name: <your-site-name>
nav:                            # navigation menu
  - Home: index.md              # home markdown file
  - Page2: page2.md             # other page markdown file
                                # create a page for each .md file
theme: readthedocs              # you can configure a theme for your website here
```

## Running
Now, lets test the site running, type `mkdocs serve` in your terminal and see your website in `localhost:8000`.

## Building
To put your site in production, do:
```bash
$ mkdocs build
```
It will create a /site folder, and inside it we have:
```bash
$ ls site
css  deploy  fonts  img  index.html
js  mkdocs  search.html  sitemap.xml
```

Now, just deploy your project and your website will run :D.

# LeonardoZanotti