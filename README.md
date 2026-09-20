# 📊 Dashboard de Análise de Imóveis Despublicados (Looker Studio)

> Painel de auditoria e controle de qualidade para monitoramento de anúncios de imóveis publicados na plataforma e despublicados em até 7 dias, cobrindo a performance do time de vendas, gestão de consequências e reincidência.

---

## 🎯 Objetivo & Contexto de Negócio

* **Problema:** Imóveis publicados na plataforma estavam sendo despublicados em um intervalo curto (até 7 dias), sinalizando potenciais inconsistências operacionais ou de cadastro no time de vendas. A gestão não possuía uma visão consolidada para identificar os motivos de criticidade, acompanhar analistas ofensores e garantir a aplicação da gestão de consequências.
* **Solução:** Criação de um **Dashboard no Looker Studio** alimentado por uma planilha central de controle. A solução estruturou o acompanhamento de ponta a ponta: desde a evolução semanal do volume de análises até a identificação detalhada de reincidências e oportunidades por operação.

---

## 🛠️ Tecnologias & Ferramentas

* **Visualização de Dados (BI):** [Looker Studio](https://lookerstudio.google.com/)
* **Fonte de Dados:** Google Sheets / Excel (Planilha de Controle Operacional)
* **Modelagem:** Campos calculados do Looker, métricas personalizadas de criticidade e agrupamentos por período/operação.

---

## 🖼️ Demonstração Visual

### 1. Visão Geral e Indicadores Semanais
![Visão Geral do Dashboard](https://via.placeholder.com/800x400.png?text=Cole+aqui+um+print+da+Vis%C3%A3o+Geral)

### 2. Mapeamento de Criticidade e Analistas Ofensores
![Análise de Criticidade](https://via.placeholder.com/800x400.png?text=Cole+aqui+um+print+das+an%C3%A1lises+por+analista)

---

## 📈 Funcionalidades & Visões da Solução

O painel foi projetado com filtros universais (**Período, Operação, Contexto do Listing e Nível de Risco**) que se adaptam dinamicamente a todas as seções:

* 📊 **Volume Geral & Semanal:** Acompanhamento do total de análises realizadas e resumo comparativo de evolução por semana.
* 👥 **Performance por Analista e Operação:** Distribuição da carga de análises por integrante do time e por frente operacional.
* ⚠️ **Gestão de Criticidade:** Identificação do volume de ocorrências por nível de risco e mapeamento dos **principais motivos de criticidade**.
* 🚨 **Analistas Ofensores & Reincidentes:** Painel de rastreamento de desvios recorrentes para suporte em auditorias operacionais.
* ⚖️ **Gestão de Consequência:** Módulo para acompanhamento e controle das tratativas aplicadas aos casos fora do padrão.

---

## ⚙️ Arquitetura do Fluxo de Dados

```text
[ Atendimentos & Imóveis Despublicados (<= 7 dias) ]
                         │
                         ▼
          [ Planilha de Controle / Entrada ]
                         │
                         ▼
         [ Conector Nativo do Looker Studio ]
                         │
                         ▼
   [ Dashboard Interativo com Filtros Universais ]
   (Período | Operação | Contexto Listing | Risco)
