# 4: Repositório Remoto (Push, Pull, Fetch, Clone, Reflog e Cherry-pick)

## git remote

```
git remote add origin <remote link>
git remote // lista os repositórios remotos
git remote show origin // mostra detalhes do repositório remoto 'origin'
```

## git push

```
git push origin master // envia para o repositório 'origin' a branch 'master
git push origin --all // envia todas as branches locais para a 'origin'
git push origin --all -u // flag -u salva o comando de push, no caso de exemplo: sempre que fazer o 'git push' vai fazer 'git push origin --all'
```

## git push —force

```
git reset HEAD~1 --hard // volta 1 commit
git push // vai dar erro porque esta enviando uma branch que está atrás da branch origin
git push --force // não vai deixar caso a branch master esteja protegida na configuração do seu repositório remoto
git push -f //mesmo que git push --force
```

## git reflog

```
git reflog // mostra o histórico do que aconteceu no repositório até os commits que foram resetados
```

## git cherry-pick

```
git cherry-pick <hash-commit> // pega um commit, usado em conjunto com o reflog
```

## git pull

```
/*
    Quando se trabalha em equipe deve se fazer sempre o git pull antes de fazer um push
*/
git pull // Faz o download do repositório remoto e faz o merge no local.
```

## git fetch

```
git fetch // Faz o download do repositório remoto mas não faz merge com o local, precisa fazer o merge depois.
git checkout origin/master // vai para a branch do remoto para ver o que veio da origin
git checkout master // voltar para a master para fazer o merge
git merge origin/master //  faz o merge do que veio da origin com a master local

```

## git clone

```
git clone // Faz o clone do repositório remoto para a maquina local.
```
