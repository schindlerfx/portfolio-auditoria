# RAI-2026-005 — Ciclo de Destruição de Valor

**Referência:** RAI-2026-005 — Auditoria Operacional Sistémica  
**Data de Emissão:** Abril de 2026  
**Elaborado por:** Analista de Auditoria e Controlos Internos  
**Destinatário:** CFO — Empresa Manufatureira  
**Framework:** COSO — Internal Control Integrated Framework (2013) · COSO ERM (2017)  
**Referência RAI:** Fundamentado em RAI-2026-003 — Ausência de KPIs  
**Período:** 24 meses de observação contínua — 2024/2025 a Abril 2026  
**Classificação:** Interno e Confidencial

---

## 1. Sumário Executivo

A presente auditoria operacional documenta a existência de um ciclo sistémico de destruição de valor numa empresa manufatureira europeia em processo de insolvência, identificado ao longo de 24 meses de observação contínua, indagação multi-nível e análise documental parcial. O ciclo opera de forma invisível — porque a ausência de KPIs (documentada no RAI-2026-003) elimina qualquer mecanismo de detecção precoce.

O ciclo tem causa raiz identificável — overbooking de capacidade produtiva por ausência de processo formal de avaliação de encomendas — e propaga-se por oito elos interdependentes que conectam produção, qualidade, caixa, fornecedores e clima organizacional. Cada elo alimenta o seguinte, acelerando o ciclo em vez de o interromper.

Esta auditoria não é uma constatação de ausência. É uma constatação de presença — a presença de um ciclo destrutivo activo, com evidência documental em três dos quatro elos investigados, e com impacto financeiro directo no contexto de insolvência em que a empresa opera.

> **Nota de independência:** O presente auditor recomendou controlos no âmbito do RAI-2026-002 (SoD, Blind Receiving). A presente auditoria avalia processos distintos e não revê a eficácia dos controlos anteriormente recomendados. Não existe ameaça de autoavaliação. Declaração emitida em conformidade com IIA Standard 1130.

---

## 2. Plano de Auditoria

### 2.1 Origem e Justificação

Este trabalho tem origem directa no RAI-2026-003, que documentou a ausência total de KPIs nos processos críticos da operação. A constatação de que não existem instrumentos de monitorização levantou uma questão de auditoria mais profunda: qual o impacto operacional real dessa ausência? A presente auditoria responde a essa questão, transformando o diagnóstico qualitativo acumulado em 24 meses numa constatação formal com evidência documentada.

### 2.2 Objectivo

Identificar, documentar e quantificar o ciclo sistémico de destruição de valor operacional — mapeando a sua causa raiz, os elos de propagação, os controlos existentes e os gaps de cobertura — e reportar o risco resultante à gestão com recomendações priorizadas.

### 2.3 Procedimentos Aplicados

| Procedimento | Descrição | Grau de asseguração |
|--------------|-----------|---------------------|
| Observação directa | Acompanhamento contínuo dos processos operacionais ao longo de 24 meses | **Limitada** — válida apenas para os momentos observados |
| Indagação formal | Entrevistas estruturadas com a CFO sobre processos financeiros e de decisão | **Limitada** — evidência oral sem confirmação documental |
| Indagação informal | Diálogos com líderes de produção, compras, RH e expedição | **Mínima** — corrobora mas não prova |
| Análise documental | Emails de fornecedores, reclamações de clientes, comunicações internas | **Razoável** — evidência documental mais robusta |

*Base normativa: NBC TA 500 — Evidências de Auditoria*

### 2.4 Âmbito

**Incluído:** Processos de produção e planeamento de capacidade · Compras e relação com fornecedores · Expedição e entrega · Tesouraria · Clima organizacional e RH

**Excluído:** Auditoria financeira às demonstrações contabilísticas · Processos cobertos em RAI-001, RAI-002 e RAI-003 · Sistemas de TI e ERP

### 2.5 Limitação de Âmbito — Declarada

Evidência documental directa para o elo de atraso de entrega (OTD) não estava acessível ao auditor — os registos de comunicação com clientes sobre prazos são geridos directamente pelo dono da organização e não foram disponibilizados. O achado relativo a este elo baseia-se em observação directa e indagação consistente com múltiplos interlocutores. Esta limitação é declarada explicitamente e não invalida a constatação — reduz o grau de certeza de "confirmado por evidência documental" para "suportado por observação e indagação".

