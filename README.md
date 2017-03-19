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

#### Put the blog under source control

```bash
git init
git add .
git commit -m "Initial commit"
```
