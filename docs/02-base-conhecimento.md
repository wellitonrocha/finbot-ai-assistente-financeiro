# 📄 Base de Conhecimento — FinBot

---

## 1. Visão Geral

A base de conhecimento do FinBot é composta por dados estruturados que representam o perfil financeiro, histórico de transações, interações anteriores e produtos disponíveis.

Esses dados são utilizados como fonte primária de contexto para geração de respostas, garantindo confiabilidade, rastreabilidade e redução de alucinações.

---

## 2. Dados Utilizados

| Arquivo | Formato | Finalidade |
|---------|---------|------------|
| `historico_atendimento.csv` | CSV | Registro de interações anteriores |
| `perfil_investidor.json` | JSON | Perfil financeiro e tolerância ao risco |
| `produtos_financeiros.json` | JSON | Catálogo de produtos bancários |
| `transacoes.csv` | CSV | Histórico de movimentações |

---

## 3. Estrutura dos Dados

### 3.1 historico_atendimento.csv

Campos principais:

- id_atendimento
- data
- assunto
- canal
- resolvido

---

### 3.2 perfil_investidor.json

Principais atributos:

- nome
- idade
- renda_mensal
- perfil_risco
- objetivos
- horizonte_investimento

---

### 3.3 produtos_financeiros.json

Campos relevantes:

- id_produto
- tipo
- risco
- rentabilidade_esperada
- liquidez
- descricao

---

### 3.4 transacoes.csv

Campos principais:

- data
- descricao
- categoria
- valor
- tipo

---

## 4. Tratamento e Preparação dos Dados

Antes da utilização, os dados passam por:

- Validação de formato
- Padronização de datas
- Normalização de valores monetários
- Remoção de inconsistências
- Tratamento de valores ausentes
- Enriquecimento semântico

Processo realizado via Python e Pandas.

---

## 5. Pipeline de Ingestão

Fluxo de ingestão:

```

Arquivos CSV/JSON → Leitura (Pandas) → Validação → Normalização → Indexação → Armazenamento

```

Etapas:

1. Leitura automatizada
2. Verificação de schema
3. Padronização
4. Persistência
5. Atualização periódica

---

## 6. Estratégia de Integração (RAG)

O FinBot utiliza abordagem de Retrieval-Augmented Generation (RAG) para integrar dados ao modelo generativo.

### 6.1 Processo de Recuperação

1. Identificação da intenção
2. Consulta aos datasets relevantes
3. Filtragem semântica
4. Construção do contexto
5. Envio ao LLM

---

### 6.2 Indexação

Os dados são indexados utilizando:

- Vetorização semântica (embeddings)
- Metadados estruturados
- Filtros por categoria e data

Essa estratégia permite recuperação eficiente e contextualizada.

---

### 6.3 Atualização

- Atualização manual (fase educacional)
- Versionamento via Git
- Logs de modificação
- Auditoria de dados

---

## 7. Integração com Prompts

Os dados são integrados ao prompt por meio de um bloco de contexto estruturado.

Exemplo:

```

[CONTEXT]
Perfil:

* Nome: João Silva
* Risco: Moderado
* Renda: R$ 6.500

Objetivos:

* Reserva de emergência
* Aposentadoria

Transações Recentes:

* Mercado: R$ 450
* Streaming: R$ 55
* Farmácia: R$ 120

Produtos Disponíveis:

* CDB Premium (Risco Baixo)
* Fundo Balanceado (Risco Médio)

```

Esse contexto é inserido dinamicamente antes da geração da resposta.

---

## 8. Qualidade dos Dados

Indicadores monitorados:

- Completude
- Consistência
- Atualidade
- Precisão
- Conformidade

Processos de validação evitam uso de dados degradados.

---

## 9. Segurança da Informação

Medidas adotadas:

- Dados anonimizados
- Ambiente local isolado
- Sem uso de dados reais
- Versionamento controlado
- Controle de acesso

---

## 10. Limitações Atuais

- Base simulada
- Volume reduzido
- Atualização manual
- Ausência de dados externos em tempo real

---

## 11. Evolução Futura

- Integração com APIs bancárias
- Data Lake
- Feature Store
- Atualização automática
- Governança avançada
- Monitoramento de drift

---

## 12. Considerações Finais

A base de conhecimento foi estruturada para suportar geração de respostas confiáveis, escaláveis e auditáveis, servindo como pilar fundamental do funcionamento do FinBot.