---

## 3. Matriz de Controlo Interno

| Risco identificado | SoD | KPIs | Aprovação | Blind Rec. | Proc. formal | GAP? |
|-------------------|-----|------|-----------|------------|-------------|------|
| Overbooking de capacidade produtiva | — | ✗ | ✗ | — | ✗ | **SIM** |
| Sobrecarga e deterioração da qualidade | — | ✗ | — | — | ✗ | **SIM** |
| Atraso na entrega — OTD não medido | — | ✗ | — | — | — | **SIM*** |
| Insatisfação de clientes — não pagamento | — | ✗ | — | — | — | **SIM** |
| Ruptura de caixa — sem projecção | — | ✗ | — | — | — | **SIM** |
| Fornecedor retém matéria-prima | ✓ | ✗ | ~ | ✓ | — | **PARCIAL** |
| Clima hostil — turnover e perda de know-how | — | ✗ | — | — | — | **SIM** |
| Fraude interna — pagamentos | ✓ | — | ✓ | ✓ | — | **NÃO** |

*✓ Controlo adequado · ✗ GAP — controlo inexistente · ~ Controlo parcial · — Não aplicável*  
*\* Evidência suportada por observação e indagação — sem documental directo (ver 2.5)*

---

## 4. Constatações de Auditoria

### CON-01 — Overbooking de Capacidade Produtiva

| Campo | Detalhe |
|-------|---------|
| **Área** | Produção / Planeamento |
| **Nível de risco** | **ALTO** |
| **Critério** | IIA Standards (Série 2000) + COSO ICIF — Control Activities (P10): toda organização deve dispor de processo documentado de avaliação de capacidade operacional antes de assumir compromissos com clientes. |
| **Condição** | Não existe ordem de produção formal nem checklist de avaliação de capacidade. Encomendas aceites com base em julgamento informal sem consulta estruturada à produção. |
| **Causa raiz** | Ausência de processo formal de avaliação de capacidade — decisão tomada por intuição e pressão de caixa. |
| **Efeito** | Sobrecarga sistemática da linha de produção, gerando taxa de defeito elevada, atrasos e activação do ciclo de destruição de capital de giro. Em contexto de insolvência, cada encomenda mal avaliada agrava a posição de liquidez. |
| **Evidência** | Observação directa 24 meses + indagação com líderes de produção + comunicações internas. NBC TA 500. |
| **Referência COSO** | Control Activities — P10 · Risk Assessment — P7 |
| **Recomendação** | Implementar checklist formal de avaliação de capacidade antes de aceitar encomenda. |

### CON-02 — Deterioração da Qualidade sem Mecanismo de Detecção

| Campo | Detalhe |
|-------|---------|
| **Área** | Produção / Qualidade |
| **Nível de risco** | **ALTO** |
| **Critério** | COSO ICIF — Monitoring Activities (P16): a organização deve medir e monitorizar indicadores de qualidade produtiva de forma contínua, antes da expedição. |
| **Condição** | Não existe registo formal de não-conformidades. Avaliação de qualidade por inspecção visual informal sem critérios documentados. Defeitos detectados após expedição. |
| **Causa raiz** | Ausência de controlo de qualidade pré-expedição. Sobrecarga produtiva (CON-01) agrava a frequência de defeitos. |
| **Efeito** | Custos de retrabalho não quantificados, reclamações de clientes com impacto no recebimento. Activação do elo 3 do ciclo: defeito → atraso → cliente não paga. |
| **Evidência** | Emails de clientes reportando defeitos observados pelo auditor. Indagação com responsáveis de produção. NBC TA 500. |
| **Referência COSO** | Monitoring Activities — P16 |
| **Recomendação** | Implementar Taxa de Defeito e Taxa de Retrabalho. Checklist de qualidade obrigatório antes da expedição. |

### CON-03 — Atraso na Entrega sem Registo (OTD)

