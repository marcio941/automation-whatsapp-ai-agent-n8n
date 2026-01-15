#  Automação Conversacional com IA via WhatsApp (n8n)

##  Visão Geral
Este projeto implementa um **agente de IA conversacional** integrado ao WhatsApp, utilizando o **n8n como orquestrador de automações**.  
A solução permite responder mensagens automaticamente, mantendo contexto de conversa e escalando atendimentos sem intervenção humana.

O sistema foi projetado para rodar em **infraestrutura autohospedada**, garantindo controle total sobre dados e integrações.

---

##  Arquitetura da Solução
A arquitetura é composta por serviços desacoplados:

- **WhatsApp** → Canal de entrada e saída de mensagens  
- **Evolution API** → Interface de comunicação com o WhatsApp  
- **n8n** → Orquestração dos fluxos e regras de negócio  
- **Agente de IA (LLM)** → Interpretação da mensagem e geração de respostas  
- **Redis** → Gerenciamento de contexto conversacional  
- **PostgreSQL** → Persistência de dados  
- **VPS + EasyPanel** → Infraestrutura e deploy

---

##  Funcionamento do Fluxo
1. O usuário envia uma mensagem via WhatsApp  
2. A Evolution API dispara um **Webhook** para o n8n  
3. O n8n processa a mensagem e envia o conteúdo para o agente de IA  
4. A IA interpreta a intenção e gera a resposta  
5. O n8n envia a resposta de volta ao usuário via Evolution API  
6. O contexto da conversa é armazenado no Redis

---

##  Tecnologias Utilizadas
- **n8n**
- **REST API / Webhooks**
- **Evolution API (WhatsApp)**
- **Agente de IA (LLM)**
- **Redis**
- **PostgreSQL**
- **Docker**
- **VPS (Hostinger)**
- **EasyPanel**

---

##  Resultados Alcançados
- Atendimento automatizado 24/7  
- Redução de esforço manual em atendimento  
- Arquitetura escalável e reutilizável  
- Respostas baseadas em contexto conversacional

---

## Estrutura do Repositório

