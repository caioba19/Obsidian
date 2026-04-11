# Setup - Node, NVM e CLIs globais

## Resumo rápido
Como você quer instalar ferramentas com `npm i -g`, o caminho certo é:

1. instalar o **NVM**
2. instalar uma versão do **Node.js** usando o NVM
3. conferir se `node` e `npm` funcionam
4. instalar as CLIs globais

---

## 1) O que é NVM
NVM significa **Node Version Manager**.

Ele serve para instalar e trocar versões do Node.js.

### Por que isso é útil
- alguns projetos pedem Node 18
- outros pedem Node 20 ou 22
- com NVM você troca sem reinstalar tudo

---

## 2) No Windows: qual NVM usar
No Windows, o mais comum é usar **nvm-windows**.

Depois de instalar, você costuma usar comandos assim:

```bash
nvm install 22
nvm use 22
node -v
npm -v
```

### O que cada comando faz

#### `nvm install 22`
Baixa e instala a versão 22 do Node.js.

#### `nvm use 22`
Ativa a versão 22 na sua máquina/sessão.

#### `node -v`
Mostra a versão atual do Node.

#### `npm -v`
Mostra a versão atual do npm.

---

## 3) Como instalar as CLIs globais

### Comandos
```bash
npm i -g @openai/codex
npm i -g @google/gemini-cli
npm i -g @github/copilot
npm i -g @gitlawb/openclaude
```

---

## 4) O que cada parte faz

### `npm`
É o gerenciador de pacotes do Node.js.

### `i`
É atalho para `install`.

### `-g`
Significa **global**.

Ou seja, instala a ferramenta para você poder chamá-la no terminal de qualquer pasta.

Sem `-g`, o pacote seria instalado só no projeto atual.

---

## 5) O que cada pacote é

### `@openai/codex`
Instala o pacote/CLI do Codex no escopo global.

### `@google/gemini-cli`
Instala o Gemini CLI globalmente.

### `@github/copilot`
Instala o pacote CLI do GitHub Copilot globalmente.

### `@gitlawb/openclaude`
Instala o OpenClaude globalmente.

---

## 6) Como pensar em instalação global
Quando você instala globalmente, o executável costuma ficar disponível no terminal como comando.

Exemplo de lógica:
- instala com `npm i -g pacote`
- fecha e reabre o terminal, se necessário
- roda o comando da ferramenta

---

## 7) Ordem recomendada
```bash
nvm install 22
nvm use 22
node -v
npm -v
npm i -g @openai/codex
npm i -g @google/gemini-cli
npm i -g @github/copilot
npm i -g @gitlawb/openclaude
```

---

## 8) Verificação prática
Depois da instalação, confira se o sistema reconhece as ferramentas.

Exemplos de checagem:
```bash
node -v
npm -v
```

Se a CLI não for reconhecida, normalmente o problema é um destes:
- Node não foi instalado corretamente
- o terminal precisa ser reaberto
- PATH não foi atualizado ainda
- a instalação global falhou

---

## 9) Regra prática
Se você vai trabalhar com ferramentas modernas de terminal em JavaScript, quase sempre precisa desta base:

- NVM
- Node.js
- npm
- terminal funcionando
