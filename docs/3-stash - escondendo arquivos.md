# 3 - Stash - Escondendo Arquivos

```
git stash // esconde as modificações feitas "joga para de baixo do tapete" 
git stash -u // faz o stash de arquivos não trackeados
git stash save  'your message' // adiciona uma mensagem ao stash 

git stash list // mostra todos os stash funciona como pilha
git stash show // mostra detalhes do stash que esta no topo da pilha

git stash pop // retorna o primeiro stash da pilha
git stash apply 1 // retorna um stash indicado da pilha mas não remove da pilha

git stash drop 1 // remove da pilha o stash indicado

git stash clear // remove todos os stash da pilha
```