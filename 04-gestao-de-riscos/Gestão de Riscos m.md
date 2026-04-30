# Gestão de Riscos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, análise e tratamento de riscos relacionados à segurança da informação e ao tratamento de dados dentro da empresa. A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é eliminar totalmente os riscos, mas identificar, avaliar e reduzir seus impactos a níveis aceitáveis, garantindo maior segurança e continuidade das operações.

---

## 1. A empresa possui um processo formal de gestão de riscos?

Considere qualquer tipo de risco relacionado a dados, sistemas, pessoas ou processos.

- **Se não possui:** seguir os itens 1.1 a 1.3 abaixo.  
- **Se possui:** pular para a etapa 2.  

---

### 1.1 Definição de metodologia de gestão de riscos

A empresa precisa de um padrão para identificar e tratar riscos.

**O que fazer:**

- Definir uma metodologia de gestão de riscos (qualitativa, quantitativa ou híbrida)  
- Estabelecer critérios de avaliação de risco (probabilidade x impacto)  
- Padronizar a forma de registro e análise dos riscos  
- Documentar a metodologia em política formal  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — gestão de riscos em segurança da informação.

---

### 1.2 Identificação de riscos

Não é possível tratar riscos que não são conhecidos.

**O que fazer:**

- Mapear ativos da empresa (dados, sistemas, processos, pessoas)  
- Identificar ameaças como:
  - Vazamento de dados  
  - Erro humano  
  - Ataques cibernéticos ([phishing](https://pt.wikipedia.org/wiki/Phishing), [ransomware](https://pt.wikipedia.org/wiki/Ransomware))  
- Identificar vulnerabilidades (ex: falta de controle, sistemas desatualizados)  
- Registrar todos os riscos identificados  

📁 **Exemplo prático:** Consulte a pasta `/exemplos/Identificacao de Riscos/` para ver modelos de levantamento de riscos.

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — obrigação de proteger dados contra acessos não autorizados e incidentes.

---

### 1.3 Registro de riscos (Risk Register)

Os riscos precisam ser documentados e acompanhados.

**O que fazer:**

- Criar um registro centralizado de riscos ([Risk Register](https://en.wikipedia.org/wiki/Risk_register)) em planilha ou ferramenta  
- Incluir:
  - Descrição do risco  
  - Causa/origem  
  - Impacto  
  - Probabilidade  
  - Responsável  
- Classificar riscos por nível de criticidade  
- Atualizar o registro periodicamente  

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e prestação de contas.

---

## 2. A empresa avalia os riscos identificados?

Nem todo risco tem o mesmo impacto ou prioridade.

- **Se não avalia:** seguir os itens 2.1 e 2.2 abaixo.  
- **Se avalia:** pular para a etapa 3.  

---

### 2.1 Análise de probabilidade e impacto

**O que fazer:**

- Definir critérios claros de probabilidade (baixo, médio, alto)  
- Definir critérios de impacto:
  - Financeiro  
  - Reputacional  
  - Operacional  
  - Legal  
- Avaliar cada risco com base nesses critérios  
- Classificar o nível de risco (baixo, médio, alto, crítico)  

---

### 2.2 Priorização de riscos

Nem todos os riscos devem ser tratados imediatamente.

**O que fazer:**

- Priorizar riscos com maior impacto e probabilidade  
- Definir ordem de tratamento  
- Focar primeiro nos riscos críticos  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — avaliação e priorização de riscos.

---

## 3. A empresa define planos de tratamento para os riscos?

Identificar riscos sem agir sobre eles não gera valor.

- **Se não define:** seguir os itens 3.1 a 3.4 abaixo.  
- **Se define:** pular para a etapa 4.  

---

### 3.1 Estratégias de tratamento de risco

Existem diferentes formas de lidar com riscos.

**O que fazer:**

- Definir estratégia para cada risco:
  - **Mitigar:** reduzir o risco  
  - **Aceitar:** quando o risco é baixo  
  - **Transferir:** (ex: seguros ou terceiros)  
  - **Evitar:** interromper a atividade de risco  
- Documentar a decisão para cada risco  

---

### 3.2 Implementação de controles

**O que fazer:**

- Definir controles técnicos e administrativos para mitigação  

**Exemplos:**

- Controle de acessos  
- Backup de dados  
- Treinamento de colaboradores  
- Monitoramento de sistemas  

- Atribuir responsáveis pela implementação  

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — adoção de medidas de segurança.

---

### 3.3 Plano de ação para riscos

**O que fazer:**

- Criar plano de ação com prazos e responsáveis  
- Definir etapas claras de implementação  
- Acompanhar execução dos planos  

---

### 3.4 Registro das decisões de risco

**O que fazer:**

- Documentar decisões de aceitação ou tratamento  
- Manter histórico das ações realizadas  
- Garantir rastreabilidade  

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — prestação de contas.

---

## 4. A empresa monitora e revisa os riscos periodicamente?

Riscos mudam ao longo do tempo.

- **Se não monitora:** seguir o item 4.1 abaixo.  
- **Se monitora:** pular para a etapa 5.  

---

### 4.1 Monitoramento contínuo de riscos

**O que fazer:**

- Revisar riscos periodicamente (trimestral ou semestral)  
- Atualizar probabilidade e impacto conforme mudanças  
- Identificar novos riscos  
- Reavaliar controles implementados  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — monitoramento contínuo.

---

## 5. A empresa possui plano de resposta a riscos materializados (incidentes)?

Quando o risco acontece, ele se torna um incidente.

- **Se não possui:** seguir o item 5.1 abaixo.  
- **Se possui:** pular para a etapa 6.  

---

### 5.1 Integração com resposta a incidentes

**O que fazer:**

- Definir fluxo de resposta para riscos que se concretizam  
- Integrar gestão de riscos com plano de incidentes  
- Definir responsáveis por resposta e comunicação  
- Registrar ocorrências e aprendizados  

**Referência legal:** [Art. 48º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art48) — comunicação de incidentes.

---

## 6. A alta gestão está envolvida na gestão de riscos?

Gestão de riscos não é apenas responsabilidade da TI.

- **Se não está:** seguir o item 6.1 abaixo.  
- **Se está:** pular para a etapa 7.  

---

### 6.1 Governança de riscos

**O que fazer:**

- Envolver liderança na tomada de decisão sobre riscos  
- Apresentar relatórios periódicos de risco  
- Definir nível de risco aceitável ([risk appetite](https://en.wikipedia.org/wiki/Risk_appetite))  
- Garantir apoio institucional às ações de mitigação  

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização.

---

## 7. A empresa possui cultura de gestão de riscos?

Sem cultura, o processo não se sustenta.

- **Se não possui:** seguir o item 7.1 abaixo.  
- **Se possui:** encerrar o diagnóstico e avançar para a fase DO do framework.  

---

### 7.1 Conscientização sobre riscos

**O que fazer:**

- Treinar colaboradores sobre identificação de riscos  
- Incentivar reporte de vulnerabilidades  
- Integrar gestão de riscos aos processos do dia a dia  
- Promover visão preventiva, não apenas reativa  

---

## Riscos comuns associados à ausência de gestão de riscos

- Falta de preparo para incidentes  
- Decisões sem análise de impacto  
- Exposição a ameaças evitáveis  
- Perdas financeiras e reputacionais  
- Não conformidade com a LGPD  

---

*Documento gerado como parte do framework data-trust — fase PLAN / gestão de riscos.*