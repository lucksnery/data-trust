# Controle de Acessos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, estruturação e controle de acessos a sistemas e dados dentro da empresa, conforme a [Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm).  

A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto.

O objetivo é garantir que apenas pessoas autorizadas tenham acesso aos recursos corretos, reduzindo riscos de vazamentos, fraudes e acessos indevidos.

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

📁 **Exemplo prático:** Consulte `/exemplos/Matriz de Acessos/`

**Referência legal:**  
[Art. 6º, VII — Princípio da Segurança](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º — Medidas de Segurança](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

### 1.2 Definição de responsáveis pelos acessos

Sem responsáveis definidos, o controle se torna informal e inseguro.

**O que fazer:**

- Definir responsáveis por cada sistema (ex: TI, gestor da área)  
- Estabelecer quem pode conceder, alterar ou remover acessos  
- Documentar esse processo formalmente  

**Referência legal:**  
[Art. 6º, X — Responsabilização e Prestação de Contas](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 1.3 Criação de processo formal de gestão de acessos

A concessão de acesso não deve ser feita de forma ad hoc.

**O que fazer:**

- Criar fluxo de solicitação de acesso (ex: e-mail, sistema ou formulário)  
- Exigir aprovação do gestor responsável  
- Registrar todas as concessões e alterações  
- Padronizar o processo para toda a empresa  

**Referência legal:**  
[Art. 46º — Segurança de Dados](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 2. A empresa aplica controle de acesso por perfil (RBAC)?

Nem todos os usuários devem ter o mesmo nível de acesso.

- **Se não aplica:** seguir os itens 2.1 e 2.2  
- **Se aplica:** pular para a etapa 3  

---

### 2.1 Definição de perfis de acesso

O acesso deve ser baseado na função do colaborador.

**O que fazer:**

- Criar perfis por cargo ou função (financeiro, RH, TI, etc.)  
- Definir quais sistemas cada perfil pode acessar  
- Evitar concessões individuais fora do padrão  

📘 Saiba mais: [RBAC — Role-Based Access Control](https://pt.wikipedia.org/wiki/Controle_de_acesso_baseado_em_fun%C3%A7%C3%B5es)

**Referência legal:**  
[Art. 6º, III — Princípio da Necessidade](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 2.2 Princípio do menor privilégio

Cada usuário deve acessar apenas o necessário.

**O que fazer:**

- Revisar acessos e remover excessos  
- Evitar privilégios administrativos desnecessários  
- Implementar política de restrição  

📘 Saiba mais: [Princípio do Menor Privilégio](https://pt.wikipedia.org/wiki/Princ%C3%ADpio_do_menor_privil%C3%A9gio)

**Referência legal:**  
[Art. 6º, III](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

**Referência técnica:**  
[ISO/IEC 27001](https://www.iso.org/isoiec-27001-information-security.html)

---

## 3. Existe controle sobre o ciclo de vida dos acessos?

A gestão deve acompanhar toda a jornada do colaborador.

- **Se não existe:** seguir 3.1 a 3.3  
- **Se existe:** pular para a etapa 4  

---

### 3.1 Concessão de acesso (onboarding)

📘 Saiba mais: [Onboarding](https://pt.wikipedia.org/wiki/Onboarding)

**O que fazer:**

- Definir acessos padrão por função  
- Garantir aprovação antes da concessão  
- Registrar data, responsável e justificativa  

**Referência legal:**  
[Art. 6º, X](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.2 Alteração de acesso (movimentações internas)

**O que fazer:**

- Revisar acessos ao mudar de função  
- Remover acessos antigos  
- Atualizar permissões  

**Referência legal:**  
[Art. 6º, III](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)

---

### 3.3 Revogação de acesso (offboarding)

📘 Saiba mais: [Offboarding](https://en.wikipedia.org/wiki/Offboarding)

**O que fazer:**

- Revogar acessos imediatamente  
- Usar checklist de desligamento  
- Bloquear e-mail e sistemas  

📁 **Exemplo:** `/exemplos/Offboarding/`

**Referência legal:**  
[Art. 46º](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 4. A empresa possui políticas de autenticação seguras?

- **Se não possui:** seguir 4.1 e 4.2  
- **Se possui:** pular para a etapa 5  

---

### 4.1 Política de senhas

**O que fazer:**

- Exigir senhas fortes  
- Proibir reutilização  
- Definir troca periódica  
- Bloquear tentativas inválidas  

📘 Saiba mais: [Autenticação](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o)

**Referência legal:**  
[Art. 46º](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

### 4.2 Autenticação multifator (MFA / 2FA)

📘 Saiba mais: [Autenticação de dois fatores (2FA)](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o_de_dois_fatores)

**O que fazer:**

- Implementar MFA em sistemas críticos  
- Priorizar contas administrativas  
- Utilizar apps autenticadores  

**Referência técnica:**  
[NIST SP 800-63](https://pages.nist.gov/800-63-3/)

---

## 5. A empresa registra e monitora acessos?

- **Se não registra:** seguir 5.1  
- **Se registra:** pular para a etapa 6  

---

### 5.1 Logs de acesso

📘 Saiba mais: [Log (informática)](https://pt.wikipedia.org/wiki/Log_(inform%C3%A1tica))

**O que fazer:**

- Registrar acessos (quem, quando, ação)  
- Proteger logs contra alteração  
- Monitorar comportamentos suspeitos  

**Referência legal:**  
[Art. 6º, X](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6)  
[Art. 46º](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46)

---

## 6. A empresa revisa periodicamente os acessos?

- **Se não revisa:** seguir 6.1  
- **Se revisa:** pular para a etapa 7  

---

### 6.1 Auditoria de acessos

📘 Saiba mais: [Auditoria de sistemas](https://pt.wikipedia.org/wiki/Auditoria_de_sistemas)

**O que fazer:**

- Revisão trimestral ou semestral  
- Validar com gestores  
- Remover acessos indevidos  
- Documentar revisões  

📁 **Exemplo:** `/exemplos/Revisao de Acessos/`

---

## 7. Existe controle sobre acessos de terceiros?

- **Se não existe:** seguir 7.1  
- **Se existe:** pular para a etapa 8  

---

### 7.1 Gestão de terceiros

📘 Saiba mais: [Terceirização](https://pt.wikipedia.org/wiki/Terceiriza%C3%A7%C3%A3o)

**O que fazer:**

- Identificar terceiros com acesso  
- Conceder acessos limitados  
- Revisar periodicamente  
- Revogar ao fim do contrato  

**Referência legal:**  
[Art. 39º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art39)

---

## 8. A empresa possui controle de acesso físico?

- **Se não possui:** seguir 8.1  
- **Se possui:** pular para a etapa 9  

---

### 8.1 Controle físico

📘 Saiba mais: [Controle de acesso](https://pt.wikipedia.org/wiki/Controle_de_acesso)

**O que fazer:**

- Restringir áreas sensíveis  
- Utilizar crachá ou biometria  
- Registrar entradas e saídas  

---

## 9. Existe cultura e conscientização sobre acessos?

- **Se não existe:** seguir 9.1  
- **Se existe:** encerrar diagnóstico  

---

### 9.1 Conscientização

📘 Saiba mais: [Engenharia social](https://pt.wikipedia.org/wiki/Engenharia_social_(seguran%C3%A7a))

**O que fazer:**

- Não compartilhar credenciais  
- Bloquear tela ao se ausentar  
- Evitar contas compartilhadas  
- Promover boas práticas  

---

## ⚠️ Riscos comuns

- Acessos indevidos por colaboradores  
- Ex-colaboradores com acesso ativo  
- Vazamento de dados sensíveis  
- Uso indevido de credenciais  
- Falta de rastreabilidade  

---

*Documento gerado como parte do framework data-trust — fase PLAN / controle de acessos.*