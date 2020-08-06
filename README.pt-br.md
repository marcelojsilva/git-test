# Guia rápido de Git
Lista de comandos para consulta rápida

*Read this in [English](README.md)*

## Índice
- [Configuração inicial](#configuração-inicial)
- [Listar configurações atuais](#listar-configurações-atuais)
- [Iniciar um repositório local](#iniciar-um-repositório-local)
- [Adicionar alterações](#adicionar-alterações)
- [Dar commit das alterações](#dar-commit-das-alterações)
- [Novo repositório remoto](#novo-repositório-remoto)
- [Adicionando repositório remoto](#adicionando-repositório-remoto)
- [Enviar para o repositório remoto](#enviar-para-o-repositório-remoto)
- [Criar uma branch e mudar para ela](#criar-uma-branch-e-mudar-para-ela)
- [Voltar para a Master](#voltar-para-a-master)
- [Criar uma segunda branch, efetuar alterações e efetuar merge com a master](#criar-uma-segunda-branch-efetuar-alterações-e-efetuar-merge-com-a-master)
- [Visualizar branchs](#visualizar-branchs)
- [Status do repositório](#status-do-repositório)
- [Histórico de commits com estatística](#histórico-de-commits-com-estatística)
- [Lista repositórios remotos](#Lista-repositórios-remotos)
- [Efetuando merge do repositório remoto com o repositório local](#efetuando-merge-do-repositório-remoto-com-o-repositório-local)

## Github

<!-- toc -->

### Configuração inicial
Configuração inicial (somente a primeira vez)
```bash
git config --global user.name "UserName"
git config --global user.email "your_email@mail.com"
```

### Listar configurações atuais
```bash
git config --list
```

### Iniciar um repositório local
```bash
git init
```

### Adicionar alterações
```bash
git add .
```

### Dar commit das alterações
```bash
git commit -m "Initial commit"
```

### Novo repositório remoto
curl -u 'marcelojsilva' https://api.github.com/user/repos -d '{"name":"[repository-name]"}'

### Adicionando repositório remoto
```bash
git remote add origin https://github.com/[user-git]/[repository-name]
```

### Enviar para o repositório remoto
```bash
git push -u origin master
```

### Criar uma branch e mudar para ela
```bash
git checkout -b development
```

### Voltar para a Master
```bash
git checkout master
```

### Criar uma segunda branch, efetuar alterações e efetuar merge com a master
```bash
git checkout -b hotfix
#efetuar alterações
git checkout master
git merge hotfix
git branch -d hotfix
```
### Visualizar branchs
```bash
git branch -v
```

### Status do repositório
```bash
git status
```

### Histórico de commits com estatística
```bash
git log --stat -2
```

### Lista repositórios remotos
```bash
git remote -v
```

### Efetuando merge do repositório remoto com o repositório local

*Para resolver erro "fatal: refusing to merge unrelated histories"*

```bash
git pull origin master --allow-unrelated-histories -m "Merge text" 
```
