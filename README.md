# ChatBot Groq com LangChain
<div align="justify">


Um assistente de chat interativo desenvolvido em Python que utiliza a **API da Groq** e o framework **LangChain** para oferecer conversação livre e funcionalidades de processamento de documentos (websites e vídeos do YouTube).

O projeto é capaz de conversar com o usuário ou atuar como um **RAG (Retrieval-Augmented Generation)** simples, respondendo a perguntas com base no conteúdo de uma URL fornecida.>
---

## Funcionalidades

* **Conversação Livre:** Interaja com o modelo de linguagem **Llama 3.1 70B** em tempo real para qualquer tipo de pergunta ou tarefa.
* **Análise de Websites:** Forneça a URL de um site para que o chatbot possa responder a perguntas ou resumir o conteúdo da página.
* **Análise de Vídeos do YouTube:** Forneça a URL de um vídeo do YouTube para que o chatbot use a transcrição (legendas) para responder a perguntas sobre o conteúdo.
* **Histórico de Conversa:** Mantém o contexto da conversa, permitindo interações mais coerentes e fluidas.

---

## Tecnologias Utilizadas

* **Python:** Linguagem de programação principal.
* **Groq:** Plataforma para inferência rápida de modelos de linguagem (LLMs), usando o modelo `llama-3.3-70b-versatile`.
* **LangChain:** Framework para desenvolvimento de aplicações alimentadas por LLMs, sendo essencial para:
    * `ChatGroq`: Conexão com a API da Groq.
    * `ChatPromptTemplate`: Gerenciamento do sistema de prompt e histórico de mensagens.
    * `WebBaseLoader`: Carregamento e processamento de conteúdo de websites.
    * `YoutubeLoader`: Carregamento e processamento de transcrições de vídeos do YouTube.
* **Variáveis de Ambiente (`os`):** Utilizado para configurar a chave de API da Groq.

---

## Como Executar o Projeto

### Pré-requisitos

1.  **Chave de API da Groq:** Obtenha sua chave de API no site da [Groq Cloud](https://console.groq.com/keys).
2.  **Python:** Tenha o Python (versão 3.x) instalado em sua máquina.

### Instalação

1.  **Clone o repositório** (se estiver em um repositório).
2.  **Instale as dependências** necessárias. Você precisará de:
    ```bash
    pip install langchain-groq langchain-community
    ```

### Configuração da API Key

No código, a chave de API está definida diretamente, mas o **melhor caminho** é utilizar variáveis de ambiente para segurança.

**No código original:**
A chave é definida e carregada no ambiente de execução:

```python
api_key = "gsk_..." # Substitua pela sua chave REAL
os.environ['GROQ_API_KEY'] = api_key
```

</div>