#### Initial setup

```bash
yarn init -y
```

### Install Hexo command-line

```bash
yarn add hexo-cli
```

#### Add scripts to `package.json`

```json
"scripts": {
  "hexo": "hexo"
}
```

#### Create a new blog

```bash
yarn run hexo init blog
```

#### Move the new blog

```bash
mv blog ..
```

#### Reset the node modules

```bash
cd ../blog
rm -rf node_modules
yarn install
```

#### Add scripts to `package.json`

```json
  "scripts": {
    "draft": "hexo new draft",
    "publish": "hexo publish",
    "start": "hexo server --draft"
  }
```

#### Put the blog under source control

```bash
git init
git add .
git commit -m "Initial commit"
```

#### Draft an article

```bash
yarn run draft "My First Article"
```

#### Run the server

```bash
yarn start
```

#### View the article

[http://localhost:4000](http://localhost:4000)

#### Publish the article

```bash
yarn run publish My-First-Article
```

#### Add the article to source control

```bash
git add source
git commit -m "New article"
```
