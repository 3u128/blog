[![Netlify Status](https://api.netlify.com/api/v1/badges/f88447a3-1d72-4ae3-8cbd-d0caafd49856/deploy-status)](https://app.netlify.com/sites/3u128/deploys)

#### __Yevhen Lytviak__ personal blog
site: https://arta.pp.ua

theme:
 - fork https://github.com/3u128/hugo-notepadium
   with small changes
deploy:
 - https://netlify.com
requirements:
 - hugo
 - golang
 - markdown knowledge

```
git submodule add https://github.com/3u128/hugo-notepadium themes/hugo-notepadian
```

for updates in theme:

```
git submodule update --remote --recursive
```

run for test site locally:

``` hugo server -D ```
