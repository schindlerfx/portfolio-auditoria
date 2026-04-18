# RAI-002 — Implementação de Controlos Internos (Internal Controls)

**Referência:** RAI-[ANO]-002  
**Tipo:** Auditoria Operacional — Controlos Internos  
**Ambiente:** Empresa manufatureira europeia · Processo de insolvência  
**Framework:** COSO — Control Activities + Risk Assessment  
**Estado:** ✅ Implementado

---

## Contexto

Empresa sem qualquer controlo interno formalizado no setor de compras e recepção de materiais. A ausência de segregação de funções criava exposição directa a risco de fraude — qualquer colaborador com acesso ao processo de compras podia, em teoria, executar todas as etapas sem supervisão independente.

---

## Problema Identificado

### Caso concreto — Fraude detectada

Durante revisão do processo de compras, foi identificado que [N] colaboradores tinham acesso simultâneo a três funções que deveriam estar separadas:

1. **Solicitação** — criação do pedido de compra
2. **Recepção** — confirmação da entrada do material no armazém
3. **Aprovação de pagamento** — autorização do pagamento ao fornecedor

Este acesso acumulado permitia que um único colaborador pudesse criar um pedido fictício, confirmar uma recepção que não ocorreu e autorizar o pagamento correspondente — sem qualquer ponto de controlo independente.

> **Resultado:** Situação de fraude detectada e reportada formalmente à gestão.

---

## Controlos Implementados

### 1. Segregação de Funções (SoD — Segregation of Duties)

**Antes:**
```
Colaborador A → Solicita + Recebe + Aprova pagamento
```

**Depois:**
```
Colaborador A → Solicita material
Colaborador B → Recebe material (independente)
CFO / Gestão  → Aprova pagamento
```

**Referência COSO:** Control Activities, Princípio 10 — *"A organização define e desenvolve actividades de controlo que contribuem para a mitigação de riscos."*

---

### 2. Conferência Cega (Blind Receiving)

**O que é:** Procedimento em que o responsável pela recepção de material no armazém **não tem acesso** às quantidades do pedido de compra antes de efectuar a contagem física.

**Como foi implementado:**
- O pedido de compra é gerado no sistema mas a quantidade não é visível para o recebedor
- O recebedor conta fisicamente e regista a quantidade real
- Só depois o sistema compara as duas quantidades e sinaliza divergências

**Por que importa:** Sem este controlo, o recebedor tende inconscientemente (ou intencionalmente) a confirmar a quantidade do pedido sem contar — o que permite fraude ou simplesmente não detecta erros de entrega.

---

### 3. Auditoria Documental — XML vs. PO

**O que é:** Filtro de conferência automática entre o arquivo XML da factura electrónica e o Pedido de Compra (PO) aprovado no sistema.

**Fluxo implementado:**
```
Factura XML recebida
        ↓
Extracção automática: fornecedor, valor, referência, quantidade
        ↓
Comparação com PO aprovado no sistema
        ↓
✅ Match → pagamento liberado para aprovação
❌ Divergência → pagamento bloqueado + alerta gerado
```

**Risco mitigado:** Pagamentos sem lastro documental — facturas que não correspondem a compras efectivamente aprovadas.

---

### 4. Circularização de Fornecedores

**O que é:** Procedimento de auditoria externa que consiste em contactar directamente os fornecedores para confirmar saldos e condições comerciais acordadas.

**Objectivo:** Detectar transacções extra-contabilísticas — acordos ou pagamentos que não estão reflectidos nos registos da empresa.

**Processo:**
1. Selecção de fornecedores com maior volume de transacções
2. Envio de carta/email de confirmação com o saldo registado internamente
3. Confirmação (ou divergência) pelo fornecedor
4. Análise e reconciliação das diferenças

---

## Documentação Formal

Todos os controlos foram documentados em:
- Procedimento escrito por controlo
- Fluxograma do processo actualizado
- Matriz de responsabilidades (RACI)
- Registo de ocorrências para monitorização contínua

---

## Aprendizagens Técnicas

### O triângulo da fraude (Fraud Triangle — ACFE)
Todo o caso de fraude organizacional envolve três elementos simultâneos:
1. **Pressão** — motivo financeiro ou pessoal
2. **Oportunidade** — acesso e ausência de controlo
3. **Racionalização** — justificação interna do acto

A Segregação de Funções actua directamente sobre o elemento **Oportunidade** — é o controlo mais eficaz para eliminar a possibilidade estrutural de fraude.

### COSO — Risk Assessment (Princípio 7)
> *"A organização identifica riscos para a consecução dos seus objectivos em toda a entidade e analisa os riscos como base para determinar como devem ser geridos."*

A ausência de SoD representava um risco não avaliado formalmente. A implementação começou exactamente aqui — identificar o risco, quantificá-lo e propor o controlo adequado.

### Lição principal
**Controlos internos não existem para desconfiar das pessoas — existem para protegê-las.** Um colaborador honesto que trabalha num sistema sem controlos está vulnerável a ser injustamente suspeito quando algo corre mal. Os controlos criam rastreabilidade que protege todos.

---

## Templates Criados

→ Ver [templates/checklist-bom-validation.md](../../templates/checklist-bom-validation.md)  
→ Ver [templates/registro-ocorrencias.md](../../templates/registro-ocorrencias.md)

---

## Referências

- COSO Internal Control — Integrated Framework (2013), Princípios 7 e 10
- ACFE — Fraud Examiners Manual, Secção Fraud Prevention
- ISA 315 — Identificação e Avaliação de Riscos de Distorção Material

---

*Documento anonimizado em conformidade com LGPD/RGPD.*
