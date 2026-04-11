# Setup - Claude, Anthropic e OpenClaude

## Resumo rápido
Aqui estão as primeiras ideias para não confundir os nomes:

- **Anthropic**: empresa/plataforma
- **Claude**: modelo/assistente da Anthropic
- **Claude Code**: ferramenta de terminal para trabalhar com código
- **OpenClaude**: implementação/fork compatível com o fluxo de trabalho do Claude Code

Se você vai usar CLIs no terminal, o mais importante é:
1. ter Node.js funcionando
2. instalar a CLI certa
3. autenticar ou configurar variáveis de ambiente
4. escolher o modelo/provider correto

---

## 1) O que cada nome significa

### Anthropic
É a empresa/plataforma que oferece modelos Claude e serviços relacionados.

### Claude
É o nome da família de modelos.

### Claude Code
É a experiência de usar Claude no terminal para ajudar em tarefas de desenvolvimento.

### OpenClaude
É uma alternativa compatível com esse fluxo, normalmente usada por terminal e configuração via ambiente.

---

## 2) Primeira configuração: ordem mental correta
Antes de sair configurando variável de ambiente, pense assim:

1. instalar Node.js
2. instalar a CLI
3. ver qual provider ela vai usar
4. definir variáveis só se necessário

---

## 3) Variáveis de ambiente que você mencionou

### PowerShell
```powershell
$env:CLAUDE_CODE_USE_OPENAI="1"
$env:OPENAI_MODEL="codexplan"
```

### CMD
```cmd
setx CLAUDE_CODE_USE_OPENAI "1"
setx OPENAI_MODEL "codexplan"
```

---

## 4) O que cada parte faz

### `CLAUDE_CODE_USE_OPENAI`
Essa variável diz para a ferramenta compatível que ela deve usar um provider/modelo no estilo OpenAI, em vez do caminho padrão do Claude/Anthropic.

### valor `"1"`
Ativa essa opção.

Em variáveis de ambiente, `1` normalmente significa **ligado**.

### `OPENAI_MODEL`
Define qual modelo será usado quando a ferramenta consultar o provider OpenAI-compatível configurado.

### valor `"codexplan"`
É o nome do modelo selecionado.

Ou seja:
- a primeira variável ativa o modo OpenAI
- a segunda escolhe o modelo usado nesse modo

---

## 5) Diferença entre PowerShell e CMD

### PowerShell
```powershell
$env:VAR="valor"
```
Isso define a variável **na sessão atual** do PowerShell.

Se você fechar a janela, a configuração pode deixar de existir.

### CMD com `setx`
```cmd
setx VAR "valor"
```
Isso grava a variável no ambiente do Windows para uso futuro.

Normalmente você precisa:
- fechar e abrir o terminal de novo
- ou abrir uma nova janela

para a variável aparecer nas novas sessões.

---

## 6) Regra prática
Use:
- **PowerShell + `$env:`** quando quiser testar agora
- **CMD + `setx`** quando quiser persistir no Windows

---

## 7) Observação importante
Essas variáveis só fazem sentido se a ferramenta que você está usando realmente suportar esse modo de operação.

Na prática, a lógica é:
- instalar a CLI
- ver a documentação dela
- configurar as variáveis que aquela CLI entende

Se a CLI não ler essas variáveis, elas não terão efeito.

---

## 8) Exemplo mental completo
Se você configurar:

```powershell
$env:CLAUDE_CODE_USE_OPENAI="1"
$env:OPENAI_MODEL="codexplan"
```

você está dizendo algo como:

> "Nesta sessão do terminal, use backend OpenAI-compatível e selecione o modelo `codexplan`."

---

## 9) Checklist rápido
- Node instalado
- npm funcionando
- CLI instalada globalmente
- terminal reiniciado se você usou `setx`
- provider/modelo compatíveis com a CLI
