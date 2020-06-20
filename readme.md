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

Adicionando repositório remoto
```bash
git remote add mj https://github.com/marcelojsilva/git-test #trocar mj pelo nome do repositório remoto que deseja, quando não informado fica com default 'origin'
```

Lista repositórios remotos
```bash
git remote -v
```

Enviar para o repositório remoto (formato: "git push \<remote-name> \<branch-name>)
```bash
git push mj master
```