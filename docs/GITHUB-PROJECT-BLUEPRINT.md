# GitHub Project — Blueprint do Case 04

Este documento define como reconstruir, no GitHub Projects, uma visão executiva e anonimizada do projeto **Adequação Sistêmica para Nova Identificação Fiscal**.

> O objetivo não é reproduzir integralmente o ambiente corporativo original. A proposta é demonstrar, para fins de portfólio, a lógica de governança, rastreabilidade, sprints, riscos, dependências e homologação utilizada no projeto.

## Fonte dos cards

Foram criadas 16 Issues representativas no repositório, todas encerradas como **Completed**, pois o projeto real foi concluído.

Essas Issues representam:
- governança;
- ERP;
- HCM;
- CRM;
- ITSM;
- portais;
- integrações/APIs;
- dados & analytics;
- dependências críticas;
- fornecedor com ciclos de correção.

## Campos recomendados no GitHub Project

| Campo | Tipo | Valores sugeridos |
|---|---|---|
| Status | Single select | Concluído |
| Macrofrente | Single select | Governança; ERP & Financeiro; HCM & Pessoas; CRM & Comercial; ITSM & Serviços; Portais & Canais Digitais; Integrações & APIs; Dados & Analytics; Dependências |
| Sprint | Single select | Sprint 1; Sprint 2; Sprint 3; Sprint 4; Sprint 5; Sprint 6; Sprint 7 |
| Tipo | Single select | Governança; Decisão; Handover; Sistema; Integração; Dados; Dependência; Fornecedor |
| Responsabilidade | Single select | Interna; Interna + Fornecedor; Fornecedor; GP / Tecnologia; GP / Stakeholders; GP / Sustentação; Dados / Tecnologia; Squad externa ao projeto |
| Risco histórico | Single select | Baixo; Médio; Alto |
| Dependência externa | Single select | Sim; Não |
| Homologação | Single select | Não aplicável; Aprovada; Residual |
| Marco | Single select | Estruturação; Execução; Marco intermediário; Estabilização; Encerramento |

## Views recomendadas

### 1. Executive Overview
**Layout:** Table  
**Group by:** Macrofrente  
**Sort:** Sprint crescente

Campos visíveis:
- Title
- Macrofrente
- Sprint
- Risco histórico
- Dependência externa
- Homologação
- Status

Objetivo: mostrar rapidamente a distribuição dos itens pelas macrofrentes.

### 2. Sprints
**Layout:** Board  
**Group by:** Sprint

Objetivo: demonstrar a cadência quinzenal e a distribuição das entregas ao longo do projeto.

### 3. Riscos & Dependências
**Layout:** Table  
**Filtro recomendado:** Risco histórico = Alto OR Dependência externa = Sim

Campos visíveis:
- Title
- Macrofrente
- Responsabilidade
- Risco histórico
- Dependência externa
- Sprint

Objetivo: destacar o modelo de gestão por exceção.

### 4. Governança
**Layout:** Table  
**Filtro recomendado:** Macrofrente = Governança

Objetivo: evidenciar decisões gerenciais, definição do modelo de rastreabilidade, revisão de critério de aceite e handover.

### 5. Sistemas & Integrações
**Layout:** Board  
**Group by:** Macrofrente  
**Filtro recomendado:** Tipo = Sistema OR Tipo = Integração OR Tipo = Dados

Objetivo: apresentar a visão sistêmica sem expor nomes corporativos reais.

## Cards que merecem destaque

- **#3 — Revisar critério de aceite do marco intermediário**  
  Demonstra uma decisão de governança com impacto direto na leitura executiva do projeto.

- **#15 — Priorizar adequação em outra esteira de produto**  
  Demonstra gestão de dependência entre squads/produtos.

- **#16 — Estabilizar solução após três ciclos de correção**  
  Demonstra gestão de fornecedor e tratamento de risco técnico.

## Regra de confidencialidade

Não adicionar ao Project:
- nomes reais de sistemas internos não públicos;
- nomes de colaboradores;
- chamados;
- contratos;
- valores;
- dados pessoais;
- identificadores corporativos;
- arquitetura sensível;
- documentos internos originais.

Use sempre nomenclaturas funcionais e generalizadas.

## Resultado esperado

O GitHub Project deve funcionar como um **digital twin executivo e anonimizado** da governança do projeto, complementando o README com evidência prática de organização, rastreabilidade e gestão visual.
