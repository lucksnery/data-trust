# Controle de Acessos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, estruturação e controle de acessos a dados pessoais dentro da empresa, conforme os princípios da LGPD (Lei nº 13.709/2018). O objetivo é garantir que apenas pessoas autorizadas tenham acesso aos dados, reduzindo riscos de vazamentos, acessos indevidos e incidentes de segurança.

A abordagem segue o modelo sequencial: cada etapa inicia com um diagnóstico e direciona para ações práticas de adequação.

---

## 1. A empresa controla quem tem acesso aos dados pessoais?

O primeiro passo é entender se existe qualquer tipo de controle sobre quem pode acessar dados — seja em sistemas, arquivos, planilhas ou documentos físicos.

- **Se não existe controle formal:** seguir para os itens 1.1 a 1.3.
- **Se existe, mas é informal ou não documentado:** revisar os itens abaixo.
- **Se existe controle estruturado:** avançar para a etapa 2.

---

### 1.1 Mapeamento de acessos a dados pessoais

Não é possível proteger o que não se conhece. Antes de controlar acessos, é necessário mapear quem acessa o quê.

**O que fazer:**

- Identificar todos os sistemas, pastas, bancos de dados e arquivos que contenham dados pessoais  
- Listar todos os usuários com acesso a esses dados (colaboradores, terceiros, fornecedores)  
- Documentar:
  - Qual usuário acessa quais dados  
  - Qual o nível de acesso (leitura, edição, exclusão)  
  - Qual a justificativa do acesso (função exercida)  
- Consolidar essas informações em uma matriz de controle de acessos (Access Matrix)

---

### 1.2 Definição de perfis de acesso (RBAC)

Nem todo colaborador precisa acessar todos os dados. A LGPD exige limitação de acesso conforme necessidade.

**O que fazer:**

- Criar perfis de acesso baseados em funções (ex: financeiro, RH, marketing, TI)  
- Vincular cada perfil a permissões específicas  
- Evitar acessos genéricos ou compartilhados  
- Garantir que novos usuários sejam vinculados a perfis — nunca a permissões individuais diretas  

**Referência legal:** Art. 6º, III da LGPD — princípio da necessidade (limitação ao mínimo necessário).

---

### 1.3 Aplicação do princípio do menor privilégio

O acesso deve ser restrito ao mínimo necessário para execução da função.

**O que fazer:**

- Revisar acessos existentes e remover permissões excessivas  
- Garantir que:
  - Um colaborador não acesse dados de outro departamento sem necessidade  
  - Dados sensíveis (ex: saúde, biometria) tenham acesso ainda mais restrito  
- Implementar política formal de “least privilege”  

---

## 2. A empresa possui autenticação segura nos sistemas?

Ter controle de acesso não é suficiente se a autenticação for fraca.

- **Se não há políticas de autenticação:** seguir os itens 2.1 a 2.3.  
- **Se há, mas são básicas:** revisar e fortalecer.  
- **Se são robustas:** avançar para a etapa 3.  

---

### 2.1 Política de senhas

Senhas fracas são uma das principais causas de incidentes.

**O que fazer:**

- Exigir senhas com:
  - Mínimo de caracteres (recomendado: 8 ou mais)  
  - Combinação de letras, números e símbolos  
- Proibir reutilização de senhas antigas  
- Bloquear acesso após tentativas inválidas consecutivas  
- Proibir compartilhamento de credenciais  

---

### 2.2 Implementação de autenticação multifator (2FA)

Apenas senha não é suficiente para sistemas críticos.

**O que fazer:**

- Ativar 2FA em:
  - Sistemas com dados pessoais  
  - E-mails corporativos  
  - Acessos administrativos  
- Priorizar aplicativos autenticadores ou tokens  

**Referência legal:** Art. 46º da LGPD — adoção de medidas de segurança técnicas e administrativas.

---

### 2.3 Gestão de credenciais

O ciclo de vida das credenciais precisa ser controlado.

**O que fazer:**

- Criar processo para:
  - Criação de acessos (onboarding)  
  - Alteração de permissões  
  - Revogação imediata em desligamentos (offboarding)  
