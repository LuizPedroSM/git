# Padronização de commits (gitmoji, commitlint, e commitizen)

## gitmoji

```sh
npm i -g gitmoji-cli
```

```sh
gitmoji -l |less # mostra a lista de emoji
gitmoji -c # inicia a cli de commit interativo do gitmoji
gitmoji -i # inicia o gitmoji como um commit hook
```

[gitmoji-github](https://github.com/carloscuesta/gitmoji)

## commitlint

```sh
# For Windows:
npm install --save-dev @commitlint/config-conventional @commitlint/cli

# Configure commitlint to use conventional config
echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

To lint commits before they are created you can use Husky's `commit-msg` hook:

```sh
# Install Husky v6
npm install husky --save-dev
# or
yarn add husky --dev

# Activate hooks
npx husky install
# or
yarn husky install

# Add hook
npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```

[commitlint-github](https://github.com/conventional-changelog/commitlint)

## Commitizen

```sh
npm install -g commitizen
```

```json
"scripts":{
  "commit":"cz"
}
```

```sh
npm run commit # roda o script "commit", que inicia a cli do commitizen
git cz # inicia a cli de commit do commitizen
```

### husky

```sh
npm install husky
```

```json
"husky": {
  "hooks": {
    "prepare-commit-msg": "exec < /dev/tty && git cz --hook || true"
  }
}
```

```sh
git commit # vai iniciar a cli de commit do commitizen devido ao hook do husky
```

[commitizen-github](https://github.com/commitizen/cz-cli)
