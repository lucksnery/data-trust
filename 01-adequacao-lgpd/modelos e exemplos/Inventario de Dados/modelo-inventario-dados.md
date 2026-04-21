# Inventário de Dados Pessoais (Data Mapping)

**Empresa:** [Nome da Empresa]
**CNPJ:** [00.000.000/0001-00]
**Responsável pelo inventário:** [Nome do DPO ou responsável]
**Última atualização:** DD de mês de AAAA
**Versão:** 1.0

---

## Instruções de uso

Este documento registra todos os dados pessoais tratados pela empresa, organizados por processo ou departamento. Ele deve ser mantido atualizado sempre que houver:

- Novo sistema ou ferramenta que colete dados pessoais
- Mudança de finalidade no uso de um dado
- Novo fornecedor com acesso a dados pessoais
- Encerramento de um processo ou sistema

Revise este inventário ao menos **uma vez por ano**.

> **[Instrução de preenchimento]:** Cada linha da tabela representa um conjunto de dados de um processo específico. Se a empresa tiver muitos processos, crie uma tabela por departamento. Não agrupe processos muito diferentes na mesma linha — prefira granularidade maior.

---

## Como preencher os campos

| Campo | O que registrar |
|---|---|
| **ID** | Número sequencial para identificar o registro (ex: 001, 002) |
| **Processo / Área** | O processo ou departamento responsável pela coleta (ex: Comercial, RH, Marketing) |
| **Descrição do processo** | O que acontece nesse processo em relação a dados pessoais |
| **Dados coletados** | Liste os dados pessoais tratados (nome, e-mail, CPF, telefone, etc.) |
| **Categoria do dado** | Comum ou Sensível (dados sensíveis: saúde, biometria, religião, etnia, etc.) |
| **Titular** | Quem são as pessoas cujos dados são tratados (clientes, colaboradores, fornecedores, visitantes) |
| **Finalidade** | Por que esses dados são coletados e usados |
| **Base legal** | A base legal da LGPD que justifica o tratamento (ver tabela de referência abaixo) |
| **Armazenamento** | Onde os dados ficam guardados (sistema, planilha, nuvem, físico) |
| **Acesso** | Quais departamentos ou cargos têm acesso |
| **Compartilhamento** | Se os dados são compartilhados com terceiros e com quem |
| **Retenção** | Por quanto tempo os dados são mantidos |
| **Descarte** | Como os dados são eliminados após o prazo |
| **Observações** | Informações adicionais relevantes |

---

## Tabela de referência — Bases legais (Art. 7º LGPD)

| Código | Base Legal | Quando usar |
|---|---|---|
| BL01 | Consentimento | O titular autorizou expressamente o tratamento |
| BL02 | Contrato | Tratamento necessário para executar contrato com o titular |
| BL03 | Obrigação legal | Exigido por lei ou regulação (ex: dados trabalhistas, fiscais) |
| BL04 | Políticas públicas | Execução de políticas públicas pela administração pública |
| BL05 | Pesquisa | Estudos por órgão de pesquisa, com anonimização quando possível |
| BL06 | Proteção da vida | Proteção da vida ou incolumidade física do titular ou terceiro |
| BL07 | Tutela da saúde | Procedimentos realizados por profissionais de saúde |
| BL08 | Legítimo interesse | Interesses legítimos da empresa, desde que não prejudiquem o titular |
| BL09 | Proteção do crédito | Proteção ao crédito, conforme legislação pertinente |

> **[Instrução de preenchimento]:** Use o código da base legal (ex: BL01) na coluna correspondente da tabela de inventário. Evite usar BL01 (consentimento) como padrão para tudo — analise caso a caso qual base é mais adequada.

---

## Inventário

> **[Instrução de preenchimento]:** Duplique os blocos abaixo para cada processo da empresa. Se preferir, este inventário pode ser migrado para uma planilha (Excel ou Google Sheets) mantendo os mesmos campos — o formato aqui serve como referência e documentação no repositório.

---

### Registro 001