- Garantir que acessos de ex-colaboradores sejam removidos no mesmo dia  

---

## 3. A empresa monitora os acessos realizados?

Sem monitoramento, não há visibilidade sobre possíveis abusos ou incidentes.

- **Se não há monitoramento:** seguir os itens 3.1 e 3.2.  
- **Se há:** validar qualidade e cobertura.  

---

### 3.1 Registro de logs de acesso

Toda ação relevante deve ser registrada.

**O que fazer:**

- Ativar logs em sistemas que tratam dados pessoais  
- Registrar:
  - Usuário  
  - Data e hora  
  - Ação realizada (visualização, alteração, exclusão)  
- Garantir que os logs sejam protegidos contra alteração  

---

### 3.2 Monitoramento e auditoria de acessos

Registrar não basta — é preciso analisar.

**O que fazer:**

- Criar rotina de auditoria periódica dos logs  
- Identificar:
  - Acessos fora do horário padrão  
  - Tentativas de acesso não autorizadas  
  - Volume incomum de consultas ou downloads  
- Definir responsáveis pela análise (TI, segurança ou DPO)  

---

## 4. A empresa revisa os acessos periodicamente?

Acessos acumulam com o tempo — especialmente em empresas em crescimento.

- **Se não há revisão periódica:** seguir o item 4.1.  
- **Se há:** validar frequência e formalização.  

---

### 4.1 Revisão periódica de acessos

**O que fazer:**

- Realizar revisão de acessos ao menos a cada 6 meses  
- Validar com gestores:
  - Se o colaborador ainda precisa daquele acesso  
  - Se o nível de permissão está adequado  
- Revogar acessos desnecessários imediatamente  
- Documentar todas as revisões realizadas  

---

## 5. A empresa controla acessos de terceiros?

Fornecedores também podem ser um vetor de risco.

- **Se terceiros têm acesso a dados:** seguir os itens 5.1 e 5.2.  
- **Se não têm:** validar periodicamente.  

---

### 5.1 Controle de acesso para terceiros

**O que fazer:**

- Conceder acesso apenas quando necessário  
- Criar usuários individuais — nunca compartilhados  
- Definir prazo de validade para acessos temporários  
- Monitorar atividades realizadas por terceiros  

---

### 5.2 Cláusulas contratuais de acesso

**O que fazer:**

- Incluir cláusulas de:
  - Confidencialidade  
  - Segurança da informação  
  - Responsabilidade sobre uso indevido  
- Garantir que terceiros sigam padrões compatíveis com a LGPD  

**Referência legal:** Art. 39º da LGPD — o operador deve seguir as instruções do controlador.

---

## 6. Existe política formal de controle de acessos?

Sem formalização, o processo não é sustentável.

- **Se não existe política:** seguir o item 6.1.  
- **Se existe:** revisar e atualizar.  

---

### 6.1 Criação da política de controle de acessos

**O que fazer:**

- Documentar política contendo:
  - Regras de concessão de acesso  
  - Critérios de autenticação  
  - Uso de senhas e 2FA  
  - Monitoramento e auditoria  
  - Penalidades em caso de violação  
- Comunicar a política a todos os colaboradores  
- Integrar a política ao programa de segurança da informação  

---

## 7. Os colaboradores estão conscientes sobre controle de acessos?

Tecnologia sem conscientização não funciona.

- **Se não há treinamento:** seguir o item 7.1.  
- **Se há:** revisar periodicidade.  

---

### 7.1 Treinamento sobre acesso e segurança

**O que fazer:**

- Treinar colaboradores sobre:
  - Uso correto de credenciais  
  - Riscos de compartilhamento de acessos  
  - Engenharia social (phishing, pretexting)  
- Simular ataques para validação (ex: phishing interno)  
- Registrar participação e evidências  

---

### Referências legais gerais

- Art. 6º, III — Princípio da necessidade  
- Art. 46º — Segurança da informação  
- Art. 48º — Comunicação de incidentes  
- Art. 39º — Responsabilidade do operador  

---

*Documento gerado como parte do framework data-trust — fase PLAN / controle de acessos.*