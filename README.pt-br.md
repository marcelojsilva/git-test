# Guia rápido de Git
Lista de comandos para consulta rápida

*Read this in [English](README.md)*

## Índice
- [Configuração inicial](#config-init)
- [Listar configurações atuais](#config-list)
- [Iniciar um repositório local](#init)
- [Adicionar alterações](#add)
- [Dar commit das alterações](#commit)
- [Novo repositório remoto](#new-remote)
- [Adicionando repositório remoto](#add-remote)
- [Enviar para o repositório remoto](#send-remote)
- [Criar uma branch e mudar para ela](#branch)
- [Voltar para a Master](#back-master)
- [Criar uma segunda branch, efetuar alterações e efetuar merge com a master](#second-brach)
- [Visualizar branchs](#view-branchs)
- [Status do repositório](#status)
- [Histórico de commits com estatística](#stat)
- [Lista repositórios remotos](#list-remote)
- [Efetuando merge do repositório remoto com o repositório local](#merge-remote)

## Github

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
git add *
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
