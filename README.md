# nickbean01.github.io
Experimental Static Site

## How to Thumbnail

https://data-dive.com/pelican-colorbox-images

## Fix Broken Themes

https://github.com/getpelican/pelican-themes/issues/482#issuecomment-346653264

> 1. git clone https://github.com/getpelican/pelican-plugins.git pelican-plugins
> 
> 2. adding in `pelicanconf.py`
> 
> ```
> PLUGIN_PATHS = ['/path/to/git/pelican-plugins', ]
> PLUGINS = ['i18n_subsites', ]
> JINJA_ENVIRONMENT = {
>     'extensions': ['jinja2.ext.i18n'],
> }
> ```

## Publish Changes

```
pelican content -o output -s publishconf.py
ghp-import -m "Generate Pelican site" --no-jekyll -b master output
git push origin master
```
