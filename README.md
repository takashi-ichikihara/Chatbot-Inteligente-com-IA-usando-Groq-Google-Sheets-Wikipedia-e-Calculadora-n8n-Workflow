# 🤖 Chatbot Inteligente com IA com Groq, Google Sheets, Wikipedia e Calculadora – n8n Workflow

Este projeto é um workflow no [n8n](https://n8n.io) que atua como um **chatbot inteligente**, capaz de:
- Armazenar conversas em uma planilha do Google Sheets,
- Realizar cálculos simples,
- Consultar a Wikipedia,
- Usar um modelo de linguagem (LLM) para responder perguntas abertas,
- Manter contexto entre mensagens com memória simples.

## 🧠 Visão Geral

Este fluxo automatiza o atendimento e processamento de mensagens com IA, integrando múltiplas ferramentas através de um agente inteligente. Ele pode ser usado para criar assistentes virtuais personalizados com capacidade de aprendizado contextual.

## 🔧 Tecnologias e Serviços Utilizados

- **n8n** – Plataforma de automação de workflows.
- **Google Sheets** – Armazenamento de logs/conversas.
- **Groq (LLM via Groq API)** – Respostas baseadas em IA.
- **Wikipedia API** – Pesquisa de informações.
- **Calculadora (n8n built-in)** – Operações matemáticas simples.
- **Simple Memory (n8n built-in)** – Armazenamento de contexto da conversa.

---

## ⚙️ Funcionalidade do Fluxo

1. **Recebe uma mensagem do usuário**.
2. **Edita os dados recebidos (normalização)**.
3. **Registra a mensagem no Google Sheets**.
4. **O Agente IA decide**:
   - Responder diretamente via IA (Groq),
   - Realizar um cálculo,
   - Buscar na Wikipedia,
   - Ou não realizar nenhuma operação.
5. **Responde ao usuário** com base na escolha.
6. **Mantém o contexto** das conversas anteriores com memória simples.

---

## 📦 Instalação e Configuração

### Pré-requisitos

Você precisa ter acesso ou configurar:

1. **Conta no n8n.cloud** ou instalação local do n8n.
2. **Credenciais e permissões para:**
   - **Google Sheets API** (com acesso de escrita à planilha desejada),
   - **Groq API Key** (ou outro provedor de LLM),
   - **Acesso à internet** (para Wikipedia funcionar),
3. **Permissões nos nós utilizados no fluxo:**
   - Editar e conectar nós do tipo: Google Sheets, HTTP Request (para Wikipedia), e ferramentas personalizadas.
4. **Habilitar o módulo de IA Agents e Tools no n8n**, se aplicável (requer plugins beta ou versões recentes).

### Passos

1. Clone ou importe o workflow `.json` para seu ambiente n8n.
2. Configure as credenciais de:
   - Google Sheets
   - Groq (ou outro modelo de linguagem suportado)
3. Configure os nós:
   - Apontar o nó Google Sheets para a planilha correta.
   - Verificar parâmetros do AI Agent.
4. Ative o fluxo e faça testes!

---

## 💡 Exemplos de Uso

- Responder perguntas como “Quem foi Albert Einstein?”
- Realizar contas como “Quanto é 7 * 8?”
- Manter uma conversa com contexto em múltiplas mensagens
- Armazenar todo o histórico da conversa para análise posterior

---

## 📁 Estrutura do Projeto

```text
.
├── README.md
├── Curso-N8N-Gratuito-do-YT---NoCode-Start-Up.json
└── video
      └── agente_de_ia_com_groq.mp4
└── images
    └── 1.png
    └── 2.png
