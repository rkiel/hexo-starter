#### Create a space to work in

```bash
mkdir ~/hexo-cli-tool
cd ~/hexo-cli-tool
```

#### Create an initial, starter `package.json`.

```bash
yarn init -y
```

#### Install Hexo command-line

```bash
yarn add hexo-cli
```

#### Add scripts to `package.json`

```bash
vim package.json
```

Add the following contents:

```json
"scripts": {
  "generate": "hexo init"
}
```

#### Create a new blog

```bash
yarn run generate ~/blog
```

#### Reset the node modules with `yarn`

```bash
cd ~/blog
rm -rf node_modules
yarn install
```

#### Add scripts to `package.json`

```bash
vim package.json
```

Add the following contents:

```json
  "scripts": {
    "draft": "hexo new draft",
    "generate": "rm -rf public && hexo generate",
    "list": "hexo list post && echo && hexo list tag && echo && hexo list category && echo && hexo list page",
    "publish": "hexo publish",
    "start": "hexo server --draft"
  }
```

#### Customize

```bash
vim _config.yml
```

Update the `title` and `author` fields.

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
yarn run publish "My First Article"
```

#### Add the article to source control

```bash
git add source
git commit -m "New article"
```

####  Prepare blog for hosting

```bash
yarn run generate
```
