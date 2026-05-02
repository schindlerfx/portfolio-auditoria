# Metodologia — Implementação de Segregação de Funções (SoD)

**Referência:** RAI-2026-002  
**Framework:** COSO — Control Activities (P10) + Risk Assessment (P7)  
**Norma:** ISA 315 — Identificação e Avaliação de Riscos  
**Contexto:** Empresa manufatureira europeia em processo de insolvência  
**Classificação:** Anonimizado em conformidade com LGPD/RGPD

---

## 1. Quando aplicar esta metodologia

Esta metodologia aplica-se quando:

- A empresa não tem controlos internos formalizados no processo de compras
- Um único colaborador tem acesso a múltiplas funções incompatíveis
- Foi detectado ou existe risco elevado de fraude interna
- O auditor precisa de estruturar SoD do zero num ambiente sem controlos

---

## 2. O princípio da Segregação de Funções

A SoD (Segregation of Duties) assenta num princípio simples: **nenhum colaborador deve ter acesso simultâneo a funções que, combinadas, permitam executar e ocultar uma fraude**.

No processo de compras, as três funções críticas a separar são:

| Função | Risco se acumulada |
|--------|--------------------|
| Solicitação — criar o pedido de compra | Pode criar pedidos fictícios |
| Recepção — confirmar entrada no armazém | Pode confirmar recepções que não ocorreram |
| Aprovação de pagamento — autorizar pagamento | Pode autorizar pagamentos sem lastro |

**O triângulo da fraude (ACFE):**
```
Pressão (motivo) + Oportunidade (acesso) + Racionalização
      ↓
A SoD elimina a Oportunidade — o elemento mais controlável
```

---

## 3. Metodologia passo a passo

### Passo 1 — Mapear o estado actual

Antes de qualquer implementação, documentar quem tem acesso a quê:

| Colaborador | Solicita | Recebe | Aprova pagamento |
|-------------|----------|--------|-----------------|
| [Colaborador A] | ✓ | ✓ | ✓ |

Este mapeamento é a evidência de auditoria que justifica a implementação dos controlos.

### Passo 2 — Definir a nova estrutura

Redistribuir as funções por pessoas independentes:

```
ANTES:
Colaborador A → Solicita + Recebe + Aprova pagamento

DEPOIS:
Colaborador A → Solicita material
Colaborador B → Recebe material (independente do solicitador)
CFO / Gestão  → Aprova pagamento
```

**Regra de ouro:** Quem solicita não pode receber. Quem recebe não pode aprovar o pagamento.

### Passo 3 — Implementar Conferência Cega (Blind Receiving)

A Blind Receiving complementa a SoD no processo de recepção:

**O que é:** O responsável pela recepção efectua a contagem física **sem ter acesso** às quantidades do pedido de compra.

**Fluxo correcto:**
```
1. PO gerado no sistema → quantidade não visível para o recebedor
2. Recebedor conta fisicamente e regista a quantidade real
3. Sistema compara as duas quantidades
4. Match → processo continua
5. Divergência → alerta gerado para o auditor / gestão
```

**Por que importa:** Sem este controlo, o recebedor tende a confirmar a quantidade do pedido sem contar — inconscientemente ou intencionalmente.

### Passo 4 — Implementar filtro XML vs. PO

Controlo documental que bloqueia pagamentos sem lastro:

```
Factura XML recebida
        ↓
Extracção: fornecedor, valor, referência, quantidade
        ↓
Comparação com PO aprovado no sistema
        ↓
✅ Match → pagamento liberado para aprovação do CFO
❌ Divergência → pagamento bloqueado + alerta gerado
```

### Passo 5 — Documentar formalmente

Todos os controlos implementados devem ser documentados em:

- **Procedimento escrito** — descrição passo a passo de cada controlo
- **Fluxograma** — processo actualizado com os pontos de controlo visíveis
- **Matriz RACI** — quem é Responsável, Aprovador, Consultado, Informado em cada etapa
- **Registo de ocorrências** — log de divergências detectadas para monitorização contínua

---

## 4. Indicadores de eficácia (KPIs de monitorização)

Após implementação, monitorizar:

| KPI | O que mede | Frequência |
|-----|-----------|-----------|
| Nº de divergências XML vs. PO | Tentativas de pagamento sem PO | Mensal |
| Nº de discrepâncias na recepção | Divergências entre PO e contagem física | Por recepção |
| Nº de ocorrências registadas | Volume de irregularidades detectadas | Mensal |

---

## 5. Caso concreto documentado

No contexto desta implementação, o mapeamento do estado actual revelou que colaboradores com acesso acumulado às três funções tinham utilizado essa posição para executar transacções irregulares.

**Resultado:** Detecção e reporte formal à gestão de caso de fraude interna envolvendo 3 colaboradores — documentado no RAI-2026-002.

> Este caso demonstra que a SoD não é apenas um controlo preventivo — é também um controlo detectivo. O próprio processo de mapeamento para implementação revelou a irregularidade.

---

## 6. Conexão ao framework COSO

| Princípio | Aplicação |
|-----------|-----------|
| P7 — Risk Assessment | Identificação do risco de fraude por acumulação de funções |
| P10 — Control Activities | SoD, Blind Receiving e XML vs. PO como controlos concretos |
| P1 — Control Environment | Estabelecer que controlos são respeitados mesmo em contexto de crise |

---

## 7. Nota importante — Controlos protegem as pessoas

> Controlos internos não existem para desconfiar das pessoas — existem para protegê-las. Um colaborador honesto que trabalha num sistema sem controlos está vulnerável a ser injustamente suspeito quando algo corre mal. Os controlos criam rastreabilidade que protege todos.

---

*Metodologia desenvolvida em contexto real — empresa manufatureira europeia, 2026.*  
*Anonimizado em conformidade com LGPD/RGPD.*
