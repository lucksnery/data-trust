# Adequação à LGPD — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação do cenário atual da empresa em relação à [Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) e da [ANPD (Autoridade Nacional de Proteção de Dados)](https://www.gov.br/cidadania/pt-br/acesso-a-informacao/institucional/anpd). A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é apenas mapear lacunas, mas entregar um caminho claro do que precisa ser feito para alcançar a conformidade.

---

## 1. A empresa possui um website ou presença digital ativa?

Considere qualquer domínio ativo onde a empresa coleta, recebe ou exibe dados de usuários — site institucional, landing pages, e-commerce, portais de clientes ou aplicações web.

- **Se não possui:** pular para a etapa 2.
- **Se possui:** seguir os itens 1.1 a 1.4 abaixo.

---

### 1.1 Banner de gerenciamento de cookies

O site coleta [cookies](https://pt.wikipedia.org/wiki/Cookie_(inform%C3%A1tica)) de terceiros, analytics, publicidade ou rastreamento? Pela LGPD, o usuário precisa ser informado e dar consentimento antes de qualquer coleta não essencial.

**O que fazer:**

- Implementar um banner de cookies visível logo na primeira visita, antes de qualquer rastreamento ser ativado
- O banner deve oferecer ao usuário a opção de aceitar, recusar ou personalizar as categorias de cookies
- Utilizar uma plataforma de gestão de consentimento (CMP), como CookieYes, Osano, Cookiebot ou solução própria
- Registrar e armazenar o consentimento do usuário com data, hora e versão da política vigente
- Garantir que cookies não essenciais só sejam disparados após consentimento explícito

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Banner de Gerenciamento de Cookies/` para ver modelos de implementação de banner com boas práticas.

**Referência legal:** [Art. 7º, I da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art7) — o consentimento deve ser livre, informado e inequívoco.

---

### 1.2 Página de política de privacidade

A empresa precisa comunicar de forma clara e acessível como trata os dados pessoais de seus usuários.

**O que fazer:**

- Criar uma página dedicada de política de privacidade, com URL fixa e de fácil acesso (rodapé do site)
- O documento deve conter, no mínimo:
  - Quais dados são coletados e com qual finalidade
  - A base legal utilizada para cada tratamento (consentimento, legítimo interesse, contrato, etc.)
  - Com quem os dados são compartilhados (parceiros, fornecedores, plataformas)
  - Por quanto tempo os dados são retidos
  - Como o titular pode exercer seus direitos (acesso, correção, exclusão, portabilidade)
  - Contato do DPO ou canal responsável
- A linguagem deve ser clara, direta e compreensível — evitar juridiquês excessivo
- Atualizar a política sempre que houver mudança relevante no tratamento de dados

**Referência legal:** [Art. 9º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art9) — o titular tem direito à informação clara sobre o tratamento.

---

### 1.3 Consentimento em formulários

Todo formulário que coleta [dados pessoais](https://pt.wikipedia.org/wiki/Dado_pessoal) (cadastro, contato, newsletter, orçamento) precisa registrar o consentimento do usuário de forma explícita.

**O que fazer:**

- Adicionar checkbox de consentimento em todos os formulários — não pode vir pré-marcado
- O texto do checkbox deve informar a finalidade da coleta e conter link para a política de privacidade
- Registrar o consentimento com timestamp e versão da política vigente
- Não condicionar o uso do serviço ao fornecimento de dados desnecessários (princípio da minimização)

**Referência legal:** [Art. 7º, I](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art7) e [Art. 8º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art8) — o consentimento deve ser destacado das demais cláusulas.

---

### 1.4 Canal de atendimento ao titular no site

O titular de dados tem o direito de solicitar acesso, correção, exclusão e [portabilidade](https://pt.wikipedia.org/wiki/Portabilidade_de_dados) de seus dados a qualquer momento.

**O que fazer:**

- Disponibilizar no site um canal claro para solicitações de titulares (formulário, e-mail dedicado ou chat)
- Estabelecer prazo de resposta interno (a LGPD não define prazo fixo, mas a prática de mercado é até 15 dias úteis)
- Criar processo interno para triagem, análise e resposta das solicitações
- Documentar todas as solicitações recebidas e as respostas fornecidas

**Referência legal:** [Art. 18º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art18) — direitos do titular de dados.

---

## 2. A empresa possui um DPO (Encarregado de Proteção de Dados) nomeado?

O DPO — [Data Protection Officer](https://www.gov.br/cidadania/pt-br/acesso-a-informacao/institucional/anpd), ou Encarregado — é a pessoa responsável por atuar como canal entre a empresa, os titulares de dados e a ANPD. A nomeação é obrigatória para controladores de dados.

- **Se já possui DPO nomeado e com contato publicado:** pular para a etapa 3.
- **Se não possui:** seguir os itens 2.1 a 2.3 abaixo.

---

### 2.1 O que é um DPO e quem pode exercer essa função?

O DPO não precisa ter formação específica em direito ou TI — o que importa é o conhecimento sobre proteção de dados e capacidade de interlocução com a ANPD e com os titulares.

**Pode ser:**

- Um colaborador interno designado formalmente (gerente de TI, jurídico, compliance)
- Um profissional externo contratado como DPO as a Service
- Uma empresa especializada em privacidade de dados prestando o serviço

**Onde encontrar um DPO externo:**

- Consultorias especializadas em LGPD e privacidade (ex: escritórios de advocacia com área de dados, consultorias de compliance)
- Plataformas de DPO as a Service disponíveis no mercado brasileiro
- Associações do setor como IAPP Brasil e ANPPD

---

### 2.2 Como nomear e formalizar o DPO

A nomeação precisa ser formal e o contato do DPO deve ser publicado de forma acessível.

**O que fazer:**

- Emitir um documento interno de nomeação (portaria, ata ou contrato) formalizando o DPO
- Se for colaborador interno, definir a função em seu cargo com as responsabilidades descritas
- Se for externo, formalizar contrato de prestação de serviço com escopo de atuação definido
- Publicar o nome e canal de contato do DPO na página de política de privacidade do site
- Registrar o DPO no [portal da ANPD](https://www.gov.br/cidadania/pt-br/acesso-a-informacao/institucional/anpd) quando exigido (verificar obrigatoriedade conforme porte da empresa)

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Nomeacao do DPO/` para ver modelos de documento de nomeação e termo de responsabilidade.

**Referência legal:** [Art. 41º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art41) — a indicação do encarregado e seu contato devem ser divulgados publicamente.

---

### 2.3 Responsabilidades do DPO

Após a nomeação, o DPO precisa estar operacionalmente ativo.

**Atribuições mínimas:**

- Receber e responder solicitações de titulares de dados
- Orientar colaboradores e a empresa sobre boas práticas de proteção de dados
- Atuar como canal de comunicação com a ANPD em caso de incidentes ou consultas
- Conduzir ou supervisionar auditorias e revisões de conformidade internas
- Manter-se atualizado sobre mudanças na legislação e nas orientações da ANPD

---

## 3. A empresa sabe quais dados pessoais coleta, onde estão armazenados e por quê?

O mapeamento de dados — também chamado de inventário ou data mapping — é a espinha dorsal de qualquer programa de governança de dados. Sem saber o que se tem, não é possível proteger nem justificar o tratamento.

- **Se já existe um inventário atualizado:** pular para a etapa 4.
- **Se não existe:** seguir os itens 3.1 a 3.3 abaixo.

---

### 3.1 Como criar o inventário de dados (data mapping)

**O que fazer:**

- Mapear todos os pontos de coleta de dados pessoais: formulários, sistemas, planilhas, e-mails, contratos, atendimentos
- Para cada conjunto de dados, registrar:
  - Quais dados são coletados (nome, CPF, e-mail, dados bancários, etc.)
  - Qual a finalidade do tratamento
  - Qual a base legal utilizada
  - Onde os dados estão armazenados (servidor, nuvem, planilha local, etc.)
  - Quem tem acesso (departamento, cargo, fornecedor)
  - Por quanto tempo são retidos
  - Se são compartilhados com terceiros e com quem
- Registrar o inventário em documento formal (planilha estruturada ou ferramenta de GRC)
- Revisar o inventário ao menos uma vez por ano ou sempre que houver novo processo de coleta

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Inventario de Dados/` para ver modelos prontos de planilha de inventário com estrutura LGPD-compliant.

---

### 3.2 Definir a base legal para cada tratamento

A LGPD exige que todo tratamento de [dado pessoal](https://pt.wikipedia.org/wiki/Dado_pessoal) tenha uma base legal definida. Não basta coletar com "boa intenção".

**As principais bases legais ([Art. 7º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art7)):**

| Base Legal | Quando usar |
|---|---|
| Consentimento | Quando o titular opta por receber comunicações, newsletters, etc. |
| Contrato | Dados necessários para execução de um contrato com o titular |
| Legítimo interesse | Finalidades legítimas da empresa, desde que não prejudiquem o titular |
| Obrigação legal | Dados exigidos por lei (ex: dados fiscais, trabalhistas) |
| Proteção da vida | Situações de emergência envolvendo risco à vida |

**O que fazer:**

- Para cada categoria de dado no inventário, definir e documentar a base legal aplicável
- Evitar usar "consentimento" como base padrão para tudo — em muitos casos, contrato ou obrigação legal é mais adequado e mais robusto juridicamente
- Revisar a base legal sempre que a finalidade do tratamento mudar

---

### 3.3 Política de retenção e descarte de dados

Guardar dados indefinidamente é um risco. A LGPD exige que os dados sejam mantidos apenas pelo tempo necessário à finalidade.

**O que fazer:**

- Definir prazos de retenção por categoria de dado (ex: dados de clientes por 5 anos após encerramento do contrato, currículos por 6 meses)
- Documentar os prazos em uma política formal de retenção de dados
- Criar rotina periódica de descarte seguro — exclusão definitiva ou [anonimização](https://pt.wikipedia.org/wiki/Anonimiza%C3%A7%C3%A3o) dos dados fora do prazo
- Garantir que o descarte de dados em mídias físicas (HDs, pendrives, documentos impressos) seja feito de forma segura e rastreável

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Retencao e Descarte de Dados/` para ver templates de política de retenção e guia de procedimentos de descarte seguro.

---

### 3.4 Controle sobre compartilhamento de dados com terceiros

A empresa compartilha dados pessoais sempre que utiliza fornecedores, plataformas, parceiros ou prestadores de serviço que têm acesso a esses dados — mesmo que indiretamente. Pela LGPD, a empresa continua responsável pelo tratamento mesmo quando o dado está nas mãos de um terceiro (operador).

**O que fazer:**

- Mapear todos os terceiros que têm acesso a dados pessoais da empresa: plataformas de e-mail marketing, CRMs, ERPs, contabilidades, escritórios jurídicos, agências, provedores de nuvem, etc.
- Para cada terceiro, registrar:
  - Quais dados são compartilhados
  - Qual a finalidade do compartilhamento
  - Onde os dados ficam armazenados (país/região — atenção para transferências internacionais)
  - Qual o prazo de retenção pelo terceiro
- Incluir cláusulas de proteção de dados ([DPA — Data Processing Agreement](https://en.wikipedia.org/wiki/Data_processing_agreement)) em todos os contratos com fornecedores que tratam dados pessoais
- Garantir que os terceiros possuam políticas de segurança compatíveis com os requisitos da LGPD
- Revisar a lista de terceiros ao menos uma vez por ano ou sempre que houver mudança de fornecedor

**📁 Exemplo prático:** Consulte a pasta `/exemplos/DPA/` para ver modelos de Data Processing Agreement e lista de verificação de conformidade com fornecedores.

**Referência legal:** [Art. 39º](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art39) — o operador deve realizar o tratamento segundo as instruções fornecidas pelo controlador. [Art. 42º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art42) — o operador responde solidariamente pelos danos causados quando descumprir as obrigações da LGPD.

---

## 4. A empresa possui controles de acesso a sistemas e dados pessoais?

Acesso irrestrito a dados pessoais é um dos principais vetores de risco — tanto para vazamentos acidentais quanto para ataques internos.

- **Se já existem controles formais de acesso:** pular para a etapa 5.
- **Se não existem ou são informais:** seguir os itens 4.1 e 4.2 abaixo.

---

### 4.1 Implementar controle de acesso por perfil (least privilege)

**O que fazer:**

- Mapear todos os sistemas que armazenam dados pessoais
- Definir perfis de acesso por função (ex: analista acessa apenas dados do seu departamento, gestor acessa relatórios agregados)
- Aplicar o princípio do [menor privilégio](https://pt.wikipedia.org/wiki/Princ%C3%ADpio_do_menor_privil%C3%A9gio): cada colaborador acessa apenas o que precisa para sua função
- Registrar logs de acesso a sistemas sensíveis (quem acessou, quando, o quê)
- Criar processo formal de concessão, revisão e revogação de acessos — especialmente em casos de desligamento

---

### 4.2 Gestão de senhas e autenticação

**O que fazer:**

- Exigir senhas fortes e únicas para sistemas com dados pessoais
- Implementar autenticação de dois fatores (2FA) em sistemas críticos
- Proibir o compartilhamento de credenciais entre colaboradores
- Definir política de troca periódica de senhas e bloqueio após tentativas malsucedidas

---

## 5. A empresa possui plano de resposta a incidentes de segurança?

Vazamentos de dados são uma realidade. A LGPD exige que incidentes que possam causar risco ou dano aos titulares sejam comunicados à ANPD e aos titulares afetados em prazo razoável — o mercado trabalha com até 72 horas para notificação inicial.

- **Se já existe um plano formal de resposta a incidentes:** pular para a etapa 6.
- **Se não existe:** seguir o item 5.1 abaixo.

---

### 5.1 Criar o plano de resposta a incidentes (Playbook)

**O que fazer:**

- Definir o que caracteriza um incidente de dados na empresa (acesso não autorizado, vazamento, perda de dispositivo, etc.)
- Estabelecer um fluxo claro de resposta com responsáveis em cada etapa:
  1. Detecção e contenção do incidente
  2. Avaliação do impacto (quais dados, quantos titulares afetados)
  3. Notificação interna ao DPO e à liderança
  4. Comunicação à [ANPD](https://www.gov.br/cidadania/pt-br/acesso-a-informacao/institucional/anpd) (quando obrigatório)
  5. Comunicação aos titulares afetados (quando necessário)
  6. Registro e análise pós-incidente
- Testar o plano ao menos uma vez por ano com simulações internas
- Documentar todos os incidentes ocorridos, mesmo os de baixo impacto

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Resposta a Incidentes/` para ver fluxograma de resposta e templates de comunicação com titulares e ANPD.

**Referência legal:** [Art. 48º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art48) — o controlador deve comunicar à ANPD e ao titular a ocorrência de incidente que possa acarretar risco ou dano relevante.

---

## 6. Os colaboradores foram treinados sobre LGPD e proteção de dados?

A maior parte dos incidentes de dados tem origem humana — envio de arquivo errado, senhas fracas, phishing. A conscientização é uma camada de proteção indispensável.

- **Se já existe programa de treinamento ativo:** encerrar o diagnóstico e avançar para a fase DO do framework.
- **Se não existe:** seguir o item 6.1 abaixo.

---

### 6.1 Criar programa de conscientização em proteção de dados

**O que fazer:**

- Desenvolver trilha de treinamento obrigatório sobre LGPD para todos os colaboradores — especialmente os que lidam com [dados pessoais](https://pt.wikipedia.org/wiki/Dado_pessoal)
- O treinamento deve cobrir, no mínimo:
  - O que é [dado pessoal](https://pt.wikipedia.org/wiki/Dado_pessoal) e [dado sensível](https://pt.wikipedia.org/wiki/Dados_sens%C3%ADveis)
  - Quais são os [direitos dos titulares](https://pt.wikipedia.org/wiki/GDPR#Direitos_dos_titulares_dos_dados)
  - Como identificar e reportar um incidente de dados
  - Boas práticas de segurança (senhas, e-mails, dispositivos)
- Registrar a participação de cada colaborador com data e versão do treinamento
- Realizar reciclagem mínima anual ou sempre que houver mudança relevante na legislação
- Incluir cláusula de confidencialidade e proteção de dados nos contratos de trabalho e com terceiros

---

*Documento gerado como parte do framework data-trust — fase PLAN / adequação LGPD.*
