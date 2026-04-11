# Setup - Git, GitHub e clonagem

## Resumo rápido
Se você quer baixar um projeto do GitHub sem usar `Download ZIP`, o caminho correto é usar **Git** com `git clone`.

Isso faz com que você baixe:
- os arquivos
- o histórico do projeto
- branches e referência ao repositório remoto

---

## 1) Configuração inicial do Git
Comandos comuns:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git config --global init.defaultBranch main
```

### O que cada parte faz

#### `git config`
Abre ou altera configurações do Git.

#### `--global`
Aplica a configuração ao seu usuário no computador inteiro.

Sem `--global`, a configuração vale só para o repositório atual.

#### `user.name`
Define o nome que aparece nos commits.

#### `user.email`
Define o email associado aos commits.

#### `init.defaultBranch main`
Faz novos repositórios começarem com branch `main` por padrão.

---

## 2) Como clonar do GitHub sem baixar ZIP

### Exemplo
```bash
git clone https://github.com/usuario/repositorio.git
```

### O que cada parte faz

#### `git clone`
Baixa uma cópia completa do repositório remoto.

#### `https://github.com/usuario/repositorio.git`
É a URL do repositório.

- `https://github.com/` = servidor GitHub
- `usuario` = dono do repositório
- `repositorio.git` = nome do projeto em formato Git

---

## 3) Depois da clonagem
```bash
cd repositorio
```

### O que isso faz
- `cd` entra na pasta do projeto
- a partir daí você roda os comandos dentro do repositório

---

## 4) Verificar se o remoto ficou configurado
```bash
git remote -v
```

### O que isso faz
Mostra qual repositório remoto está ligado ao seu projeto local.

---

## 5) Baixar atualizações depois
```bash
git pull
```

### O que isso faz
Baixa e integra mudanças do repositório remoto para sua cópia local.

---

## 6) Enviar suas mudanças
```bash
git add .
git commit -m "Minha alteração"
git push origin main
```

### O que cada parte faz

#### `git add .`
Prepara arquivos alterados para entrar no próximo commit.

#### `git commit -m "Minha alteração"`
Cria um ponto no histórico com uma mensagem explicando a mudança.

#### `git push origin main`
Envia os commits locais para o remoto `origin`, na branch `main`.

---

## 7) Diferença entre baixar ZIP e usar clone

### `Download ZIP`
- baixa só os arquivos
- não baixa o histórico Git
- não liga sua pasta ao repositório remoto

### `git clone`
- baixa os arquivos
- baixa o histórico
- conecta sua pasta ao repositório remoto
- permite usar `pull`, `push`, `commit`, `branch`

---

## 8) HTTPS vs SSH

### HTTPS
Mais simples para começar.

Exemplo:
```bash
git clone https://github.com/usuario/repositorio.git
```

### SSH
Bom para uso frequente, mas exige chave SSH configurada.

Exemplo:
```bash
git clone git@github.com:usuario/repositorio.git
```

---

## 9) Sequência mínima para começar
1. instalar Git
2. configurar `user.name` e `user.email`
3. copiar a URL do repositório no GitHub
4. rodar `git clone`
5. entrar na pasta com `cd`
6. editar os arquivos
7. usar `add`, `commit` e `push`
