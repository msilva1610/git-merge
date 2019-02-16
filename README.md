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

## Git tag

Incluindo Tag para ajudar no controle de versão do arquivo

Verificar os commits realizados no git 
```
ubuntu@ubuntu-Inspiron-5458:~/devopstemp$ git log --pretty=oneline
438b61063145ed44801511ad7ba10f5a63210796 (HEAD -> master, conflito/master) Acertando readme
9337fe6a5b44ad3f65de0dded9dd8f97154c7ae1 Conflito resolvido
530791292c5c816f36812e79b0b54d1c45064067 Incluindo linha remota de conflito
11d0eedd62fe491ee911d0b36abfcc9260bea08b Update teste.txt
0268b1fc90c7356befed327291fee1b7e9367e83 Merge branch 'master' of https://github.com/msilva1610/git-merge
52310b9bdbd0d7d5ed5ec16119cb98103eee38f5 inicio
c6f3737fb59d3553fefa6c00f25fbd03bea36fd2 Delete teste.txt
9cdd321473beb31e12e949c1eb0355f46dea700e Delete .gitignore
c7f1e4ac650619d99266256dd260d73a1e4731d1 Conflito resolvido
2220c22d05801eeb65722598ad3c9287470630d3 Linha do conflito adicionada
1302d8fc62dec655dd448ce31efd484a724faa8d Linha do github
b3785897b5fe8e5654a5b69add8350755043e40a Merge branch 'master' of https://github.com/msilva1610/git-merge
c83bea8fa393d77da31c45cb41815196c82d8ead Delete teste.txt
387018819739bb3f59f9a512f8f90724753abb51 Delete .gitignore
296c9d84b456985b0f4a30a857cab683e618afa1 inicio
f32d8cc2e8ab5323bdf4eac4918af06829589b51 Update README.md
c51b6fb00cd137e6791c0ea22cb33374d6de66e5 Merge branch 'master' of https://github.com/msilva1610/git-merge
270168235632de5f4b6781dace035a1430491be1 inicio remoto
ef968733f1383c38366bfca8ef7733c0e04c4f19 Delete teste.txt
200106cbeef0d2548270d2df0cbe93f97d7901d4 Delete .gitignore
a409f2bbacbb43370a997a28bcf9553dcee4dfdd Update README.md
1519eb9448e32c660bc099e580ebdf0f20f7c33a Merge branch 'master' of https://github.com/msilva1610/git-merge
b2b0efbbc0b5a8e90f3090235da9eb437a49f8bb Arquivos iniciais origin
```
Pegar os 5 primeiros caracteres da log e usar no comando abaixo 
``` 
git tag -a v0.0 b2b0e 
```

Dar o comando ```git tag``` para ver as modificações

Para subir as modificações, execute

```
git push conflito --tags
```
