## Comandos Git

Configuração inicial (somente a primeira vez)
```bash
git config --global user.name "MJ"
git config --global user.email "marcelojosedasilva@gmail.com"
```

Listar configurações atuais
```bash
git config --list
```

Iniciar um repositório local
```bash
git init
```

Status do repositorio
```bash
git status
```

Adicionar alterações
```bash
git add *
```

Dar commit das alterações
```bash
git commit -m "Descrever comentário"
```

Histórico de commits com estatístca
```bash
git log --stat -2
```

Adicionando repositório remoto (Criar primeiro o repositório remoto, neste exemplo o git-test)
```bash
git remote add mj https://github.com/marcelojsilva/git-test #trocar mj pelo nome do repositório remoto que deseja, quando não informado fica com default 'origin'
```

Lista repositórios remotos
```bash
git remote -v
```

Efetuando merge do repositório remoto com o repositório local (para resolver erro "fatal: refusing to merge unrelated histories")
```bash
git pull mj master --allow-unrelated-histories
#Após este comando será aberto o editor default para justificar o merge
```

Enviar para o repositório remoto (formato: git push \<remote-name> \<branch-name>)
```bash
git push mj master
```

Criar uma branch e mudar para ela
```bash
git checkout -b development
```

Voltar para a Master
```bash
git checkout master
```

Criar uma segunda branch, efetuar alterações e efetuar merge com a master
```bash
git checkout -b hotfix
#efetuar alterações
git checkout master
git merge hotfix
git branch -d hotfix
```
