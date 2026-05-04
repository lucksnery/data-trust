# Controle de Acessos — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na estruturação e implementação de um programa de controle de acessos dentro da empresa. O escopo é segurança da informação — a [LGPD (Lei Geral de Proteção de Dados)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) aparece como contexto legal aplicável, não como único referencial. Frameworks como [ISO 27001](https://pt.wikipedia.org/wiki/ISO/IEC_27001) (controles A.9 e A.5), [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) e [CIS Controls](https://www.cisecurity.org/cis-controls) 5 e 6 orientam as boas práticas aqui descritas.

O princípio central que guia este documento é o **[Zero Trust](https://en.wikipedia.org/wiki/Zero_trust_security_model)**: nunca confie, sempre verifique. Em vez de presumir que tudo dentro do perímetro corporativo é seguro, o modelo Zero Trust trata cada acesso — independentemente de origem, dispositivo ou usuário — como potencialmente não confiável até que seja verificado. Esse paradigma é especialmente relevante em ambientes com trabalho remoto, uso de cloud e múltiplos fornecedores com acesso a sistemas internos.

A abordagem é sequencial: cada etapa começa com um diagnóstico e direciona para ações práticas de adequação.

---

## 1. A empresa sabe quem acessa o quê?

O primeiro passo é entender se existe qualquer tipo de controle sobre quem pode acessar dados, sistemas e ambientes — seja em plataformas digitais, arquivos, planilhas ou espaços físicos.

- **Se não existe controle formal:** seguir os itens 1.1 a 1.4.
- **Se existe, mas é informal ou não documentado:** revisar os itens abaixo.
- **Se existe controle estruturado e documentado:** avançar para a etapa 2.

---

### 1.1 Mapeamento de acessos

Não é possível proteger o que não se conhece. Antes de controlar acessos, é necessário mapear quem acessa o quê — em sistemas, arquivos, ambientes físicos e integrações entre sistemas.

**O que fazer:**

- Identificar todos os sistemas, pastas, bancos de dados, ambientes cloud e arquivos que contenham dados sensíveis ou críticos para a operação
- Listar todos os usuários com acesso a esses dados: colaboradores internos, terceiros, fornecedores e contas de serviço
- Para cada acesso, documentar:
  - Qual usuário ou sistema acessa quais dados ou ambientes
  - Qual o nível de acesso (leitura, edição, exclusão, administração)
  - Qual a justificativa do acesso (função exercida ou integração necessária)
  - Se o acesso é permanente ou temporário
- Consolidar essas informações em uma Matriz de Controle de Acessos

**Ferramentas que auxiliam no mapeamento:**

| Ferramenta | Tipo | Para que serve |
|---|---|---|
| Netwrix Auditor | Pago | Auditoria de acessos em [AD](https://pt.wikipedia.org/wiki/Active_Directory), arquivos e sistemas |
| SolarWinds Access Rights Manager | Pago | Mapeamento e auditoria de permissões em ambientes Windows |
| ManageEngine ADManager Plus | Pago | Gestão e auditoria de acessos no [Active Directory](https://pt.wikipedia.org/wiki/Active_Directory) |
| Google Workspace Admin | Nativo | Mapeamento de acessos em ambientes Google |
| Microsoft Entra ID (Azure AD) | Nativo/Pago | Mapeamento e gestão de identidades em ambientes Microsoft |

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Controle de Acessos/` para ver modelo de Matriz de Controle de Acessos com estrutura pronta para preenchimento.

---

### 1.2 Definição de perfis de acesso — RBAC

Acesso genérico é acesso excessivo. O modelo [RBAC (Role-Based Access Control)](https://pt.wikipedia.org/wiki/Controle_de_acesso_baseado_em_fun%C3%A7%C3%A3o) organiza permissões por função — não por pessoa. Cada cargo ou perfil tem um conjunto fixo de permissões, e o colaborador herda as permissões do seu perfil.

**O que fazer:**

- Definir os perfis de acesso da empresa com base nas funções existentes
- Vincular cada perfil a permissões específicas e documentadas
- Evitar acessos individuais diretos — toda concessão de acesso deve passar por um perfil
- Garantir que novos colaboradores sejam associados a um perfil no onboarding, nunca recebam permissões avulsas

**Exemplo de estrutura de perfis:**

| Perfil | Acesso permitido | Acesso proibido |
|---|---|---|
| Financeiro | Sistemas financeiros, relatórios contábeis, dados de faturamento | Dados de RH, sistemas de TI, dados de clientes além do necessário |
| RH | Dados de colaboradores, folha de pagamento, sistemas de recrutamento | Sistemas financeiros, dados de clientes, acesso administrativo |
| Marketing | CRM (dados de leads e clientes para campanhas), plataformas de mídia | Dados financeiros, dados de RH, sistemas internos de TI |
| TI — Suporte | Sistemas de helpdesk, acesso remoto a estações de trabalho | Bancos de dados de produção, sistemas financeiros, dados de RH |
| TI — Administrador | Acesso privilegiado a sistemas críticos (ver seção 3) | Sem restrição técnica — requer controles adicionais de PAM |
| Terceiro / Fornecedor | Apenas o sistema ou dado específico para o qual foi contratado | Todos os demais ambientes |

**Referência:** ISO 27001 — Controle A.9.2 (Gestão de acesso de usuários), CIS Control 5.

---

### 1.3 Princípio do menor privilégio

Cada usuário, sistema ou serviço deve ter acesso apenas ao mínimo necessário para executar sua função — nada além disso. Permissões excessivas aumentam a superfície de ataque: se uma conta for comprometida, o dano se limita ao que aquela conta pode acessar.

**O que fazer:**

- Revisar acessos existentes e remover permissões que não têm justificativa ativa
- Questionar ativamente: esse colaborador realmente precisa desse acesso para trabalhar?
- Dados de categorias sensíveis — saúde, biometria, financeiro, dados de menores — devem ter acesso ainda mais restrito, com aprovação formal do gestor
- Implementar política formal de menor privilégio, revisada a cada 6 meses (ver etapa 5)

**Referência:** ISO 27001 — Controle A.9.2.3, NIST SP 800-53 — AC-6, LGPD Art. 6º, III (princípio da necessidade).

---

### 1.4 Controle de acesso físico

Controle de acessos não é só digital. Salas de servidores, armários de equipamentos, áreas restritas de operação e impressoras com dados sensíveis fazem parte do escopo e exigem controle equivalente.

**O que fazer:**

- Mapear todos os espaços físicos que contêm equipamentos, documentos ou infraestrutura crítica
- Implementar controle de entrada com crachá, [biometria](https://pt.wikipedia.org/wiki/Biometria) ou PIN para áreas restritas
- Manter registro de entrada e saída em áreas sensíveis (log físico ou eletrônico)
- Restringir o acesso à sala de servidores apenas ao time de TI autorizado — nunca acesso irrestrito a toda a equipe técnica
- Garantir que visitantes e terceiros sejam sempre acompanhados em áreas restritas
- Impressoras e dispositivos multifuncionais com armazenamento interno devem ter acesso controlado e rotina de limpeza de dados

**Referência:** ISO 27001 — Controles A.11.1 e A.11.2.

---

## 2. A empresa possui autenticação segura?

Ter perfis de acesso definidos não é suficiente se a autenticação for fraca. Uma credencial comprometida com autenticação simples anula qualquer controle de permissões.

- **Se não há políticas de autenticação:** seguir os itens 2.1 a 2.4.
- **Se há, mas são básicas:** revisar e fortalecer.
- **Se são robustas e documentadas:** avançar para a etapa 3.

---

### 2.1 Política de senhas

Senhas fracas ou reutilizadas são a causa de uma parcela significativa dos acessos não autorizados. A política de senhas define os requisitos mínimos e as proibições.

**O que exigir:**

- Comprimento mínimo de 12 caracteres — quanto mais longa, mais segura
- Combinação de letras maiúsculas, minúsculas, números e símbolos
- Proibição de reutilização das últimas 5 senhas
- Bloqueio temporário após 5 tentativas inválidas consecutivas
- Proibição explícita de compartilhamento de credenciais entre colaboradores
- Senhas com dados óbvios (nome, data de nascimento, nome da empresa + ano) devem ser rejeitadas

**Gerenciadores de senhas recomendados para o ambiente corporativo:**

| Ferramenta | Destaque | Modelo |
|---|---|---|
| Bitwarden | Open source, plano corporativo acessível, auditável | Pago (plano gratuito disponível) |
| 1Password Business | Interface robusta, relatórios de segurança, integração com SSO | Pago |
| Keeper Security | Forte em auditoria e relatórios de conformidade | Pago |
| Dashlane Business | Boa experiência para usuários finais, painel centralizado | Pago |

---

### 2.2 Autenticação multifator (MFA/2FA)

Senha sozinha não é suficiente para sistemas com dados sensíveis ou acesso remoto. O segundo fator garante que mesmo com a senha comprometida, o acesso não seja possível sem o segundo elemento de verificação.

**Onde ativar obrigatoriamente:**

- E-mail corporativo
- [VPN](https://pt.wikipedia.org/wiki/Red_privada_virtual) e acesso remoto
- Sistemas com dados pessoais ou financeiros
- Painel de administração de qualquer plataforma
- Ambientes cloud (AWS, Azure, GCP, Google Workspace, Microsoft 365)
- Repositórios de código (GitHub, GitLab, Bitbucket)

**Métodos de MFA — do mais seguro ao menos seguro:**

| Método | Segurança | Observação |
|---|---|---|
| Chave de segurança física (YubiKey, Titan Key) | Muito alta | Resistente a [phishing](https://pt.wikipedia.org/wiki/Phishing); recomendado para acessos críticos |
| Aplicativo autenticador (Google Authenticator, Microsoft Authenticator, Authy) | Alta | Padrão recomendado para a maioria dos casos |
| Push notification (Duo, Microsoft Authenticator) | Alta | Conveniente, mas vulnerável a fadiga de [MFA (push bombing)](https://en.wikipedia.org/wiki/Fatigue_attack) |
| SMS / ligação telefônica | Baixa | Evitar — vulnerável a [SIM swapping](https://pt.wikipedia.org/wiki/SIM_swap_scam) |

**Referência:** ISO 27001 — Controle A.9.4.2, LGPD Art. 46º (medidas técnicas de segurança).

---

### 2.3 Gestão centralizada de identidades (IAM / IdP)

Em ambientes com múltiplos sistemas, cada um com sua própria gestão de usuários, o controle fragmentado é inviável. Uma plataforma de [Identity and Access Management (IAM)](https://pt.wikipedia.org/wiki/Identity_and_access_management) centraliza a criação, gestão e revogação de identidades, e um Identity Provider (IdP) permite que o colaborador acesse todos os sistemas com uma única identidade verificada — conceito conhecido como [Single Sign-On (SSO)](https://pt.wikipedia.org/wiki/Single_sign-on).

**Por que isso importa:**

- Com SSO, o colaborador tem uma única credencial para todos os sistemas — e o time de TI tem um único ponto de controle e revogação
- Quando um colaborador é desligado, basta desativar a conta no IdP — o acesso a todos os sistemas integrados é revogado automaticamente
- Facilita a aplicação de MFA de forma centralizada, sem depender de cada sistema configurar individualmente

**Principais plataformas de IAM/IdP:**

| Plataforma | Contexto ideal | Modelo |
|---|---|---|
| Microsoft Entra ID (Azure AD) | Empresas no ecossistema Microsoft 365 | Pago (incluído em planos M365) |
| Google Workspace | Empresas no ecossistema Google | Pago (incluído no Workspace) |
| Okta | Ambientes híbridos, múltiplos sistemas e fornecedores | Pago |
| JumpCloud | PMEs que precisam de IAM sem ecossistema Microsoft ou Google | Pago (plano gratuito limitado) |
| Keycloak | Open source, para empresas com capacidade técnica interna | Gratuito |

---

### 2.4 Gestão do ciclo de vida de credenciais

O ciclo de vida de uma credencial começa no onboarding e termina no offboarding — e precisa ser controlado em cada etapa.

**Onboarding — criação de acesso:**

- O acesso deve ser solicitado formalmente pelo gestor antes do primeiro dia
- A conta deve ser criada com o perfil correto (ver item 1.2) — nunca com acesso total provisório
- O colaborador deve receber as credenciais por canal seguro e redefinir a senha no primeiro acesso
- MFA deve ser ativado antes do primeiro acesso a sistemas críticos

**Movimentações internas — mudança de função ou área:**

- Ao mudar de cargo ou área, os acessos do perfil anterior devem ser revogados imediatamente
- Novos acessos devem ser concedidos com base no novo perfil — nunca acumulando os anteriores
- O processo deve ser iniciado pelo RH e validado pelo TI antes da data de mudança

**Offboarding — desligamento:**

- No momento do desligamento, todos os acessos devem ser revogados no mesmo dia — de preferência antes que o colaborador seja comunicado formalmente, quando o desligamento é involuntário
- Checklist mínimo de offboarding:
  - Desativação da conta no IdP (revoga SSO e todos os sistemas integrados)
  - Revogação de acessos em sistemas não integrados ao IdP (verificar manualmente)
  - Bloqueio de e-mail corporativo e redirecionamento de mensagens
  - Revogação de tokens de API e acessos a repositórios de código
  - Retirada de acessos físicos (crachá, biometria)
  - Recuperação de equipamentos corporativos
  - Transferência de arquivos e dados do colaborador para o gestor

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Controle de Acessos/` para ver checklist de offboarding completo em formato editável.

---

## 3. A empresa controla acessos privilegiados?

Contas privilegiadas — administradores de sistemas, contas root, contas de serviço e acessos de emergência — são os alvos mais críticos em qualquer ambiente. Se comprometidas, o dano pode ser total. O gerenciamento de acessos privilegiados (PAM — Privileged Access Management) é uma disciplina própria dentro do controle de acessos e exige atenção separada.

- **Se não há controle específico sobre contas privilegiadas:** seguir os itens 3.1 a 3.3.
- **Se há controles básicos:** revisar e formalizar.
- **Se há PAM estruturado:** avançar para a etapa 4.

---

### 3.1 Inventário de contas privilegiadas

**O que fazer:**

- Listar todas as contas com privilégios administrativos em todos os sistemas: servidores, bancos de dados, plataformas cloud, roteadores, firewalls, sistemas de RH e financeiro
- Incluir no inventário:
  - Contas de administrador de domínio (Domain Admin)
  - Contas root em servidores Linux
  - Contas de administrador local em estações de trabalho
  - Contas de serviço usadas por sistemas e automações
  - Contas de emergência (break-glass accounts)
  - Credenciais de APIs e integrações entre sistemas
- Verificar se há contas privilegiadas compartilhadas — se houver, individualizar imediatamente

---

### 3.2 Boas práticas para contas privilegiadas

**O que fazer:**

- Administradores devem ter duas contas separadas: uma conta comum para uso cotidiano (e-mail, navegação) e uma conta privilegiada exclusivamente para tarefas administrativas
- A conta privilegiada não deve ser usada para acesso a e-mail, navegação ou qualquer atividade não administrativa
- [MFA](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o_multifatorial) obrigatório para todas as contas privilegiadas — sem exceção
- Acessos privilegiados devem ser concedidos de forma temporária ([Just-in-Time](https://en.wikipedia.org/wiki/Just-in-time_access)) quando possível: o administrador solicita o acesso, executa a tarefa, e o acesso expira automaticamente
- Senhas de contas privilegiadas devem ser rotacionadas periodicamente e armazenadas em cofre de senhas seguro

---

### 3.3 Ferramentas de PAM

| Ferramenta | Destaque | Modelo |
|---|---|---|
| CyberArk | Referência de mercado para grandes empresas, cofre de credenciais + gravação de sessão | Pago |
| BeyondTrust | [PAM](https://en.wikipedia.org/wiki/Privileged_access_management) completo com acesso remoto seguro integrado | Pago |
| Delinea (ex-Thycotic) | Boa relação custo-benefício para PMEs | Pago |
| HashiCorp Vault | Open source, forte para gestão de secrets e credenciais de API | Gratuito / Pago (Enterprise) |
| Teleport | PAM para ambientes cloud-native e DevOps | Gratuito / Pago |

---

## 4. A empresa monitora e audita os acessos realizados?

Controlar quem tem acesso é necessário — mas sem monitoramento, não há visibilidade sobre o que está sendo feito com esse acesso. Acessos abusivos, exfiltração de dados e movimentações laterais em um ataque muitas vezes só são detectados com análise de logs.

- **Se não há monitoramento:** seguir os itens 4.1 e 4.2.
- **Se há:** validar cobertura, qualidade e periodicidade da análise.

---

### 4.1 Registro de logs de acesso

**O que registrar:**

- Usuário que realizou a ação
- Data, hora e origem (IP ou dispositivo)
- Sistema ou recurso acessado
- Ação realizada: visualização, criação, edição, exclusão, exportação, download
- Resultado: acesso permitido ou negado

**Onde ativar logs obrigatoriamente:**

- Sistemas com dados pessoais ou financeiros
- Active Directory / IdP (logins, criação e alteração de contas, mudanças de permissão)
- Ambientes cloud (AWS CloudTrail, Azure Monitor, Google Cloud Audit Logs)
- VPN e acesso remoto
- Servidores de arquivos e repositórios de documentos
- Bancos de dados de produção

**Requisitos de integridade dos logs:**

- Logs devem ser protegidos contra alteração — armazenados em local separado dos sistemas que os geram
- Período de retenção mínimo recomendado: 12 meses
- Acesso aos logs deve ser restrito ao time de segurança e auditoria

---

### 4.2 Monitoramento e auditoria de acessos

Registrar não basta — é preciso analisar. Um log que nunca é lido não detecta nada.

**O que monitorar ativamente:**

- Acessos fora do horário padrão de trabalho
- Tentativas de acesso negado repetidas (possível tentativa de força bruta)
- Volume anormal de downloads, consultas ou exportações de dados
- Acessos a dados de classificação restrita ou confidencial
- Logins de localizações geográficas incomuns ou simultâneos de locais diferentes
- Criação ou alteração de contas privilegiadas
- Desativação ou alteração de configurações de log

**Ferramentas de monitoramento e SIEM:**

| Ferramenta | Tipo | Destaque |
|---|---|---|
| Microsoft Sentinel | [SIEM](https://pt.wikipedia.org/wiki/SIEM) cloud | Integrado ao ecossistema Microsoft, boa cobertura para M365 e Azure |
| Splunk | SIEM | Referência de mercado, altamente customizável |
| IBM QRadar | SIEM | Forte em correlação de eventos e ambientes complexos |
| Elastic Security (ELK Stack) | Open source | Customizável, exige capacidade técnica interna |
| Wazuh | Open source | SIEM + [EDR](https://en.wikipedia.org/wiki/Endpoint_detection_and_response) open source, boa opção para PMEs com equipe técnica |
| Datadog Security | SaaS | Forte para ambientes cloud-native e DevOps |

**Referência:** ISO 27001 — Controle A.12.4, LGPD Art. 46º e Art. 48º.

---

## 5. A empresa revisa os acessos periodicamente?

Acessos acumulam com o tempo. Colaboradores mudam de função, projetos encerram, fornecedores deixam de prestar serviço — mas os acessos raramente são revogados com a mesma agilidade com que são concedidos. A revisão periódica corrige essa deriva.

- **Se não há revisão periódica:** seguir o item 5.1.
- **Se há:** validar frequência e formalização.

---

### 5.1 Revisão periódica de acessos (Access Review)

**O que fazer:**

- Realizar revisão formal de acessos ao menos a cada 6 meses — ambientes críticos merecem revisão trimestral
- O processo deve envolver os gestores de cada área, que validam se cada colaborador da sua equipe ainda precisa dos acessos que possui
- Para cada acesso, a decisão deve ser: manter, reduzir ou revogar — com justificativa documentada
- Acessos sem justificativa ativa devem ser revogados imediatamente, sem exceção
- Contas inativas (sem login há mais de 30 ou 60 dias, conforme política interna) devem ser bloqueadas e investigadas antes de qualquer reativação
- Toda revisão deve ser documentada com data, responsável e resultado

**Referência:** ISO 27001 — Controle A.9.2.5, CIS Control 5.3.

---

## 6. A empresa controla os acessos de terceiros e sistemas integrados?

Fornecedores, parceiros e sistemas integrados são vetores reais de risco. Um ataque que começa em um fornecedor com acesso à sua rede pode comprometer dados internos sem que nenhum colaborador interno seja o ponto de entrada.

- **Se terceiros têm acesso a sistemas ou dados:** seguir os itens 6.1 a 6.3.
- **Se não têm:** validar periodicamente se essa situação se mantém.

---

### 6.1 Controle de acesso para terceiros

**O que fazer:**

- Conceder acesso apenas ao recurso estritamente necessário para a execução do serviço contratado — nunca acesso amplo ao ambiente
- Criar contas individuais e nominais para cada terceiro — nunca compartilhadas entre fornecedores ou entre um fornecedor e colaboradores internos
- Definir prazo de validade para todos os acessos de terceiros — acesso temporário, com data de expiração automática quando possível
- Exigir MFA para terceiros que acessam sistemas com dados sensíais
- Monitorar as atividades realizadas por terceiros com o mesmo rigor aplicado a colaboradores internos
- Revogar todos os acessos imediatamente ao encerramento do contrato

---

### 6.2 Contas de serviço e integrações entre sistemas

Contas de serviço são credenciais usadas por sistemas, scripts ou automações para se comunicar com outros sistemas — e são frequentemente negligenciadas nos processos de controle de acesso. São alvos valiosos em ataques porque raramente têm MFA e muitas vezes têm permissões amplas.

**O que fazer:**

- Inventariar todas as contas de serviço e credenciais de integração existentes (APIs, tokens, service accounts)
- Aplicar o princípio do menor privilégio também para contas de serviço — cada integração acessa apenas o que precisa
- Nunca usar credenciais de usuários humanos para automações ou integrações — sempre contas dedicadas
- Armazenar tokens e secrets em cofre de senhas ou sistema de gestão de secrets (ex: HashiCorp Vault, AWS Secrets Manager, Azure Key Vault) — nunca em código-fonte ou planilhas
- Rotacionar credenciais de serviço periodicamente e sempre que houver mudança de fornecedor ou colaborador com acesso

---

### 6.3 Cláusulas contratuais de acesso

**O que incluir nos contratos com fornecedores que acessam sistemas ou dados:**

- Cláusula de confidencialidade e sigilo sobre dados acessados
- Obrigação de adotar medidas de segurança compatíveis com as exigidas pela empresa
- Responsabilidade por incidentes causados por uso indevido de acesso concedido
- Obrigação de comunicar ao contratante qualquer incidente de segurança que envolva os acessos concedidos
- Direito da empresa de auditar os acessos realizados pelo fornecedor

**Referência:** LGPD Art. 39º (o operador deve seguir as instruções do controlador), ISO 27001 — Controle A.15.1.

---

## 7. A empresa controla acessos em ambientes cloud?

Ambientes [cloud](https://pt.wikipedia.org/wiki/Computa%C3%A7%C3%A3o_em_nuvem) — AWS, Azure, Google Cloud, plataformas SaaS — têm especificidades próprias no controle de acessos que não se resolvem com as mesmas ferramentas e processos usados em ambientes on-premise. Permissões mal configuradas em cloud são uma das causas mais comuns de exposição de dados.

- **Se a empresa usa serviços cloud:** seguir os itens 7.1 e 7.2.
- **Se não usa:** ignorar esta etapa e avançar para a etapa 8.

---

### 7.1 Boas práticas de IAM em cloud

**O que fazer:**

- Nunca usar a conta root ou a conta de administrador principal para operações rotineiras — criar contas individuais com permissões específicas para cada pessoa e sistema
- Aplicar o princípio do menor privilégio nas políticas IAM de cada provedor cloud
- Ativar MFA obrigatório para todas as contas com acesso ao console de administração
- Revisar periodicamente as permissões IAM — ambientes cloud acumulam permissões excessivas rapidamente
- Desativar ou excluir usuários e credenciais não utilizados
- Ativar os logs nativos de auditoria de cada provedor:
  - AWS: CloudTrail + AWS Config
  - Azure: Azure Monitor + Microsoft Defender for Cloud
  - Google Cloud: Cloud Audit Logs

---

### 7.2 Controle de acesso em plataformas SaaS

Cada plataforma SaaS usada pela empresa (Salesforce, HubSpot, Notion, Slack, ferramentas de RH, ERP, etc.) representa um ponto de controle de acesso independente — com seus próprios usuários, permissões e logs.

**O que fazer:**

- Manter inventário de todas as plataformas SaaS em uso e os usuários com acesso em cada uma
- Garantir que o provisionamento e desprovisionamento de usuários em plataformas SaaS esteja integrado ao IdP (SSO) quando possível — para que o offboarding revogue automaticamente esses acessos
- Para plataformas não integradas ao SSO, criar processo manual de revisão e revogação de acessos no offboarding
- Revisar periodicamente quais aplicativos terceiros têm permissão de acesso às contas corporativas ([OAuth](https://pt.wikipedia.org/wiki/OAuth) apps) — revogar os que não são mais usados ou não têm justificativa

---

## 8. Existe política formal de controle de acessos?

Sem formalização, o processo não é sustentável. Boas práticas aplicadas de forma informal dependem de pessoas — e pessoas mudam. A política formaliza o processo, define responsabilidades e garante continuidade.

- **Se não existe política formal:** seguir o item 8.1.
- **Se existe:** revisar e atualizar ao menos anualmente.

---

### 8.1 Criação da política de controle de acessos

**O que a política deve conter:**

- Princípios orientadores: [menor privilégio](https://en.wikipedia.org/wiki/Principle_of_least_privilege), [Zero Trust](https://en.wikipedia.org/wiki/Zero_trust_security_model), [separação de funções](https://en.wikipedia.org/wiki/Separation_of_duties)
- Regras de concessão de acesso: quem pode solicitar, quem aprova, prazo de atendimento
- Critérios de autenticação: requisitos de senha e MFA por tipo de sistema
- Regras para contas privilegiadas: dupla conta, Just-in-Time, cofre de credenciais
- Regras para terceiros e contas de serviço
- Processo de revisão periódica de acessos: frequência, responsáveis, documentação
- Monitoramento e auditoria: o que é registrado, por quanto tempo, quem analisa
- Processo de offboarding: prazo, checklist, responsáveis
- Penalidades em caso de violação da política

**O que fazer após criar a política:**

- Apresentar e comunicar a todos os colaboradores
- Integrar ao programa de onboarding (ver documento de Cultura e Educação, item 5.1)
- Revisar ao menos uma vez por ano ou sempre que houver mudança relevante no ambiente tecnológico

**Referência:** ISO 27001 — Controle A.9.1, CIS Control 6.

---

## 9. Os colaboradores entendem o papel deles no controle de acessos?

Tecnologia e política sem conscientização não funcionam. Compartilhamento de senhas, concessão informal de acessos e descuido com credenciais são comportamentos que nenhuma ferramenta resolve sozinha.

- **Se não há treinamento específico sobre o tema:** seguir o item 9.1.
- **Se há:** validar periodicidade e aderência ao conteúdo atual.

---

### 9.1 Conscientização sobre controle de acessos

Este tema deve estar integrado ao programa de Cultura e Educação em Segurança da Informação. Consulte o documento correspondente para a estrutura completa de treinamento. Os pontos específicos de controle de acessos a serem cobertos:

- Por que senhas individuais são inegociáveis — o que acontece quando uma credencial compartilhada é comprometida
- Como funciona o MFA e por que ele é necessário mesmo para quem "não tem nada importante para esconder"
- O que fazer ao receber uma solicitação de acesso informal de um colega ou superior
- Como reportar quando suspeitar que uma credencial foi comprometida
- O que é [engenharia social](https://pt.wikipedia.org/wiki/Engenharia_social_(seguran%C3%A7a)) aplicada a acessos: [pretexting](https://en.wikipedia.org/wiki/Pretexting), [shoulder surfing](https://en.wikipedia.org/wiki/Shoulder_surfing_(security)), [tailgating](https://en.wikipedia.org/wiki/Tailgating_(security)) (seguir alguém por uma porta de acesso restrito)
- Responsabilidades do colaborador sobre os acessos que possui: acesso não é propriedade, é concessão temporária vinculada à função

---

### Referências técnicas e legais

| Referência | Aplicação neste documento |
|---|---|
| ISO/IEC 27001:2022 — Controles A.5, A.9, A.11, A.12, A.15 | Framework principal de boas práticas de controle de acessos |
| NIST SP 800-53 — Família AC (Access Control) | Controles técnicos detalhados para ambientes governamentais e corporativos |
| CIS Controls v8 — Controls 5 e 6 | Controles prioritários: gestão de contas e controle de acesso |
| LGPD — Art. 6º III, Art. 39º, Art. 46º, Art. 48º | Contexto legal brasileiro aplicável ao tratamento de dados pessoais |
| NIST Zero Trust Architecture (SP 800-207) | Modelo orientador para ambientes modernos com cloud e trabalho remoto |

---

*Documento gerado como parte do framework data-trust — fase PLAN / controle de acessos.*
