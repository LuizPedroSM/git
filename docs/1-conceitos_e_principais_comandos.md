# 1 - Conceitos e Principais Comandos

### git config

```
git config --global user.name "your name"
git config --global user.email "your email"
```

### git version

```
git --version
```

### git help

```
git help
```

### git init

```
git init
```

### git status

```
git status
```

### git add

```
git add <filename> // adiciona o arquivo especifico
git add -i // adiciona de forma interativa
git add . // adiciona todos os arquivos
```

### git commit

```
git commit -m "Your commit message"
git commit // abre o editor padrão para inserir a mensagem de commit
```

### git commit --amend

```
git commit  -m "Your commit message" --amend // 'Remenda' o commit
```

### git reset

```
// Volta quantos commits quiser HEAD~(numero de commits que deseja voltar)
git reset HEAD~1 --soft  // Volta os commits com os arquivos modificados
git reset HEAD~1 --hard  // Volta os commits sem os arquivos modificados
```

### .gitignore

```
nome e diretórios de arquivos que não deseja ser monitorado
/node_modules // exemplo a pasta de dependências do node
```

### git diff

```
git diff // olha a diferença dos arquivos modificados
```

### git log

```
git log
git log --oneline // retorna o log de forma resumida
```

### git checkout

```
git checkout <filename> // descarta as alterações no arquivo
git checkout . // descarta tudo que fez
git checkout <hash commit> // vai para aquele commit
```

### git tag

```
git tag // rotula o commit, usado para criar versões
git tag v1.0.0 // adiciona a tag v1.0.0
git checkout v1.0.0 // volta para a versão v1.0.0
```

### git show

```
git show <hash commit> // mostra detalhes daquele commit
```

### git rm

```
git rm <filename> // confirma a exclusão do arquivo

git rm --cached <file> // remove o arquivo da area de stage
```
