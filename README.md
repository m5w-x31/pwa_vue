# pwa_vue

## setup

```
$ docker-compose run --rm node sh -c "npm install -g @vue/cli @vue/cli-init && vue create pwa_vue && chown -R node:node /app"

---
(Vue CLI Setup)
> Manually select features
> Babel, Progressive Web App (PWA) Support, Linter / Formatter
> 3.x
> ESLint with error prevention only
> Lint on save
> In package.json
> Use NPM
---

$ docker-compose up -d
```

## build (PWA: docs)

- ref. https://qiita.com/paragaki/items/4b4e1171f2265ad807bc

```
[vue.config.js]
---
module.exports = {
  publicPath: './',
  outputDir: '../docs'
}
```

```
$ docker exec pwa_vue sh -c "cd pwa_vue && npm run build"
```
