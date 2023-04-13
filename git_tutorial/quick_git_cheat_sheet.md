## Guia rápido

### Clonando e criando `branch`

1. Crie uma pasta para deixar depositórios:
```bash
$ mkdir ~/dev
```
2. Clone o repositório
```bash
$ git clone git@github.com:onimaru/project_douchi.git
```
3. Entre na pasta
```bash
$ cd project_douchi
```
4. Crie uma `branch` para trabalhar
```bash
$ git checkout -b <nome-da-branch>
```
Agora você pode modificar o código como quiser sem interferir no código principal. Você pode trocar de `branch` sem se preocupar em perder o código modificado nela, ao voltar para uma `branch` o código que você modificou continuará lá.

## Fazendo `commit` e `push`
1. Ver que arquivos foram modificados
```bash
$ git status
```
2. Adicione os arquivos que deseja "commitar"
```bash
$ git add <arquivo-1> <arquivo-2>
```
3. Faça o `commit` com uma mensagem
```bash
$ git commit -m 'minha mensagem de commit'
```
4. Faça o `push` para disponibilizar o código para todos
```bash
$ git push origin <nome-da-branch>
```

## Acessando uma `branch` existente para trabalhar

1. Verifique o nome das `branches` remotas
```bash
$ git branch -r
```
2. Muda para a `branch` escolhida
```bash
$ git checkout <nome-da-branch>
```
Obs: se estiver usando o `jupyter` com o código da `main` aberto, este automaticamente será trocado pelo código da `branch` escolhida.

## Atualizando `branches`
1. Vá para a `main`
```bash
$ git checkout main
```
2. Faça um pull
```bash
$ git pull
```