| Campo | Informação |
|---|---|
| **ID** | 001 |
| **Processo / Área** | [Ex: Cadastro de clientes — Comercial] |
| **Descrição do processo** | [Ex: Coleta de dados no momento do cadastro de novos clientes na plataforma] |
| **Dados coletados** | [Ex: Nome completo, e-mail, telefone, CPF, endereço] |
| **Categoria do dado** | [Comum / Sensível] |
| **Titular** | [Ex: Clientes] |
| **Finalidade** | [Ex: Identificação do cliente, emissão de nota fiscal e envio de comunicações sobre o serviço contratado] |
| **Base legal** | [Ex: BL02 — Contrato] |
| **Armazenamento** | [Ex: CRM HubSpot — nuvem / servidor próprio / planilha Google Sheets] |
| **Acesso** | [Ex: Time comercial e financeiro] |
| **Compartilhamento** | [Ex: Compartilhado com plataforma de emissão de NF (nome do sistema)] |
| **Retenção** | [Ex: Enquanto o contrato estiver ativo + 5 anos após encerramento] |
| **Descarte** | [Ex: Exclusão do CRM + destruição de arquivos físicos após prazo] |
| **Observações** | [Ex: Dados fiscais mantidos conforme obrigação legal — BL03] |

---

### Registro 002

| Campo | Informação |
|---|---|
| **ID** | 002 |
| **Processo / Área** | [Ex: Recrutamento e seleção — RH] |
| **Descrição do processo** | [Ex: Coleta de currículos e dados de candidatos durante processos seletivos] |
| **Dados coletados** | [Ex: Nome, e-mail, telefone, histórico profissional, pretensão salarial] |
| **Categoria do dado** | [Comum] |
| **Titular** | [Ex: Candidatos] |
| **Finalidade** | [Ex: Avaliação de perfil para vagas em aberto] |
| **Base legal** | [Ex: BL08 — Legítimo interesse] |
| **Armazenamento** | [Ex: Pasta compartilhada no Google Drive — acesso restrito ao RH] |
| **Acesso** | [Ex: Equipe de RH e gestores das áreas com vagas] |
| **Compartilhamento** | [Ex: Não compartilhado com terceiros] |
| **Retenção** | [Ex: 6 meses após encerramento do processo seletivo] |
| **Descarte** | [Ex: Exclusão permanente da pasta e e-mails relacionados] |
| **Observações** | [Ex: Candidatos aprovados têm seus dados migrados para o registro de colaboradores] |

---

### Registro 003

| Campo | Informação |
|---|---|
| **ID** | 003 |
| **Processo / Área** | [Ex: E-mail marketing — Marketing] |
| **Descrição do processo** | [Ex: Envio de newsletters e comunicações promocionais para leads e clientes] |
| **Dados coletados** | [Ex: Nome, e-mail] |
| **Categoria do dado** | [Comum] |
| **Titular** | [Ex: Leads e clientes] |
| **Finalidade** | [Ex: Nutrição de leads e relacionamento com clientes por e-mail] |
| **Base legal** | [Ex: BL01 — Consentimento] |
| **Armazenamento** | [Ex: Plataforma de e-mail marketing (nome da ferramenta) — nuvem fora do Brasil] |
| **Acesso** | [Ex: Time de marketing] |
| **Compartilhamento** | [Ex: Dados armazenados na plataforma (nome) — transferência internacional] |
| **Retenção** | [Ex: Enquanto o contato não solicitar descadastro ou exclusão] |
| **Descarte** | [Ex: Remoção da base na plataforma mediante solicitação do titular ou inatividade por 2 anos] |
| **Observações** | [Ex: Consentimento coletado via checkbox no formulário do site. Registros de consentimento mantidos por 5 anos] |

---

> **[Instrução de preenchimento]:** Continue adicionando registros no mesmo formato. Exemplos de processos comuns que devem ser mapeados:
> - Atendimento ao cliente (chat, e-mail, telefone)
> - Emissão de notas fiscais
> - Folha de pagamento e dados de colaboradores
> - Acesso a sistemas internos (logs)
> - Formulários do site (contato, orçamento, download de material)
> - Integrações com ferramentas de terceiros (CRM, ERP, suporte)

---

## Histórico de revisões

| Versão | Data | Descrição | Responsável |
|---|---|---|---|
| 1.0 | DD/MM/AAAA | Criação do inventário inicial | [Nome] |
| 1.1 | DD/MM/AAAA | [Descreva a alteração] | [Nome] |

---

*Documento mantido em conformidade com a Lei Geral de Proteção de Dados — LGPD (Lei nº 13.709/2018), Art. 37º.*
