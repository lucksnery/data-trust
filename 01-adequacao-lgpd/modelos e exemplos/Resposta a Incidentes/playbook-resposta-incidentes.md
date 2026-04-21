# Playbook de Resposta a Incidentes de Dados Pessoais

**Empresa:** [Nome da Empresa]
**CNPJ:** [00.000.000/0001-00]
**Responsável:** [Nome do DPO ou responsável]
**Última atualização:** DD de mês de AAAA
**Versão:** 1.0

---

## 1. Objetivo

Este playbook define o fluxo de resposta a incidentes de segurança que envolvam dados pessoais tratados pela empresa, estabelecendo responsáveis, prazos e procedimentos para cada etapa — da detecção à análise pós-incidente.

O objetivo é garantir que a empresa consiga identificar, conter e comunicar incidentes de forma rápida, organizada e em conformidade com a LGPD (Art. 48º).

---

## 2. O que é um incidente de dados pessoais

Um incidente de dados pessoais é qualquer evento — acidental ou intencional — que resulte em:

- **Acesso não autorizado** a dados pessoais por pessoa interna ou externa
- **Vazamento ou exposição** de dados pessoais (publicação indevida, envio para destinatário errado, etc.)
- **Perda ou destruição** de dados pessoais (exclusão acidental, falha de sistema, perda de dispositivo)
- **Alteração indevida** de dados pessoais sem autorização
- **Sequestro de dados** (ransomware ou outros ataques que bloqueiam o acesso)

> **[Instrução de preenchimento]:** Compartilhe esta definição com todos os colaboradores durante os treinamentos. Muitos incidentes não são reportados porque o colaborador não reconhece o evento como um incidente. Exemplos práticos para treinar: enviar planilha com dados de clientes para o e-mail errado, perder notebook com dados, clicar em phishing com acesso a sistemas.

---

## 3. Classificação de incidentes

Nem todo incidente tem o mesmo impacto. Classifique o incidente logo na detecção para dimensionar a resposta:

| Nível | Classificação | Critérios | Exemplo |
|---|---|---|---|
| 🔴 **Alto** | Crítico | Grande volume de dados afetados, dados sensíveis expostos, risco real de dano aos titulares | Vazamento de base de clientes com CPF e dados financeiros |
| 🟡 **Médio** | Moderado | Volume limitado, dados comuns, risco de dano possível mas contido | E-mail com dados de 10 clientes enviado para destinatário errado |
| 🟢 **Baixo** | Leve | Poucos dados, sem exposição externa, sem risco real de dano | Colaborador acessou dado de colega sem necessidade, sem uso indevido |

> **[Instrução de preenchimento]:** A classificação define a urgência da resposta e se há obrigação de notificar a ANPD. Incidentes de nível Alto quase sempre exigem notificação. Incidentes de nível Baixo podem não exigir, mas devem ser registrados internamente.

---

## 4. Equipe de resposta a incidentes

> **[Instrução de preenchimento]:** Preencha com os responsáveis reais da empresa. Em empresas menores, uma mesma pessoa pode acumular mais de um papel. O importante é que todos saibam seu papel antes do incidente acontecer.

| Papel | Responsável | Contato |
|---|---|---|
| **DPO / Encarregado** | [Nome] | [e-mail / telefone] |
| **Responsável de TI / Segurança** | [Nome] | [e-mail / telefone] |
| **Responsável Jurídico** | [Nome ou escritório] | [e-mail / telefone] |
| **Responsável de Comunicação** | [Nome] | [e-mail / telefone] |
| **Liderança / Diretoria** | [Nome] | [e-mail / telefone] |

---

## 5. Fluxo de resposta — passo a passo

### ETAPA 1 — Detecção e reporte inicial

**Prazo:** imediato — assim que o incidente for identificado
**Responsável:** qualquer colaborador que identifique o incidente

**O que fazer:**
- Qualquer colaborador que identifique ou suspeite de um incidente deve reportar imediatamente ao DPO ou ao responsável de TI
- Não tentar resolver sozinho, não apagar evidências e não comunicar externamente sem autorização
- Usar o canal de reporte definido pela empresa: **[e-mail / formulário / telefone — preencher aqui]**
- Registrar o máximo de informações disponíveis no momento: o que aconteceu, quando, quais sistemas ou dados podem estar envolvidos

> **[Instrução de preenchimento]:** Defina e divulgue um canal único e claro para reporte de incidentes. Pode ser um e-mail simples como incidentes@empresa.com.br. O importante é que todos saibam para onde reportar.

---

### ETAPA 2 — Avaliação inicial

**Prazo:** até 2 horas após o reporte
**Responsável:** DPO + Responsável de TI

