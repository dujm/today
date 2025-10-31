# today


## Setup
### 1. Locally: create a conda environment (named as `today`)
```sh
# create an env
conda create -n today python=3.11 

# activate env
conda activate today

# install packages
pip3 install -r requirements.txt

```

### 2. Locally: create a jupyter book repo (also named as `today`)

```sh
# create a jupyter book
jupyter-book create today

# enter main directory
cd today
```
 * Add markdown files in `docs/` (just to make it more organized)

 * Update `_toc.yml` file according to markdown file names

 * Optional: install a theme 
 ```sh
 pip install pydata-sphinx-theme
 ```

 * Update `_config.yml` 
   * update repository url (`https://github.com/yourname/today`)
   * Add the theme to your _config.yml file:
   ```yml
    sphinx:
        config:
            html_theme: pydata_sphinx_theme
   ```

### 3. Remote: on your Github (`yourname`), create a repo (`today`) 

### 4. Locally: deploy to Github Page (`https://github.com/yourname/today`)
 * Connect to Github 
```bash

# build book 
jupyter-book build --all ./

# push to Github
git init 
git remote add origin git@github.com:yourname/today.git
git add .
git commit -m "initial commit"
git push --set-upstream origin master
```

* Import documents to Github Page 
```bash
# use ghp-import to import documents to Github Page 
ghp-import -n -p -f -o _build/html
``` 

### 5. Remote: configure a publishing source on your Github 
 * Go to `https://github.com/yourname/today/settings/pages`
 * Source: `Deploy from a branch`
 * Branch: `gh-pages/root`
 * Click save 
 * Wait 1-2 min 
 * Go to `yourname.github.io/today`



---

## Ref
 * [Build your book](https://jupyterbook.org/en/stable/start/build.html)
 * [Jupyterbook on Github](https://jupyterbook.org/en/stable/publish/gh-pages.html)
 * [Configuring a publishing source for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
