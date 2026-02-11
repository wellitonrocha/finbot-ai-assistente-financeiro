# 🤖 FinBot — Assistente Financeiro com IA Generativa

Assistente virtual inteligente para análise financeira, planejamento de metas e recomendação de produtos, utilizando Inteligência Artificial Generativa com foco em segurança, governança e confiabilidade.

Projeto desenvolvido no Bootcamp **Bradesco GenAI & Dados (DIO)**.

---

## 📖 Contexto

Com o avanço da IA Generativa, instituições financeiras passaram a demandar sistemas capazes de ir além de chatbots tradicionais.

Este projeto propõe a construção de um **assistente financeiro proativo**, capaz de:

- Interpretar dados do cliente
- Analisar padrões de consumo
- Sugerir soluções personalizadas
- Garantir respostas seguras
- Evitar alucinações

Inspirado na assistente BIA, do Bradesco.

---

## 🎯 Objetivo do Projeto

Desenvolver um agente inteligente capaz de:

- Auxiliar no controle financeiro pessoal
- Analisar perfil de investidor
- Apoiar o planejamento de metas
- Recomendar produtos adequados
- Promover educação financeira

Tudo baseado exclusivamente em dados validados.

---

## ⚙️ Funcionalidades

- 📊 Análise automática de gastos
- 👤 Avaliação de perfil financeiro
- 📈 Sugestão de produtos
- 🧠 Geração de respostas com LLM
- 🔐 Camada de validação anti-alucinação
- 🗂️ Consulta à base de conhecimento

---

## 🏗️ Arquitetura do Sistema

Fluxo principal:

```
Usuário → Interface → Orquestrador → Base de Dados → LLM → Validador → Resposta
```

Componentes:

- Interface (CLI / Web)
- Backend em Python
- Motor de IA Generativa
- Módulo de Recuperação (RAG)
- Camada de Segurança
- Logs e Monitoramento

---

## 🧰 Tecnologias Utilizadas

- Python
- Pandas
- LLM (API / Local)
- LangChain (opcional)
- Streamlit / Gradio (opcional)
- Git & GitHub

---

## ▶️ Como Executar o Projeto

1. Clone o repositório:

```bash
git clone https://github.com/wellitonrocha/finbot-ai-assistente-financeiro
cd finbot-ai-assistente-financeiro
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Execute a aplicação:

```bash
python src/app.py
```

---

## 📁 Estrutura do Repositório

```
📁 finbot-ai-assistente-financeiro/
│
├── data/        # Dados simulados
├── docs/        # Documentação técnica
├── src/         # Código-fonte
├── assets/      # Diagramas e imagens
└── examples/    # Exemplos
```

---

## 📊 Avaliação e Métricas

A qualidade do agente é avaliada por:

* Precisão das respostas
* Taxa de alucinação
* Tempo de resposta
* Coerência com perfil
* Satisfação do usuário

Detalhes em: `docs/04-metricas.md`

---

## 🗺️ Roadmap

* [x] Estrutura inicial
* [x] Documentação base
* [ ] Implementação RAG
* [ ] Interface Web
* [ ] Métricas automatizadas
* [ ] Deploy

---

## 👨‍💻 Autor

**Welliton da Rocha**

Analista de Dados | IA Aplicada | Power BI | Python | SQL

LinkedIn: [www.linkedin.com/in/welliton-rocha-data-analytics](https://www.linkedin.com/in/welliton-rocha-data-analytics/)  
GitHub: [https://github.com/wellitonrocha](https://github.com/wellitonrocha)

---

## 📜 Licença

Projeto educacional desenvolvido para fins de estudo e portfólio.