# Setup - Subir plugin do Obsidian Git para o GitHub

## Resumo rápido
No seu vault, o plugin está na pasta:

```text
.obsidian/plugins/obsidian-git/
```

Ele **não subiu para o GitHub** porque ainda não foi commitado e enviado com `git push`.

Além disso, um arquivo específico está ignorado localmente:

```text
.obsidian/plugins/obsidian-git/obsidian_askpass.sh
```

Isso vem de:

```text
.git/info/exclude
```

---

## 1) Ver o status atual
```bash
git status --short
```

### O que isso faz
Mostra arquivos novos, alterados ou não rastreados.

No seu caso, a pasta do plugin aparece como não rastreada.

---

## 2) Adicionar o plugin ao Git
```bash
git add .obsidian/plugins/obsidian-git
```

### O que isso faz
Coloca os arquivos do plugin na área de staging para o próximo commit.

---

## 3) Se você também quiser subir a ativação do plugin no Obsidian
Esses arquivos podem ser relevantes:

```bash
git add .obsidian/community-plugins.json .obsidian/core-plugins.json
```

### O que isso faz
- `community-plugins.json` registra plugins de comunidade ativados
- `core-plugins.json` registra configuração dos plugins nativos

Se sua intenção é sincronizar o ambiente do Obsidian entre máquinas, vale adicionar também.

---

## 4) Criar o commit
```bash
git commit -m "Add Obsidian Git plugin"
```

### O que isso faz
Cria um commit com a mensagem que descreve a mudança.

---

## 5) Enviar para o GitHub
```bash
git push -u origin main
```

### O que isso faz
- `git push` envia commits locais para o remoto
- `-u` liga sua branch local à remota
- `origin` é o nome padrão do remoto
- `main` é a branch de destino

---

## 6) Passo a passo exato
Se o objetivo é subir só o plugin, rode nesta ordem:

```bash
git status --short
git add .obsidian/plugins/obsidian-git
git commit -m "Add Obsidian Git plugin"
git push -u origin main
```

---

## 7) Se o repositório ainda não tiver nenhum commit enviado
Como o remoto parece vazio, pode ser que este seja o primeiro push real.

Nesse caso, a sequência acima continua válida.

Se o Git reclamar de identidade, configure antes:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Depois repita:

```bash
git add .obsidian/plugins/obsidian-git
git commit -m "Add Obsidian Git plugin"
git push -u origin main
```

---

## 8) Por que o arquivo `obsidian_askpass.sh` não sobe
Esse arquivo está ignorado no seu repositório local por esta regra:

```text
.git/info/exclude
```

Com a linha:

```text
.obsidian/plugins/obsidian-git/obsidian_askpass.sh
```

### O que isso significa
Mesmo adicionando a pasta do plugin, esse arquivo específico pode continuar fora do commit.

Isso não é necessariamente um problema.

Na prática, normalmente você pode subir o plugin sem esse arquivo.

---

## 9) Como confirmar que subiu
Depois do push:

```bash
git status
```

Se estiver tudo certo, o Git deve mostrar a árvore limpa.

Depois abra o repositório no GitHub e veja se a pasta apareceu.

---

## 10) Quando faz sentido versionar plugins do Obsidian
Faz sentido quando você quer:
- sincronizar setup entre máquinas
- guardar sua configuração do vault
- reconstruir facilmente seu ambiente

Pode não fazer sentido quando:
- o plugin é só local
- você quer manter o vault mais limpo
- há arquivos temporários ou específicos da sua máquina