**O que fazer:**
- Confirmar se o evento é de fato um incidente de dados pessoais
- Classificar o nível do incidente (Alto / Médio / Baixo) conforme tabela da seção 3
- Identificar preliminarmente:
  - Quais dados foram afetados
  - Quantos titulares podem estar envolvidos
  - Se o incidente ainda está em curso ou foi contido
  - Qual a origem provável (ataque externo, erro interno, falha de sistema)
- Acionar os demais membros da equipe de resposta conforme o nível do incidente
- Abrir o Registro de Incidente (seção 8) e iniciar o preenchimento

---

### ETAPA 3 — Contenção

**Prazo:** o mais rápido possível após a avaliação inicial
**Responsável:** Responsável de TI + DPO

**O que fazer:**
- Isolar sistemas afetados para impedir propagação do incidente
- Revogar acessos comprometidos ou suspeitos imediatamente
- Preservar evidências — logs, capturas de tela, e-mails — antes de qualquer alteração no ambiente
- Bloquear o vetor de ataque ou falha identificado
- Garantir que o incidente não está mais em curso antes de avançar para as próximas etapas

> **[Instrução de preenchimento]:** Instrua o time de TI a nunca formatar ou reinstalar sistemas antes de preservar as evidências. As evidências são fundamentais tanto para a análise pós-incidente quanto para eventuais processos legais.

---

### ETAPA 4 — Avaliação de impacto

**Prazo:** até 24 horas após a contenção
**Responsável:** DPO + Jurídico + TI

**O que fazer:**
- Mapear com precisão:
  - Quais dados pessoais foram afetados (categorias e volume)
  - Quantos titulares foram impactados
  - Se há dados sensíveis envolvidos (saúde, financeiros, biometria, etc.)
  - Se os dados foram acessados, copiados, destruídos ou apenas expostos
  - Se há risco real de dano aos titulares (fraude, discriminação, exposição pública)
- Definir se o incidente exige notificação à ANPD e/ou aos titulares
- Documentar toda a avaliação no Registro de Incidente

**Critérios para notificação obrigatória à ANPD:**
- Dados sensíveis afetados
- Grande volume de titulares impactados
- Risco real de dano relevante aos titulares (financeiro, reputacional, físico)
- Exposição pública dos dados

> **[Instrução de preenchimento]:** Em caso de dúvida sobre a obrigatoriedade de notificação, o caminho mais seguro é notificar. A ANPD tende a punir mais a omissão do que a notificação desnecessária.

---

### ETAPA 5 — Notificação à ANPD

**Prazo:** até 72 horas após a ciência do incidente (para notificação preliminar)
**Responsável:** DPO + Jurídico

