# Controle de Acessos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, estruturação e controle de acessos a sistemas e dados dentro da empresa. A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é apenas identificar falhas, mas garantir que apenas pessoas autorizadas tenham acesso aos recursos corretos, reduzindo riscos de vazamentos, fraudes e acessos indevidos.

---

## 1. A empresa possui controle formal sobre quem acessa sistemas e dados?

Considere qualquer tipo de acesso — sistemas internos, e-mails corporativos, arquivos, servidores, sistemas em nuvem ou aplicações utilizadas no dia a dia.

- **Se não possui:** seguir os itens 1.1 a 1.3 abaixo.  
- **Se possui:** pular para a etapa 2.  

---

### 1.1 Mapeamento de acessos existentes

A empresa precisa saber exatamente quem acessa o quê.

**O que fazer:**

- Levantar todos os sistemas utilizados pela empresa (ERP, CRM, e-mail, arquivos, etc.)  
- Identificar todos os usuários com acesso a cada sistema  
- Registrar quais permissões cada usuário possui (leitura, edição, administrador)  
- Consolidar essas informações em uma matriz de acessos (planilha ou ferramenta)  

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Matriz de Acessos/` para ver modelos de controle de usuários e permissões.

**Referência legal:**  
- [Art. 6º, VII da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — princípio da segurança  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — obrigação de adotar medidas de segurança  

---

### 1.2 Definição de responsáveis pelos acessos

Sem responsáveis definidos, o controle de acessos se torna informal e inseguro.

**O que fazer:**

- Definir responsáveis por cada sistema (ex: TI, gestor da área)  
- Estabelecer quem pode conceder, alterar ou remover acessos  
- Documentar esse processo formalmente  

**Referência legal:**  
- [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e prestação de contas  

---

### 1.3 Criação de processo formal de gestão de acessos

A concessão de acesso não deve ser feita de forma ad hoc.

**O que fazer:**

- Criar fluxo de solicitação de acesso (ex: via e-mail, sistema ou formulário)  
- Exigir aprovação do gestor responsável antes da liberação  
- Registrar todas as concessões e alterações de acesso  
- Padronizar o processo para toda a empresa  

**Referência legal:**  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 2. A empresa aplica controle de acesso por perfil (RBAC)?

Nem todos os usuários devem ter o mesmo nível de acesso.

- **Se não aplica:** seguir os itens 2.1 e 2.2 abaixo.  
- **Se aplica:** pular para a etapa 3.  

---

### 2.1 Definição de perfis de acesso

O acesso deve ser baseado na função do colaborador.

**O que fazer:**

- Criar perfis de acesso por cargo ou função (ex: financeiro, RH, TI, gestor)  
- Definir quais sistemas e dados cada perfil pode acessar  
- Evitar concessões individuais fora do padrão sempre que possível  

**Referência legal:**  
- [Art. 6º, III da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — princípio da necessidade  

---

### 2.2 Aplicação do princípio do menor privilégio

Cada usuário deve acessar apenas o necessário para sua função.

**O que fazer:**

- Revisar acessos atuais e remover permissões excessivas  
- Garantir que usuários não tenham privilégios administrativos sem necessidade  
- Implementar política clara de restrição de acessos  

**Referência legal:**  
- [Art. 6º, III da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)  

**Referência técnica:**  
- [ISO/IEC 27001](https://www.iso.org/isoiec-27001-information-security.html)

---

## 3. Existe controle sobre o ciclo de vida dos acessos?

A gestão de acessos deve acompanhar toda a jornada do colaborador na empresa.

- **Se não existe:** seguir os itens 3.1 a 3.3 abaixo.  
- **Se existe:** pular para a etapa 4.  

---

### 3.1 Concessão de acesso (onboarding)

**O que fazer:**

- Definir acessos padrão por função no momento da contratação  
- Garantir que todo acesso seja aprovado antes de ser concedido  
- Registrar data, responsável e justificativa  

**Referência legal:**  
- [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.2 Alteração de acesso (movimentações internas)

Mudanças de cargo devem refletir nos acessos.

**O que fazer:**

- Revisar acessos sempre que houver mudança de função  
- Remover acessos antigos que não são mais necessários  
- Atualizar permissões conforme nova responsabilidade  

**Referência legal:**  
- [Art. 6º, III da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.3 Revogação de acesso (offboarding)

Colaboradores desligados não devem manter acesso.

**O que fazer:**

- Revogar todos os acessos imediatamente após desligamento  
- Incluir checklist de acessos no processo de offboarding  
- Garantir bloqueio de e-mail, sistemas e dispositivos  

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Offboarding/`.

**Referência legal:**  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 4. A empresa possui políticas de autenticação seguras?

- **Se não possui:** seguir os itens 4.1 e 4.2 abaixo.  
- **Se possui:** pular para a etapa 5.  

---

### 4.1 Política de senhas

**O que fazer:**

- Exigir senhas fortes  
- Proibir reutilização  
- Definir troca periódica  
- Bloquear após tentativas inválidas  

**Referência legal:**  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

**Referência técnica:**  
- [NIST SP 800-63](https://pages.nist.gov/800-63-3/)

---

### 4.2 Autenticação multifator (MFA / 2FA)

**O que fazer:**

- Implementar MFA em sistemas críticos  
- Priorizar contas privilegiadas  
- Utilizar apps autenticadores ou tokens  

**Referência técnica:**  
- [NIST Digital Identity Guidelines](https://pages.nist.gov/800-63-3/)  
- [ISO/IEC 27001](https://www.iso.org/isoiec-27001-information-security.html)

---

## 5. A empresa registra e monitora acessos?

- **Se não registra:** seguir o item 5.1  
- **Se registra:** pular para a etapa 6  

---

### 5.1 Implementação de logs de acesso

**O que fazer:**

- Registrar acessos (quem, quando, ação)  
- Proteger logs contra alteração  
- Definir retenção  
- Monitorar comportamentos suspeitos  

**Referência legal:**  
- [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 6. A empresa revisa periodicamente os acessos?

- **Se não revisa:** seguir o item 6.1  
- **Se revisa:** pular para a etapa 7  

---

### 6.1 Auditoria de acessos

**O que fazer:**

- Revisar acessos periodicamente  
- Validar com gestores  
- Remover acessos indevidos  
- Documentar revisões  

**📁 Exemplo prático:** `/exemplos/Revisao de Acessos/`

---

## 7. Existe controle sobre acessos de terceiros?

- **Se não existe:** seguir o item 7.1  
- **Se existe:** pular para etapa 8  

---

### 7.1 Gestão de acessos de terceiros

**O que fazer:**

- Identificar terceiros  
- Conceder acessos limitados  
- Revisar e revogar ao final  

**Referência legal:**  
- [Art. 39º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art39)  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 8. A empresa possui controle de acesso físico?

### 8.1 Controle de acesso a ambientes físicos

**O que fazer:**

- Restringir áreas sensíveis  
- Utilizar crachás ou biometria  
- Registrar acessos  
- Acompanhar visitantes  

**Referência legal:**  
- [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 9. Cultura e conscientização sobre acessos

### 9.1 Boas práticas

**O que fazer:**

- Não compartilhar credenciais  
- Bloquear tela  
- Evitar contas compartilhadas  
- Treinar colaboradores  

**Referência legal:**  
- [Art. 6º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

## Riscos comuns associados

- Acessos indevidos  
- Ex-colaboradores ativos  
- Vazamentos de dados  
- Uso indevido de credenciais  
- Falta de rastreabilidade  

---

*Documento gerado como parte do framework data-trust — fase PLAN / controle de acessos.*