| Campo | Detalhe |
|-------|---------|
| **Área** | Expedição / Planeamento |
| **Nível de risco** | **ALTO** |
| **Critério** | COSO ICIF — Monitoring Activities (P16): a organização deve monitorizar o cumprimento de prazos de entrega. OTD é a métrica padrão em operações manufatureiras. |
| **Condição** | Não existe registo do prazo prometido nem comparação com o prazo entregue. Atrasos geridos caso a caso sem visibilidade agregada. |
| **Causa raiz** | Ausência de registo estruturado. Consequência directa de CON-01 e CON-02. |
| **Efeito** | Impacto não quantificado no recebimento de clientes internacionais com pagamento condicionado à entrega. |
| **Evidência** | *Observação directa + indagação multi-nível. Evidência documental directa não acessível — limitação declarada em 2.5. NBC TA 500 (asseguração limitada).* |
| **Referência COSO** | Monitoring Activities — P16 |
| **Recomendação** | Implementar OTD. Registo obrigatório de prazo prometido vs. prazo entregue por encomenda. |

### CON-04 — Ruptura de Caixa sem Projecção

| Campo | Detalhe |
|-------|---------|
| **Área** | Tesouraria / Financeiro |
| **Nível de risco** | **ALTO — CRÍTICO EM CONTEXTO DE INSOLVÊNCIA** |
| **Critério** | COSO ICIF — Monitoring Activities (P16): a organização deve dispor de projecção de caixa com horizonte mínimo de 30 dias, monitorizada quinzenalmente. Em contexto de insolvência, este requisito é especialmente crítico. |
| **Condição** | Gestão de caixa reactiva baseada em memória e informação dispersa. Sem projecção estruturada. Saldo devedor a fornecedores não centralizado. |
| **Causa raiz** | Ausência de instrumentos de projecção financeira. Consequência directa de RAI-2026-003. |
| **Efeito** | Impossibilidade de demonstrar capacidade de cumprimento de obrigações a credores. Ruptura detectada apenas quando já ocorreu. Agrava posição negocial no processo de insolvência. |
| **Evidência** | Observação directa de gestão reactiva + indagação formal com CFO. NBC TA 500. |
| **Referência COSO** | Monitoring Activities — P16 |
| **Recomendação** | Activar imediatamente os KPIs de tesouraria já disponíveis no sistema implementado. Reunião de revisão quinzenal com CFO. |

### CON-05 — Fornecedor Retém Matéria-Prima — Controlo Parcial

| Campo | Detalhe |
|-------|---------|
| **Área** | Compras / Fornecedores |
| **Nível de risco** | **MÉDIO-ALTO — CONTROLO PARCIAL EXISTENTE** |
| **Critério** | COSO ICIF — Control Activities (P10): a organização deve assegurar a continuidade do fornecimento de matérias-primas críticas. |
| **Condição** | Existem controlos para risco de fraude (SoD, Blind Receiving — RAI-002). Contudo, sem monitorização do saldo devedor a fornecedores nem projecção de pagamentos. |
| **Causa raiz** | Ruptura de caixa (CON-04) impede pagamentos atempados. Ausência de projecção impede acção preventiva. |
| **Efeito** | Interrupção do fornecimento de matéria-prima crítica, bloqueando a linha de produção. |
| **Evidência** | Emails de fornecedores condicionando entregas a regularização de pagamentos. NBC TA 500 — Inspecção documental (asseguração razoável). |
| **Referência COSO** | Control Activities — P10 · Monitoring Activities — P16 |
| **Recomendação** | Implementar indicador de Saldo Devedor a Fornecedores e Projecção de Caixa. |

### CON-06 — Clima Organizacional Hostil sem Monitorização

| Campo | Detalhe |
|-------|---------|
| **Área** | Recursos Humanos / Ambiente Operacional |
| **Nível de risco** | **MÉDIO-ALTO** |
| **Critério** | COSO ICIF — Control Environment (P1): a organização deve manter ambiente de trabalho que promova o desempenho e a retenção de talento. |
| **Condição** | Sem métrica formal de satisfação ou clima organizacional. Deterioração do ambiente invisível para a gestão em termos quantificáveis. |
| **Causa raiz** | Ausência de cultura de medição de desempenho organizacional. Consequência directa de RAI-2026-003. |
| **Efeito** | Turnover de colaboradores com know-how crítico, perda de memória técnica e aumento de erros. Agrava CON-02 e acelera o ciclo. |
| **Evidência** | Observação directa 24 meses + indagação com líderes de área. NBC TA 500 (asseguração limitada). |
| **Referência COSO** | Control Environment — P1 · Monitoring Activities — P16 |
| **Recomendação** | Implementar eNPS e pesquisa de clima anónima semestral. |

