# Controle de Acessos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, estruturação e controle de acessos a sistemas e dados dentro da empresa, conforme a [Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm).

A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é apenas identificar falhas, mas garantir que apenas pessoas autorizadas tenham acesso aos recursos corretos, reduzindo riscos de vazamentos, fraudes e acessos indevidos.

---

## 1. A empresa possui controle formal sobre quem acessa sistemas e dados?

Considere qualquer tipo de acesso — sistemas internos, e-mails corporativos, arquivos, servidores, sistemas em nuvem ou aplicações utilizadas no dia a dia.

- **Se não possui:** seguir os itens 1.1 a 1.3 abaixo  
- **Se possui:** pular para a etapa 2  

---

### 1.1 Mapeamento de acessos existentes

A empresa precisa saber exatamente quem acessa o quê.

**O que fazer:**

- Levantar todos os sistemas utilizados pela empresa ([ERP](https://pt.wikipedia.org/wiki/ERP), [CRM](https://pt.wikipedia.org/wiki/Customer_relationship_management), e-mail, arquivos, etc.)  
- Identificar todos os usuários com acesso a cada sistema  
- Registrar quais permissões cada usuário possui (leitura, edição, administrador)  
- Consolidar essas informações em uma matriz de acessos (planilha ou ferramenta)  

📁 Exemplo prático: Consulte a pasta `/exemplos/Matriz de Acessos/` para ver modelos de controle de usuários e permissões.

**Referência legal:**  
[Art. 6º, VII da LGPD — princípio da segurança](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º da LGPD — medidas de segurança](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

### 1.2 Definição de responsáveis pelos acessos

Sem responsáveis definidos, o controle de acessos se torna informal e inseguro.

**O que fazer:**

- Definir responsáveis por cada sistema (ex: TI, gestor da área)  
- Estabelecer quem pode conceder, alterar ou remover acessos  
- Documentar esse processo formalmente  

**Referência legal:**  
[Art. 6º, X da LGPD — responsabilização e prestação de contas](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 1.3 Criação de processo formal de gestão de acessos

A concessão de acesso não deve ser feita de forma ad hoc.

**O que fazer:**

- Criar fluxo de solicitação de acesso (ex: via e-mail, sistema ou formulário)  
- Exigir aprovação do gestor responsável antes da liberação  
- Registrar todas as concessões e alterações de acesso  
- Padronizar o processo para toda a empresa  

**Referência legal:**  
[Art. 46º da LGPD — medidas técnicas e administrativas](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 2. A empresa aplica controle de acesso por perfil (RBAC)?

Nem todos os usuários devem ter o mesmo nível de acesso.

- **Se não aplica:** seguir os itens 2.1 e 2.2 abaixo  
- **Se aplica:** pular para a etapa 3  

---

### 2.1 Definição de perfis de acesso

O acesso deve ser baseado na função do colaborador.

**O que fazer:**

- Criar perfis de acesso por cargo ou função (ex: financeiro, RH, TI, gestor)  
- Definir quais sistemas e dados cada perfil pode acessar  
- Evitar concessões individuais fora do padrão sempre que possível  

📘 Saiba mais: [RBAC — Role-Based Access Control](https://pt.wikipedia.org/wiki/Controle_de_acesso_baseado_em_fun%C3%A7%C3%B5es)

**Referência legal:**  
[Art. 6º, III da LGPD — princípio da necessidade](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 2.2 Aplicação do princípio do menor privilégio

Cada usuário deve acessar apenas o necessário para sua função.

**O que fazer:**

- Revisar acessos atuais e remover permissões excessivas  
- Garantir que usuários não tenham privilégios administrativos sem necessidade  
- Implementar política clara de restrição de acessos  

📘 Saiba mais: [Princípio do menor privilégio](https://pt.wikipedia.org/wiki/Princ%C3%ADpio_do_menor_privil%C3%A9gio)

**Referência legal:**  
[Art. 6º, III da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

**Referência técnica:**  
[ISO/IEC 27001](https://www.iso.org/isoiec-27001-information-security.html)

---

## 3. Existe controle sobre o ciclo de vida dos acessos?

A gestão de acessos deve acompanhar toda a jornada do colaborador na empresa.

- **Se não existe:** seguir os itens 3.1 a 3.3 abaixo  
- **Se existe:** pular para a etapa 4  

---

### 3.1 Concessão de acesso (onboarding)

📘 Saiba mais: [Onboarding](https://pt.wikipedia.org/wiki/Onboarding)

**O que fazer:**

- Definir acessos padrão por função no momento da contratação  
- Garantir que todo acesso seja aprovado antes de ser concedido  
- Registrar data, responsável e justificativa  

**Referência legal:**  
[Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.2 Alteração de acesso (movimentações internas)

Mudanças de cargo devem refletir nos acessos.

**O que fazer:**

- Revisar acessos sempre que houver mudança de função  
- Remover acessos antigos que não são mais necessários  
- Atualizar permissões conforme nova responsabilidade  

**Referência legal:**  
[Art. 6º, III da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.3 Revogação de acesso (offboarding)

📘 Saiba mais: [Offboarding](https://en.wikipedia.org/wiki/Offboarding)

**O que fazer:**

- Revogar todos os acessos imediatamente após desligamento  
- Incluir checklist de acessos no processo de offboarding  
- Garantir bloqueio de e-mail, sistemas e dispositivos  

📁 Exemplo prático: Consulte a pasta `/exemplos/Offboarding/` para ver checklist completo de revogação de acessos.

**Referência legal:**  
[Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 4. A empresa possui políticas de autenticação seguras?

O controle de acesso depende diretamente da segurança das credenciais.

- **Se não possui:** seguir os itens 4.1 e 4.2 abaixo  
- **Se possui:** pular para a etapa 5  

---

### 4.1 Política de senhas

**O que fazer:**

- Exigir senhas fortes (mínimo de caracteres, complexidade)  
- Proibir reutilização de senhas  
- Definir política de troca periódica  
- Bloquear acesso após tentativas inválidas  

📘 Saiba mais: [Autenticação](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o)

**Referência legal:**  
[Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

### 4.2 Autenticação multifator (MFA / 2FA)

📘 Saiba mais: [Autenticação de dois fatores](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o_de_dois_fatores)

**O que fazer:**

- Implementar MFA em sistemas críticos (e-mail, VPN, sistemas financeiros)  
- Priorizar contas com privilégios elevados  
- Utilizar aplicativos autenticadores ou tokens  

**Referência técnica:**  
[NIST SP 800-63](https://pages.nist.gov/800-63-3/)

---

## 5. A empresa registra e monitora acessos?

Sem rastreabilidade, não é possível investigar incidentes.

- **Se não registra:** seguir o item 5.1 abaixo  
- **Se registra:** pular para a etapa 6  

---

### 5.1 Implementação de logs de acesso

📘 Saiba mais: [Log (informática)](https://pt.wikipedia.org/wiki/Log_(inform%C3%A1tica))

**O que fazer:**

- Registrar acessos a sistemas sensíveis (quem, quando, o que fez)  
- Garantir que logs não possam ser alterados por usuários comuns  
- Definir tempo de retenção dos logs  
- Monitorar acessos suspeitos ou fora do padrão  

**Referência legal:**  
[Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 6. A empresa revisa periodicamente os acessos?

Acessos tendem a se acumular ao longo do tempo.

- **Se não revisa:** seguir o item 6.1 abaixo  
- **Se revisa:** pular para a etapa 7  

---

### 6.1 Auditoria de acessos

📘 Saiba mais: [Auditoria de sistemas](https://pt.wikipedia.org/wiki/Auditoria_de_sistemas)

**O que fazer:**

- Realizar revisão periódica (trimestral ou semestral)  
- Validar com gestores se os acessos ainda são necessários  
- Remover acessos obsoletos ou indevidos  
- Documentar as revisões realizadas  

📁 Exemplo prático: Consulte a pasta `/exemplos/Revisao de Acessos/`

---

## 7. Existe controle sobre acessos de terceiros?

Fornecedores também podem representar risco.

- **Se não existe:** seguir o item 7.1 abaixo  
- **Se existe:** pular para a etapa 8  

---

### 7.1 Gestão de acessos de terceiros

📘 Saiba mais: [Terceirização](https://pt.wikipedia.org/wiki/Terceiriza%C3%A7%C3%A3o)

**O que fazer:**

- Identificar todos os terceiros com acesso a sistemas ou dados  
- Conceder acessos limitados e temporários  
- Exigir autenticação segura  
- Revisar acessos periodicamente  
- Revogar acessos ao fim do contrato  

**Referência legal:**  
[Art. 39º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art39)

---

## 8. A empresa possui controle de acesso físico?

A segurança não é apenas digital.

- **Se não possui:** seguir o item 8.1 abaixo  
- **Se possui:** pular para a etapa 9  

---

### 8.1 Controle de acesso a ambientes físicos

📘 Saiba mais: [Controle de acesso](https://pt.wikipedia.org/wiki/Controle_de_acesso)

**O que fazer:**

- Restringir acesso a áreas sensíveis (servidores, arquivos físicos)  
- Utilizar crachás, biometria ou controle de visitantes  
- Registrar entradas e saídas  
- Acompanhar visitantes dentro da empresa  

**Referência legal:**  
[Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 9. A empresa possui políticas e cultura relacionadas ao controle de acessos?

Tecnologia sem cultura não é suficiente.

- **Se não possui:** seguir o item 9.1 abaixo  
- **Se possui:** encerrar o diagnóstico e avançar para a fase DO do framework  

---

### 9.1 Conscientização sobre controle de acessos

📘 Saiba mais: [Engenharia social](https://pt.wikipedia.org/wiki/Engenharia_social_(seguran%C3%A7a))

**O que fazer:**

- Orientar colaboradores a não compartilhar credenciais  
- Incentivar bloqueio de tela ao se ausentar  
- Proibir uso de contas compartilhadas  
- Promover boas práticas de uso de sistemas  
- Integrar o tema aos treinamentos de segurança  

**Referência legal:**  
[Art. 6º, VII e X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

## ⚠️ Riscos comuns associados à ausência de controle de acessos

- Acessos indevidos por colaboradores  
- Ex-colaboradores com acesso ativo  
- Vazamento de informações sensíveis  
- Uso indevido de credenciais  
- Falta de rastreabilidade em incidentes  

---

*Documento gerado como parte do framework data-trust — fase PLAN / controle de acessos.*