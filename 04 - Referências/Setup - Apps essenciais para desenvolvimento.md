# Setup - Apps essenciais para desenvolvimento

## Resumo rápido
Se você quer montar uma máquina Windows para começar a desenvolver com Git, Node, CLIs de IA e projetos do GitHub, o conjunto mais importante é:

1. **Git** — versionamento de código
2. **VS Code** — editor de código
3. **PowerShell 7 ou Windows Terminal** — terminal melhor para rodar comandos
4. **Node.js via NVM** — base para instalar CLIs com `npm`
5. **GitHub** — hospedar repositórios e colaborar
6. **Obsidian** — documentação e organização pessoal

---

## 1) Git
O Git registra o histórico do projeto.

### Para que serve
- criar versões do código
- voltar mudanças
- trabalhar em branches
- enviar o projeto para o GitHub

### Sem o Git você não consegue
- clonar repositórios com `git clone`
- commitar mudanças
- enviar código com `git push`

---

## 2) VS Code
É o editor onde você escreve e organiza o código.

### Para que serve
- editar arquivos
- instalar extensões
- abrir terminal integrado
- depurar aplicações

### Extensões úteis
- GitHub Copilot
- Prettier
- ESLint
- Docker
- extensões da linguagem que você usar

---

## 3) PowerShell 7 ou Windows Terminal
Você vai usar terminal o tempo todo para instalar dependências e rodar ferramentas.

### Para que serve
- rodar `git`
- rodar `npm`
- configurar variáveis de ambiente
- iniciar CLIs como OpenClaude, Gemini CLI e Codex

### Diferença prática
- **PowerShell**: shell da Microsoft
- **CMD**: terminal antigo do Windows
- **Windows Terminal**: aplicativo que abre abas com PowerShell, CMD e outros shells

---

## 4) Node.js via NVM
Como seus comandos usam `npm`, você precisa de Node.js instalado.

### O que é Node.js
É o runtime que executa JavaScript fora do navegador.

### O que é npm
É o gerenciador de pacotes que instala bibliotecas e CLIs.

### O que é NVM
É um gerenciador de versões do Node.js.

Ele permite:
- instalar várias versões do Node
- trocar de versão sem reinstalar tudo
- evitar conflitos entre projetos

---

## 5) GitHub
É onde o repositório remoto fica hospedado.

### Para que serve
- guardar backup do projeto
- colaborar com outras pessoas
- abrir pull requests
- sincronizar o que está local com a nuvem

---

## 6) Obsidian
No seu caso, ele entra como ferramenta de documentação e organização.

### Para que serve
- guardar notas técnicas
- documentar setup
- manter checklists e processos
- centralizar links, comandos e aprendizados

---

## Extras que costumam ser úteis
Dependendo do tipo de app que você quer criar:

### Desenvolvimento web
- navegador atualizado
- Postman ou Insomnia
- Docker Desktop

### Desenvolvimento mobile
- Android Studio
- SDK do Android
- emulador
- JDK

### Desenvolvimento com IA e automação
- OpenClaude
- Gemini CLI
- Codex CLI
- GitHub Copilot

---

## Ordem recomendada de instalação
1. Git
2. VS Code
3. Windows Terminal ou PowerShell 7
4. NVM
5. Node.js usando NVM
6. GitHub login
7. CLIs globais com `npm`
8. Configuração de variáveis de ambiente

---

## Regra prática
Se um comando começa com `npm`, quase sempre você precisa primeiro de:

- Node.js
- npm
- terminal funcionando

Se um comando começa com `git`, você precisa de:

- Git instalado
- repositório inicializado ou clonado
- conta no GitHub se quiser sincronizar online