---

## 5. Síntese do Ciclo — Causa Raiz e Propagação

| # | Elo | Mecanismo | Evidência disponível |
|---|-----|-----------|---------------------|
| 1 | Overbooking | Encomendas aceites além da capacidade real | Observação + indagação + comunicações internas |
| 2 | Sobrecarga | Linha de produção opera acima do limite | Observação directa 24 meses |
| 3 | Defeito / Retrabalho | Qualidade deteriora, prazos falham | Emails de reclamação de clientes |
| 4 | Atraso OTD | Entrega fora do prazo prometido | *Observação + indagação (sem documental directo)* |
| 5 | Caixa em ruptura | Cliente insatisfeito não paga | Observação gestão reactiva + indagação CFO |
| 6 | Fornecedor retém MP | Sem caixa, pagamentos atrasam | Emails de fornecedores disponíveis |
| 7 | Clima hostil | Pressão constante, turnover, erros repetem-se | Observação 24 meses + indagação multi-nível |
| 8 | Ciclo reinicia | Sistema volta ao elo 1 com menos margem | **Ciclo confirmado — fecha e acelera** |

---

## 6. Matriz de Risco — Resumo

| Ref. | Constatação | Risco | Evidência | RAI de referência |
|------|------------|-------|-----------|------------------|
| CON-01 | Overbooking de capacidade | **ALTO** | Obs. + Ind. + Doc. | RAI-003 · RAI-006 (em elab.) |
| CON-02 | Deterioração da qualidade | **ALTO** | Obs. + Doc. | RAI-003 CON-02 |
| CON-03 | Atraso OTD sem registo | **ALTO*** | *Obs. + Ind.* | RAI-003 CON-02 |
| CON-04 | Ruptura de caixa sem projecção | **ALTO — CRÍTICO** | Obs. + Ind. | RAI-003 CON-04 |
| CON-05 | Fornecedor retém MP | **MED-ALTO** | Doc. directo | RAI-003 · RAI-002 |
| CON-06 | Clima hostil sem monitorização | **MED-ALTO** | Obs. + Ind. | RAI-003 CON-05 |

*\* CON-03 classificado como ALTO com grau de certeza reduzido por ausência de evidência documental directa — declarado em 2.5.*

---

## 7. Recomendações Consolidadas

| # | Acção | Área | Prazo | Referência |
|---|-------|------|-------|-----------|
| 1 | Activar KPIs de tesouraria já disponíveis no sistema | Tesouraria | Imediato | RAI-003 Rec. 1 e 2 |
| 2 | Implementar checklist de avaliação de capacidade antes de aceitar encomenda | Produção | 30 dias | RAI-006 (em elab.) |
| 3 | Implementar checklist de qualidade antes da expedição | Qualidade | 30 dias | RAI-003 CON-02 |
| 4 | Implementar registo de OTD — prazo prometido vs. entregue | Expedição | 30 dias | RAI-003 CON-02 |
| 5 | Implementar eNPS e pesquisa de clima anónima | RH | 60 dias | RAI-003 CON-05 |
| 6 | Formalizar processo de decisão de aceitação de encomenda | Gestão | 60 dias | RAI-006 (em elab.) |

---

## 8. Nota sobre o Âmbito

Este relatório constitui uma constatação de auditoria operacional — não uma proposta de gestão. A decisão de implementar, adaptar ou rejeitar as recomendações é da exclusiva responsabilidade da Direcção e do CFO. A ausência de resposta formal será registada no Registo de Ocorrências do sistema de controlo financeiro implementado.

---

*Documento anonimizado em conformidade com LGPD/RGPD.*  
*Empresa manufatureira europeia em processo de insolvência — 2026.*
