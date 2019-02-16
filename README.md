# git-merge
Resolvendo conflitos de arquivos no github


1. Criar um repositório no github e inicializá-lo normalmente

### P1
```
rm -rf .git
git status
git add .
git commit -m "inicio remoto"
git status
git remote add conflito https://github.com/msilva1610/git-merge.git
git remote -v
git pull conflito master --allow-unrelated-histories
git push conflito master
```


### P2
```
git remote add https://github.com/msilva1610/git-merge.git
```


### P3
```
git remote -v
```


### P1
```
git add .
```

