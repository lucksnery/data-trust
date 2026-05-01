# Gestão de Riscos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, análise e tratamento de riscos relacionados à segurança da informação, processos e dados dentro da empresa. A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é eliminar totalmente os riscos, mas identificar, avaliar e reduzir seus impactos a níveis aceitáveis, garantindo maior segurança, previsibilidade e continuidade das operações.

---

## 1. A empresa possui um processo formal de gestão de riscos?

Considere qualquer tipo de risco relacionado a dados, sistemas, pessoas, processos ou operações.

- **Se não possui:** seguir os itens 1.1 a 1.3 abaixo.  
- **Se possui:** pular para a etapa 2.  

---

### 1.1 Definição de metodologia de gestão de riscos

A empresa precisa de um padrão claro para identificar e tratar riscos.

**O que fazer:**

- Definir uma metodologia de gestão de riscos (qualitativa, quantitativa ou híbrida)  
- Estabelecer critérios de avaliação (probabilidade x impacto)  
- Padronizar a forma de identificação e análise de riscos  
- Documentar a metodologia em política formal  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — gestão de riscos em segurança da informação.

---

### 1.2 Identificação de riscos

Não é possível tratar riscos que não são conhecidos.

**O que fazer:**

- Mapear os ativos da empresa (dados, sistemas, pessoas, processos)  
- Identificar ameaças como:
  - Vazamento de dados  
  - Falha de sistema  
  - Erro humano  
  - Ataques externos ([phishing](https://pt.wikipedia.org/wiki/Phishing), [ransomware](https://pt.wikipedia.org/wiki/Ransomware))  
- Identificar vulnerabilidades (ex: ausência de controle, sistemas desatualizados, falha de processo)  
- Registrar todos os riscos identificados  

📁 **Exemplo prático:** Consulte a pasta `/exemplos/Identificacao de Riscos/` para ver modelos de levantamento de riscos.

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — obrigação de adotar medidas de segurança para proteção contra riscos e incidentes.

---

### 1.3 Registro de riscos (Risk Register)

Os riscos precisam ser documentados e acompanhados ao longo do tempo.

**O que fazer:**

- Criar um registro centralizado de riscos ([Risk Register](https://en.wikipedia.org/wiki/Risk_register)) em planilha ou ferramenta  
- Incluir:
  - Descrição  
  - Causa  
  - Impacto  
  - Probabilidade  
  - Responsável  
- Classificar riscos por nível de criticidade  
- Atualizar o registro periodicamente  

📁 **Exemplo prático:** Consulte a pasta `/exemplos/Risk Register/` para ver modelos de registro de riscos.

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e prestação de contas.

---

## 2. A empresa avalia os riscos identificados?

Nem todo risco tem o mesmo impacto ou prioridade.

- **Se não avalia:** seguir os itens 2.1 e 2.2 abaixo.  
- **Se avalia:** pular para a etapa 3.  

---

### 2.1 Análise de probabilidade e impacto

**O que fazer:**

- Definir critérios de probabilidade (baixo, médio, alto)  
- Definir critérios de impacto:
  - Financeiro  
  - Operacional  
  - Reputacional  
  - Legal  
- Avaliar cada risco com base nesses critérios  
- Classificar o nível de risco  

---

### 2.2 Priorização de riscos

Nem todos os riscos devem ser tratados ao mesmo tempo.

**O que fazer:**

- Priorizar riscos com maior impacto e probabilidade  
- Definir ordem de tratamento  
- Focar inicialmente nos riscos críticos  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — avaliação e priorização de riscos.

---

## 3. A empresa define planos de tratamento para os riscos?

Identificar riscos sem agir sobre eles não reduz exposição.

- **Se não define:** seguir os itens 3.1 a 3.4 abaixo.  
- **Se define:** pular para a etapa 4.  

---

### 3.1 Estratégias de tratamento de risco

**O que fazer:**

- Definir estratégia para cada risco identificado:
  - **Mitigar:** reduzir o risco  
  - **Aceitar:** quando o risco é baixo  
  - **Transferir:** (ex: seguros ou terceiros)  
  - **Evitar:** interromper a atividade de risco  
- Documentar a decisão adotada  

---

### 3.2 Implementação de controles

**O que fazer:**

- Definir controles técnicos e administrativos para mitigação  

**Exemplos:**

- Controle de acessos  
- Backup de dados  
- Monitoramento de sistemas  
- Treinamento de colaboradores  

- Atribuir responsáveis pela implementação  

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — adoção de medidas de segurança para proteção de dados.

---

### 3.3 Plano de ação para riscos

**O que fazer:**

- Criar plano de ação com responsáveis e prazos  
- Definir etapas claras de execução  
- Acompanhar o progresso das ações  

---

### 3.4 Registro das decisões de risco

**O que fazer:**

- Documentar decisões de aceitação, mitigação ou transferência  
- Manter histórico das ações realizadas  
- Garantir rastreabilidade das decisões  

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — prestação de contas.

---

## 4. A empresa monitora e revisa os riscos periodicamente?

Riscos mudam conforme o ambiente e os processos evoluem.

- **Se não monitora:** seguir o item 4.1 abaixo.  
- **Se monitora:** pular para a etapa 5.  

---

### 4.1 Monitoramento contínuo de riscos

**O que fazer:**

- Revisar riscos periodicamente (trimestral ou semestral)  
- Atualizar avaliações de probabilidade e impacto  
- Identificar novos riscos  
- Reavaliar controles implementados  

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — monitoramento contínuo de riscos.

---

## 5. A empresa possui integração entre gestão de riscos e incidentes?

Quando um risco se concretiza, ele se torna um incidente.

- **Se não possui:** seguir o item 5.1 abaixo.  
- **Se possui:** pular para a etapa 6.  

---

### 5.1 Integração com resposta a incidentes

**O que fazer:**

- Definir fluxo de resposta para riscos materializados  
- Integrar gestão de riscos ao plano de resposta a incidentes  
- Definir responsáveis por resposta e comunicação  
- Registrar ocorrências e aprendizados  

**Referência legal:** [Art. 48º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art48) — comunicação de incidentes de segurança.

---

## 6. A alta gestão está envolvida na gestão de riscos?

Gestão de riscos exige apoio da liderança.

- **Se não está:** seguir o item 6.1 abaixo.  
- **Se está:** pular para a etapa 7.  

---

### 6.1 Governança de riscos

**O que fazer:**

- Envolver a liderança na tomada de decisões sobre riscos  
- Definir nível de risco aceitável ([risk appetite](https://en.wikipedia.org/wiki/Risk_appetite))  
- Apresentar relatórios periódicos de riscos  
- Garantir apoio às ações de mitigação  

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e governança.

---

## 7. A empresa possui cultura de gestão de riscos?

Sem cultura, o processo não se sustenta.

- **Se não possui:** seguir o item 7.1 abaixo.  
- **Se possui:** encerrar o diagnóstico e avançar para a fase DO do framework.  

---

### 7.1 Conscientização sobre riscos

**O que fazer:**

- Treinar colaboradores sobre identificação de riscos  
- Incentivar o reporte de riscos e vulnerabilidades  
- Integrar gestão de riscos ao dia a dia das áreas  
- Promover cultura preventiva, não apenas reativa  

---

## Riscos comuns associados à ausência de gestão de riscos

- Falta de preparo para incidentes  
- Decisões sem análise de impacto  
- Exposição a ameaças evitáveis  
- Perdas financeiras e operacionais  
- Não conformidade com requisitos legais e regulatórios  

---

*Documento gerado como parte do framework data-trust — fase PLAN / gestão de riscos.*