**O que fazer:**
- Acessar o portal da ANPD e preencher o formulário de comunicação de incidente: [https://www.gov.br/anpd](https://www.gov.br/anpd)
- A notificação preliminar deve conter:
  - Descrição da natureza dos dados afetados
  - Informações sobre os titulares envolvidos
  - Medidas técnicas e de segurança adotadas
  - Riscos relacionados ao incidente
  - Identificação e contato do DPO
- A ANPD pode solicitar informações complementares — manter toda a documentação organizada e acessível
- Guardar protocolo de envio e confirmação da notificação

> **[Instrução de preenchimento]:** O prazo de 72 horas é para a notificação inicial — ela pode ser complementada depois com mais informações. Não espere ter todas as respostas para notificar. A ANPD aceita notificações preliminares.

---

### ETAPA 6 — Comunicação aos titulares afetados

**Prazo:** o mais breve possível após a avaliação de impacto, quando houver risco real de dano
**Responsável:** DPO + Comunicação + Jurídico

**O que fazer:**
- Identificar os titulares afetados e o canal de comunicação disponível (e-mail, telefone, carta)
- A comunicação deve conter:
  - O que aconteceu, de forma clara e sem juridiquês
  - Quais dados foram afetados
  - Quais riscos o titular pode enfrentar
  - O que a empresa está fazendo para resolver
  - O que o titular pode fazer para se proteger
  - Canal de contato para dúvidas (DPO ou suporte)
- Não minimizar o incidente nem omitir informações relevantes para a proteção do titular
- Registrar quem foi comunicado, quando e por qual canal

> **[Instrução de preenchimento]:** A linguagem da comunicação ao titular deve ser humana e direta. Evite termos técnicos e jurídicos. O titular precisa entender o que aconteceu e o que fazer — não precisa entender os detalhes técnicos do incidente.

---

### ETAPA 7 — Erradicação e recuperação

**Prazo:** conforme cronograma definido pela equipe de TI
**Responsável:** TI + DPO

**O que fazer:**
- Remover a causa raiz do incidente do ambiente (malware, acesso indevido, vulnerabilidade explorada)
- Restaurar sistemas e dados a partir de backups íntegros, quando necessário
- Validar que o ambiente está seguro antes de retomar operações normais
- Implementar controles adicionais para evitar recorrência imediata
- Documentar todas as ações técnicas realizadas

---

### ETAPA 8 — Análise pós-incidente

**Prazo:** até 15 dias após a resolução do incidente
**Responsável:** DPO + TI + Liderança

**O que fazer:**
- Realizar reunião de análise com todos os envolvidos na resposta
- Responder às seguintes perguntas:
  - O que causou o incidente?
  - O fluxo de resposta funcionou conforme planejado?
  - Os prazos foram cumpridos?
  - O que pode ser melhorado no processo de resposta?
  - Que controles ou treinamentos precisam ser implementados para evitar recorrência?
- Documentar as conclusões e as ações de melhoria com responsáveis e prazos
- Atualizar este playbook se necessário

---

## 6. Resumo de prazos

| Etapa | Prazo | Responsável |
|---|---|---|
| Reporte inicial | Imediato | Qualquer colaborador |
| Avaliação inicial | Até 2 horas | DPO + TI |
| Contenção | O mais rápido possível | TI + DPO |
| Avaliação de impacto | Até 24 horas após contenção | DPO + Jurídico + TI |
| Notificação à ANPD | Até 72 horas após ciência | DPO + Jurídico |
| Comunicação aos titulares | O mais breve possível | DPO + Comunicação |
| Erradicação e recuperação | Conforme cronograma TI | TI + DPO |
| Análise pós-incidente | Até 15 dias após resolução | DPO + TI + Liderança |

---

## 7. O que NÃO fazer durante um incidente

- Não apagar logs, e-mails ou evidências antes de preservá-los
- Não comunicar o incidente publicamente ou à imprensa sem autorização da liderança e do jurídico
- Não tentar resolver sozinho sem acionar a equipe de resposta
- Não minimizar o incidente internamente para evitar escalada
- Não pagar resgate em casos de ransomware sem avaliação jurídica prévia
- Não reiniciar ou formatar sistemas afetados antes de preservar as evidências

---

## 8. Registro de incidente

> **[Instrução de preenchimento]:** Abra um registro para cada incidente, mesmo os de nível Baixo. Esses registros são a prova de que a empresa monitora e responde a incidentes — fundamental em caso de fiscalização da ANPD. Mantenha os registros por no mínimo 5 anos.

| Campo | Informação |
|---|---|
| **ID do incidente** | [INC-001] |
| **Data e hora da detecção** | [DD/MM/AAAA — HH:MM] |
| **Detectado por** | [Nome e cargo] |
| **Data e hora do reporte ao DPO** | [DD/MM/AAAA — HH:MM] |
| **Classificação** | [Alto / Médio / Baixo] |
| **Descrição do incidente** | [O que aconteceu] |
| **Dados afetados** | [Categorias e volume estimado] |
| **Titulares afetados** | [Número estimado e perfil] |
| **Dados sensíveis envolvidos?** | [Sim / Não — especificar] |
| **Incidente ainda em curso?** | [Sim / Não] |
| **Causa identificada** | [Ataque externo / Erro interno / Falha de sistema / Outro] |
| **Medidas de contenção adotadas** | [Descrever ações] |
| **Notificação à ANPD necessária?** | [Sim / Não / Em avaliação] |
| **Data da notificação à ANPD** | [DD/MM/AAAA] |
| **Protocolo ANPD** | [Número do protocolo] |
| **Titulares comunicados?** | [Sim / Não / Parcial] |
| **Data da comunicação aos titulares** | [DD/MM/AAAA] |
| **Resolução** | [Descrição da solução aplicada] |
| **Data de encerramento** | [DD/MM/AAAA] |
| **Ações de melhoria identificadas** | [Listar ações com responsáveis e prazos] |
| **Responsável pelo registro** | [Nome do DPO ou responsável] |

---

## 9. Testes e simulações

Este playbook deve ser testado ao menos **uma vez por ano** por meio de simulações de incidente, envolvendo os principais membros da equipe de resposta.

**O que simular:**
- Vazamento de dados por envio de e-mail para destinatário errado
- Ataque de ransomware bloqueando acesso a sistemas
- Acesso indevido de colaborador a dados fora do seu escopo
- Perda de notebook com dados de clientes

Após cada simulação, registrar as falhas identificadas e atualizar o playbook.

---

## Histórico de revisões

| Versão | Data | Descrição | Responsável |
|---|---|---|---|
| 1.0 | DD/MM/AAAA | Emissão inicial | [Nome] |

---

*Documento elaborado em conformidade com a Lei Geral de Proteção de Dados — LGPD (Lei nº 13.709/2018), Art. 48º.*
