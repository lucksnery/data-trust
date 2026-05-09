# Gestão de Riscos e Continuidade — Guia de Diagnóstico e Ação

Este documento orienta o executor do projeto na identificação, avaliação e tratamento de riscos relacionados à segurança da informação, continuidade operacional e proteção de dados dentro da empresa. A abordagem é sequencial: cada etapa começa com uma pergunta de diagnóstico e, a partir da resposta, direciona para as ações necessárias ou para o próximo ponto. O objetivo não é eliminar totalmente os riscos — isso é impossível — mas identificá-los, avaliá-los e reduzi-los a níveis aceitáveis, garantindo maior segurança, previsibilidade e continuidade das operações.

---

## 1. A empresa possui um processo formal de gestão de riscos?

Considere qualquer tipo de risco relacionado a dados, sistemas, pessoas, processos ou operações. Sem um processo estruturado, a empresa reage a problemas em vez de preveni-los.

- **Se não possui:** seguir os itens 1.1 a 1.4 abaixo.
- **Se possui:** pular para a etapa 2.

---

### 1.1 Definição de metodologia de gestão de riscos

Antes de identificar riscos, a empresa precisa de um padrão claro para avaliá-los e tratá-los — sem metodologia, cada área faz à sua maneira e os resultados não são comparáveis.

**O que fazer:**

- Definir uma metodologia de [gestão de riscos](https://pt.wikipedia.org/wiki/Gest%C3%A3o_de_riscos) — qualitativa, quantitativa ou híbrida
- Estabelecer critérios de avaliação baseados em probabilidade e impacto
- Padronizar a forma de identificação, análise e tratamento de riscos em todas as áreas
- Documentar a metodologia em política formal aprovada pela liderança

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — gestão de riscos em segurança da informação. [NIST SP 800-30](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final) — guia de avaliação de riscos para sistemas de informação.

---

### 1.2 Inventário e identificação de ativos críticos

Não é possível proteger o que não se conhece. O inventário de ativos é o ponto de partida de qualquer programa de gestão de riscos.

**O que fazer:**

- Mapear todos os ativos da empresa relevantes para a segurança da informação:
  - **Dados:** bases de clientes, dados financeiros, dados de colaboradores, propriedade intelectual
  - **Sistemas:** ERPs, CRMs, plataformas, e-mail, sistemas legados
  - **Infraestrutura:** servidores, redes, dispositivos, ambientes de nuvem
  - **Pessoas:** colaboradores com acesso a sistemas críticos, prestadores de serviço
  - **Processos:** processos operacionais que dependem de sistemas ou dados sensíveis
- Classificar cada ativo por criticidade para o negócio (alto, médio, baixo)
- Atribuir um responsável para cada ativo crítico
- Manter o inventário atualizado — ativos mudam conforme a empresa evolui

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Inventario de Ativos/` para ver modelo de inventário com campos de criticidade e responsável.

---

### 1.3 Identificação de ameaças e vulnerabilidades

Com os ativos mapeados, o próximo passo é identificar o que pode dar errado — e por quê.

**O que fazer:**

- Para cada ativo crítico, identificar as principais [ameaças](https://pt.wikipedia.org/wiki/Amea%C3%A7a_(seguran%C3%A7a_da_informa%C3%A7%C3%A3o)):
  - Vazamento ou exfiltração de dados
  - Ataques externos: [phishing](https://pt.wikipedia.org/wiki/Phishing), [ransomware](https://pt.wikipedia.org/wiki/Ransomware), [DDoS](https://pt.wikipedia.org/wiki/Ataque_de_nega%C3%A7%C3%A3o_de_servi%C3%A7o)
  - Falha de sistema ou infraestrutura
  - Erro humano ou sabotagem interna
  - Desastres naturais ou falhas de energia
  - Indisponibilidade de fornecedores críticos
- Identificar as [vulnerabilidades](https://pt.wikipedia.org/wiki/Vulnerabilidade_(inform%C3%A1tica)) que tornam os ativos suscetíveis a essas ameaças:
  - Sistemas desatualizados ou sem patch
  - Ausência de controles de acesso
  - Backups inexistentes ou não testados
  - Falta de treinamento dos colaboradores
  - Dependência excessiva de um único fornecedor

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — obrigação de adotar medidas de segurança para proteção contra riscos e incidentes.

---

### 1.4 Registro de riscos (Risk Register)

Os riscos identificados precisam ser documentados e acompanhados ao longo do tempo — um risco sem registro é um risco sem dono e sem prazo.

**O que fazer:**

- Criar um [Risk Register](https://en.wikipedia.org/wiki/Risk_register) — registro centralizado de riscos — em planilha ou ferramenta de GRC
- Para cada risco, registrar:
  - Descrição do risco
  - Ativo afetado
  - Ameaça e vulnerabilidade associadas
  - Probabilidade (baixa, média, alta)
  - Impacto (financeiro, operacional, reputacional, legal)
  - Nível de criticidade resultante
  - Estratégia de tratamento definida
  - Responsável pelo tratamento
  - Prazo e status das ações
- Revisar e atualizar o registro ao menos trimestralmente

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Risk Register/` para ver modelo de registro de riscos com matriz de criticidade.

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e prestação de contas.

---

## 2. A empresa avalia e prioriza os riscos identificados?

Identificar riscos sem avaliá-los é ineficiente — a empresa precisa saber onde concentrar os esforços primeiro.

- **Se não avalia formalmente:** seguir os itens 2.1 e 2.2 abaixo.
- **Se já avalia com critérios definidos:** pular para a etapa 3.

---

### 2.1 Matriz de risco — probabilidade x impacto

A [matriz de risco](https://pt.wikipedia.org/wiki/Matriz_de_risco) é a ferramenta mais usada para priorizar riscos de forma visual e objetiva. Combina a probabilidade de um evento ocorrer com o impacto que causaria caso ocorresse.

**O que fazer:**

- Definir escala de probabilidade:
  - **Baixa:** evento improvável no contexto atual
  - **Média:** evento possível, já ocorreu em situações similares
  - **Alta:** evento provável ou recorrente
- Definir escala de impacto:
  - **Baixo:** impacto mínimo, facilmente recuperável
  - **Médio:** impacto relevante, requer esforço para recuperação
  - **Alto:** impacto crítico, pode comprometer a operação ou gerar sanções legais
- Classificar cada risco do Risk Register com base nessa escala
- Usar a combinação probabilidade x impacto para definir o nível de criticidade:

| | Impacto Baixo | Impacto Médio | Impacto Alto |
|---|---|---|---|
| **Probabilidade Alta** | 🟡 Médio | 🔴 Alto | 🔴 Crítico |
| **Probabilidade Média** | 🟢 Baixo | 🟡 Médio | 🔴 Alto |
| **Probabilidade Baixa** | 🟢 Baixo | 🟢 Baixo | 🟡 Médio |

---

### 2.2 Priorização e apetite de risco

Nem todos os riscos devem ser tratados ao mesmo tempo — e nem todos precisam ser eliminados. A empresa precisa definir seu [apetite de risco (risk appetite)](https://en.wikipedia.org/wiki/Risk_appetite): o nível de risco que está disposta a aceitar para operar.

**O que fazer:**

- Definir o apetite de risco da empresa em conjunto com a liderança — quais níveis são aceitáveis sem ação imediata
- Priorizar tratamento dos riscos críticos e altos
- Documentar formalmente a decisão de aceitar riscos baixos sem ação imediata
- Apresentar o mapa de riscos à liderança para validação e apoio às ações de mitigação

**Referência técnica:** [ISO/IEC 27005](https://www.iso.org/standard/75281.html) — avaliação e priorização de riscos.

---

## 3. A empresa define e executa planos de tratamento para os riscos?

Identificar e avaliar riscos sem agir sobre eles não reduz exposição. Cada risco precisa de uma decisão documentada e um responsável.

- **Se não define planos de tratamento:** seguir os itens 3.1 a 3.3 abaixo.
- **Se já define e acompanha:** pular para a etapa 4.

---

### 3.1 Estratégias de tratamento de risco

Para cada risco identificado, a empresa deve adotar uma das quatro estratégias possíveis:

| Estratégia | Quando usar | Exemplo |
|---|---|---|
| **Mitigar** | Quando é possível reduzir a probabilidade ou o impacto | Implementar backup para reduzir impacto de falha de sistema |
| **Aceitar** | Quando o risco é baixo e o custo de mitigação supera o impacto | Aceitar risco de falha em sistema legado de baixo uso |
| **Transferir** | Quando é possível repassar o risco a terceiros | Contratar seguro cibernético ou terceirizar um serviço crítico |
| **Evitar** | Quando a atividade que gera o risco pode ser interrompida | Descontinuar processo que coleta dados desnecessários |

**O que fazer:**

- Para cada risco no Risk Register, definir e documentar a estratégia adotada
- Atribuir responsável e prazo para execução
- Nunca deixar um risco crítico sem estratégia definida

---

### 3.2 Implementação de controles

Controles são as medidas concretas que reduzem riscos. Podem ser técnicos ou administrativos.

**Exemplos de controles técnicos:**

- Backup automatizado com testes periódicos de restauração
- Autenticação multifator em sistemas críticos
- Monitoramento e alertas de sistemas em tempo real
- Gestão de patches e atualizações de segurança
- Segmentação de redes e controle de acesso por perfil

**Exemplos de controles administrativos:**

- Políticas de segurança documentadas e assinadas
- Treinamentos periódicos de colaboradores
- Processos formais de onboarding e offboarding
- Auditorias internas regulares
- Cláusulas de segurança em contratos com fornecedores

**Referência legal:** [Art. 46º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art46) — adoção de medidas de segurança técnicas e administrativas para proteção de dados.

---

### 3.3 Monitoramento e revisão dos planos de tratamento

**O que fazer:**

- Revisar o status das ações de tratamento ao menos trimestralmente
- Atualizar o Risk Register sempre que um controle for implementado ou um risco mudar de nível
- Identificar novos riscos que surjam com mudanças no ambiente, nos sistemas ou nos processos
- Apresentar relatório de evolução à liderança semestralmente

---

## 4. A empresa possui política e processo de backup?

[Backup](https://pt.wikipedia.org/wiki/C%C3%B3pia_de_seguran%C3%A7a) é a base de qualquer estratégia de continuidade. Sem backup testado e funcionando, qualquer incidente — desde um ransomware até uma exclusão acidental — pode resultar em perda irreversível de dados e paralisação das operações.

- **Se já existe política de backup documentada e com testes regulares:** pular para a etapa 5.
- **Se não existe ou é informal:** seguir os itens 4.1 a 4.4 abaixo.

---

### 4.1 O que fazer backup — definindo o escopo

**O que fazer:**

- Mapear todos os dados e sistemas que precisam de backup:
  - Bases de dados de sistemas críticos (ERP, CRM, financeiro)
  - Arquivos e documentos corporativos
  - Configurações de sistemas e servidores
  - E-mails e comunicações críticas
  - Código-fonte de sistemas próprios
- Classificar por criticidade — dados críticos exigem backup mais frequente e maior redundância
- Definir o [RPO (Recovery Point Objective)](https://pt.wikipedia.org/wiki/Recovery_point_objective) para cada sistema: quanto de perda de dados é aceitável? (ex: RPO de 4h = backup a cada 4 horas no máximo)

---

### 4.2 Tipos de backup

Escolher o tipo certo de backup equilibra custo, tempo de execução e capacidade de recuperação.

| Tipo | Como funciona | Vantagem | Desvantagem |
|---|---|---|---|
| **Completo** | Copia todos os dados integralmente | Recuperação simples e rápida | Consome mais espaço e tempo |
| **Incremental** | Copia apenas o que mudou desde o último backup (completo ou incremental) | Rápido e eficiente em espaço | Recuperação mais complexa |
| **Diferencial** | Copia tudo que mudou desde o último backup completo | Equilíbrio entre velocidade e simplicidade de recuperação | Cresce ao longo do tempo |

**Recomendação prática:** adotar a estratégia [3-2-1](https://pt.wikipedia.org/wiki/Backup#Regra_3-2-1):
- **3** cópias dos dados
- **2** mídias ou locais de armazenamento diferentes
- **1** cópia offsite ou em nuvem

---

### 4.3 Onde armazenar os backups

**O que fazer:**

- **Local (on-premises):** servidores ou NAS internos — rápido para restauração, mas vulnerável a desastres físicos no mesmo local
- **Nuvem:** serviços como [AWS S3](https://aws.amazon.com/s3/), [Google Cloud Storage](https://cloud.google.com/storage), [Azure Blob Storage](https://azure.microsoft.com/en-us/products/storage/blobs/) ou soluções como [Backblaze B2](https://www.backblaze.com/cloud-storage) — escalável e geograficamente distribuído
- **Offsite físico:** mídias transportadas para local externo — útil como camada adicional para dados críticos
- Garantir que backups em nuvem estejam **criptografados** em trânsito e em repouso
- Nunca armazenar o único backup no mesmo local físico que os dados originais — um incêndio ou alagamento elimina ambos

---

### 4.4 Testes de restauração — o backup só vale se funcionar

Um backup que nunca foi testado não é um backup — é uma esperança. A maioria das empresas descobre que o backup está corrompido ou incompleto exatamente no momento em que mais precisam dele.

**O que fazer:**

- Realizar testes de restauração completos ao menos **uma vez por trimestre**
- Testar a restauração em ambiente isolado — nunca sobrescrever dados de produção durante o teste
- Validar que os dados restaurados estão íntegros e os sistemas funcionam corretamente após a restauração
- Documentar cada teste: data, escopo, resultado, tempo de restauração e responsável
- Medir o [RTO (Recovery Time Objective)](https://pt.wikipedia.org/wiki/Recovery_time_objective) real — quanto tempo leva para restaurar o sistema — e comparar com o objetivo definido

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Politica de Backup/` para ver modelo de política de backup e checklist de teste de restauração.

---

## 5. A empresa possui Plano de Continuidade de Negócios (BCP)?

O [Plano de Continuidade de Negócios (BCP — Business Continuity Plan)](https://pt.wikipedia.org/wiki/Plano_de_continuidade_de_neg%C3%B3cios) define como a empresa vai continuar operando durante e após um evento disruptivo — seja um ataque cibernético, falha de sistema, desastre natural ou indisponibilidade de fornecedor crítico.

- **Se já existe BCP documentado e testado:** pular para a etapa 6.
- **Se não existe:** seguir os itens 5.1 a 5.4 abaixo.

---

### 5.1 Identificação de processos e sistemas críticos

Antes de criar o plano, a empresa precisa saber o que não pode parar.

**O que fazer:**

- Mapear todos os processos de negócio e identificar quais são críticos para a operação
- Para cada processo crítico, identificar:
  - Sistemas e dados dos quais depende
  - Pessoas-chave envolvidas
  - Fornecedores e dependências externas
  - Impacto financeiro e operacional de cada hora de indisponibilidade
- Conduzir uma [BIA (Business Impact Analysis)](https://en.wikipedia.org/wiki/Business_impact_analysis) — análise de impacto nos negócios — para quantificar o custo da indisponibilidade de cada processo

---

### 5.2 Definição de RTO e RPO

[RTO (Recovery Time Objective)](https://pt.wikipedia.org/wiki/Recovery_time_objective) e [RPO (Recovery Point Objective)](https://pt.wikipedia.org/wiki/Recovery_point_objective) são os dois parâmetros fundamentais de qualquer plano de continuidade.

| Parâmetro | Definição | Exemplo |
|---|---|---|
| **RTO** | Tempo máximo aceitável para restaurar um sistema ou processo após um incidente | "O sistema de vendas deve estar restaurado em até 4 horas" |
| **RPO** | Quantidade máxima aceitável de perda de dados (medida em tempo) | "Podemos perder no máximo 1 hora de transações" |

**O que fazer:**

- Definir RTO e RPO para cada processo e sistema crítico
- Garantir que a estratégia de backup e recuperação está alinhada com os RPOs definidos
- Garantir que a infraestrutura de recuperação permite atingir os RTOs definidos
- Documentar os valores acordados com a liderança — eles definem os investimentos necessários em infraestrutura

---

### 5.3 Estratégias de continuidade operacional

**O que fazer:**

- Definir como cada processo crítico continuará funcionando durante um incidente:
  - Processos manuais temporários para substituir sistemas indisponíveis
  - Roteamento de operações para equipes ou locais alternativos
  - Comunicação com clientes e fornecedores sobre impactos e prazos
  - Priorização de quais processos restaurar primeiro
- Identificar dependências críticas de fornecedores e planejar alternativas em caso de indisponibilidade

---

### 5.4 Plano de comunicação em crises

Uma crise sem comunicação estruturada gera desinformação, pânico e danos reputacionais desnecessários.

**O que fazer:**

- Definir árvore de comunicação interna: quem aciona quem, em qual ordem, por qual canal
- Definir porta-voz oficial para comunicações externas — clientes, imprensa, reguladores
- Criar templates de comunicação para os cenários mais prováveis (ataque, indisponibilidade, vazamento)
- Garantir que os contatos de emergência estão disponíveis fora dos sistemas que podem estar indisponíveis (ex: lista física ou em sistema externo)

**📁 Exemplo prático:** Consulte a pasta `/exemplos/BCP/` para ver modelo de Plano de Continuidade de Negócios e templates de comunicação em crise.

---

## 6. A empresa possui Plano de Disaster Recovery (DR)?

O [Plano de Disaster Recovery (DR)](https://pt.wikipedia.org/wiki/Recupera%C3%A7%C3%A3o_de_desastres) é o conjunto de procedimentos técnicos para restaurar sistemas e infraestrutura após um evento catastrófico. É mais específico que o BCP — enquanto o BCP define como a empresa continua operando, o DR define como os sistemas voltam a funcionar.

- **Se já existe plano de DR documentado e testado:** pular para a etapa 7.
- **Se não existe:** seguir os itens 6.1 a 6.3 abaixo.

---

### 6.1 Estratégias de Disaster Recovery

A estratégia de DR define o nível de redundância e o custo associado à recuperação. Existem três abordagens principais:

| Estratégia | Como funciona | RTO | Custo |
|---|---|---|---|
| **Cold Standby** | Infraestrutura de backup existe mas fica desligada — precisa ser ligada e configurada no momento do desastre | Horas a dias | Baixo |
| **Warm Standby** | Infraestrutura de backup existe, está ligada e parcialmente atualizada — precisa de configuração final antes de assumir | Minutos a horas | Médio |
| **Hot Standby** | Infraestrutura de backup está ativa, sincronizada em tempo real e pronta para assumir imediatamente | Segundos a minutos | Alto |

**O que fazer:**

- Escolher a estratégia adequada para cada sistema crítico com base no RTO definido no BCP e no orçamento disponível
- Para sistemas com RTO de horas, Cold ou Warm Standby pode ser suficiente
- Para sistemas com RTO de minutos (ex: e-commerce, sistemas de pagamento), Hot Standby é necessário
- Documentar a estratégia escolhida e os procedimentos de ativação do ambiente de DR

---

### 6.2 Implementação do ambiente de DR

**O que fazer:**

- Definir se o ambiente de DR será:
  - **On-premises:** datacenter secundário próprio
  - **Nuvem:** ambiente em cloud provider como [AWS](https://aws.amazon.com/pt/), [Google Cloud](https://cloud.google.com/) ou [Azure](https://azure.microsoft.com/) — mais flexível e escalável
  - **Híbrido:** combinação de infraestrutura própria e nuvem
- Garantir que o ambiente de DR está em localização geográfica diferente do ambiente principal — um desastre regional não pode atingir ambos
- Manter a infraestrutura de DR atualizada conforme o ambiente de produção evolui
- Documentar passo a passo os procedimentos de ativação do DR — em um incidente real, não há tempo para improvisar

---

### 6.3 Testes e simulações do plano de DR

Um plano de DR não testado é tão arriscado quanto não ter plano.

**O que fazer:**

- Realizar testes de DR ao menos **uma vez por ano** — de preferência semestralmente para sistemas críticos
- Testar em ambiente isolado para não impactar a produção
- Simular cenários reais: falha total de servidor, ataque de ransomware, indisponibilidade de datacenter
- Medir o RTO real e comparar com o objetivo — se o sistema leva 6 horas para ser restaurado e o RTO é 2 horas, há um gap crítico a resolver
- Documentar os resultados e atualizar o plano após cada teste

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Disaster Recovery/` para ver modelo de Plano de DR e roteiro de simulação.

---

## 7. A empresa possui processo de gestão de vulnerabilidades e patches?

[Vulnerabilidades](https://pt.wikipedia.org/wiki/Vulnerabilidade_(inform%C3%A1tica)) em sistemas desatualizados são uma das principais portas de entrada para ataques. A [gestão de patches](https://pt.wikipedia.org/wiki/Patch_(inform%C3%A1tica)) — atualizações de segurança — é um controle básico e obrigatório em qualquer programa de segurança.

- **Se já existe processo formal de gestão de vulnerabilidades e patches:** pular para a etapa 8.
- **Se não existe:** seguir os itens 7.1 e 7.2 abaixo.

---

### 7.1 Gestão de vulnerabilidades

**O que fazer:**

- Realizar varreduras periódicas de vulnerabilidades em sistemas, redes e aplicações — ao menos mensalmente
- Utilizar ferramentas de [vulnerability scanning](https://en.wikipedia.org/wiki/Vulnerability_scanner):
  - [Nessus](https://www.tenable.com/products/nessus) — referência de mercado para escaneamento de vulnerabilidades
  - [OpenVAS](https://www.openvas.org/) — alternativa gratuita e open source
  - [Qualys](https://www.qualys.com/) — solução cloud com gestão centralizada
- Priorizar correção de vulnerabilidades por criticidade — críticas e altas têm prazo máximo de 72 horas para tratamento
- Manter registro de todas as vulnerabilidades identificadas, status de correção e responsável

---

### 7.2 Gestão de patches e atualizações

**O que fazer:**

- Definir política de atualização: sistemas operacionais, aplicações e firmwares devem ser atualizados em prazo definido após o lançamento do patch
- Testar patches em ambiente de homologação antes de aplicar em produção — patches mal testados podem causar indisponibilidade
- Automatizar atualizações de segurança onde possível — especialmente em endpoints (notebooks, desktops)
- Mapear sistemas legados que não recebem mais atualizações do fabricante ([End of Life](https://en.wikipedia.org/wiki/End-of-life_product)) e tratar como risco crítico
- Incluir a gestão de patches no processo de onboarding de novos sistemas

---

## 8. A empresa possui proteção contra malware e ransomware?

[Malware](https://pt.wikipedia.org/wiki/Malware) é qualquer software malicioso projetado para danificar, comprometer ou sequestrar sistemas e dados. [Ransomware](https://pt.wikipedia.org/wiki/Ransomware) é sua variante mais destrutiva — criptografa os dados da empresa e exige pagamento para liberá-los. Ataques de ransomware paralisaram empresas inteiras de todos os portes e setores.

- **Se já existe proteção multicamada implementada:** pular para a etapa 9.
- **Se não existe ou é insuficiente:** seguir os itens 8.1 e 8.2 abaixo.

---

### 8.1 Camadas de proteção contra malware

Proteção eficaz contra malware não depende de uma única ferramenta — é uma combinação de camadas técnicas e comportamentais.

**Camadas técnicas:**

- **Endpoint Protection (EPP/EDR):** solução de antivírus e detecção de comportamento em todos os dispositivos
  - [CrowdStrike Falcon](https://www.crowdstrike.com/) — referência em EDR corporativo
  - [SentinelOne](https://www.sentinelone.com/) — proteção com IA e resposta automatizada
  - [Microsoft Defender for Endpoint](https://www.microsoft.com/en-us/security/business/endpoint-security/microsoft-defender-endpoint) — integrado ao ecossistema Microsoft
- **Filtragem de e-mail:** bloquear e-mails com anexos maliciosos e links de phishing antes de chegarem ao colaborador
- **Filtragem de DNS:** bloquear acesso a domínios maliciosos conhecidos — [Cloudflare Gateway](https://www.cloudflare.com/products/zero-trust/gateway/), [Cisco Umbrella](https://umbrella.cisco.com/)
- **Segmentação de rede:** limitar o alcance lateral de um malware que consiga entrar — se um dispositivo for comprometido, a infecção não se espalha para toda a rede
- **Princípio do menor privilégio:** usuários sem privilégios de administrador não conseguem instalar software malicioso

**Camadas comportamentais:**

- Treinar colaboradores para identificar phishing e engenharia social — ponto de entrada da maioria dos ataques de ransomware
- Proibir instalação de software não autorizado em dispositivos corporativos
- Criar canal de reporte rápido para comportamentos suspeitos em sistemas

---

### 8.2 Resposta específica a ransomware

**O que fazer:**

- Nunca pagar o resgate sem avaliação jurídica e técnica — o pagamento não garante a recuperação dos dados e financia organizações criminosas
- Em caso de infecção confirmada:
  1. Isolar imediatamente os dispositivos afetados da rede
  2. Acionar o plano de resposta a incidentes
  3. Verificar a integridade dos backups antes de qualquer ação de recuperação
  4. Acionar suporte especializado em resposta a incidentes cibernéticos se necessário
- Garantir que os backups são armazenados em local inacessível pela rede de produção — backups conectados à rede são criptografados junto com os dados originais em ataques de ransomware

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Protecao contra Malware/` para ver checklist de proteção e roteiro de resposta a ransomware.

---

## 9. A empresa possui controles de segurança em ambientes de nuvem?

A adoção de [computação em nuvem](https://pt.wikipedia.org/wiki/Computa%C3%A7%C3%A3o_em_nuvem) amplia as possibilidades operacionais, mas também cria novos riscos — configurações incorretas, acessos mal gerenciados e dados expostos publicamente são alguns dos erros mais comuns e mais custosos em ambientes cloud.

- **Se já existem controles formais de segurança em nuvem:** pular para a etapa 10.
- **Se não existem:** seguir os itens 9.1 e 9.2 abaixo.

---

### 9.1 Configuração segura de ambientes cloud

O erro mais comum em nuvem não é um ataque sofisticado — é uma configuração incorreta que expõe dados publicamente sem que ninguém perceba.

**O que fazer:**

- Adotar o [modelo de responsabilidade compartilhada](https://aws.amazon.com/pt/compliance/shared-responsibility-model/): o provedor de nuvem é responsável pela segurança **da** nuvem — você é responsável pela segurança **na** nuvem
- Garantir que nenhum bucket de armazenamento (S3, GCS, Azure Blob) está configurado como público sem necessidade explícita
- Habilitar [MFA](https://pt.wikipedia.org/wiki/Autentica%C3%A7%C3%A3o_multifator) para todos os acessos ao console de administração do cloud provider
- Aplicar o princípio do menor privilégio nas permissões de IAM (Identity and Access Management)
- Habilitar logs de auditoria ([AWS CloudTrail](https://aws.amazon.com/cloudtrail/), [GCP Cloud Audit Logs](https://cloud.google.com/logging/docs/audit), [Azure Monitor](https://azure.microsoft.com/en-us/products/monitor/)) para rastrear todas as ações realizadas no ambiente
- Utilizar ferramentas de [CSPM (Cloud Security Posture Management)](https://en.wikipedia.org/wiki/Cloud_security_posture_management) para identificar configurações inseguras automaticamente

---

### 9.2 Gestão de acessos e dados em nuvem

**O que fazer:**

- Nunca usar credenciais root ou de administrador global para operações rotineiras — criar contas com permissões mínimas necessárias
- Rotacionar chaves de acesso (API keys) periodicamente e nunca expô-las em código-fonte ou repositórios públicos
- Garantir que dados sensíveis armazenados em nuvem estão criptografados em repouso e em trânsito
- Definir política de retenção de dados em nuvem — dados sem prazo definido se acumulam e aumentam a superfície de exposição
- Revisar permissões de acesso periodicamente — acessos concedidos e nunca revisados são um risco crescente

**📁 Exemplo prático:** Consulte a pasta `/exemplos/Seguranca em Nuvem/` para ver checklist de configuração segura por provedor (AWS, GCP, Azure).

---

## 10. A empresa possui integração entre gestão de riscos e resposta a incidentes?

Quando um risco se materializa, ele se torna um incidente. O ciclo só está completo quando a empresa consegue aprender com os incidentes ocorridos e retroalimentar o processo de gestão de riscos — atualizando avaliações, corrigindo controles e prevenindo recorrências.

- **Se já existe integração formal entre os dois processos:** pular para a etapa 11.
- **Se não existe:** seguir o item 10.1 abaixo.

---

### 10.1 Fechando o ciclo — de incidentes a riscos

**O que fazer:**

- Após cada incidente, realizar análise de causa raiz e identificar qual risco não estava adequadamente controlado
- Atualizar o Risk Register com o novo nível de probabilidade — um risco que se materializou uma vez tem maior chance de ocorrer novamente
- Revisar e fortalecer os controles associados ao risco materializado
- Registrar as lições aprendidas e compartilhá-las com as áreas envolvidas
- Integrar o relatório de incidentes ao ciclo de revisão periódica de riscos

**Referência legal:** [Art. 48º da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art48) — comunicação de incidentes de segurança à ANPD e aos titulares afetados.

---

## 11. A alta gestão está envolvida e comprometida com a gestão de riscos?

Gestão de riscos sem apoio da liderança não sai do papel. Decisões sobre níveis de risco aceitáveis, investimentos em controles e priorização de ações dependem diretamente do comprometimento da alta gestão.

- **Se a liderança já está ativamente envolvida:** pular para a etapa 12.
- **Se não está:** seguir o item 11.1 abaixo.

---

### 11.1 Governança de riscos

**O que fazer:**

- Apresentar o mapa de riscos à liderança ao menos semestralmente — com linguagem de negócio, não técnica
- Definir formalmente o [apetite de risco (risk appetite)](https://en.wikipedia.org/wiki/Risk_appetite) da empresa com a participação da diretoria
- Garantir que as decisões de aceitar, transferir ou mitigar riscos críticos sejam validadas e documentadas pela liderança
- Incluir segurança da informação e gestão de riscos na agenda estratégica da empresa — não tratar como assunto exclusivo de TI
- Criar comitê ou fórum periódico de riscos com representantes das principais áreas

**Referência legal:** [Art. 6º, X da LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm#art6) — responsabilização e governança como princípio do tratamento de dados.

---

## 12. A empresa possui cultura de gestão de riscos?

Processos e ferramentas não sustentam a gestão de riscos sem uma cultura que a apoie. Quando colaboradores identificam e reportam riscos proativamente, a empresa passa de reativa para preventiva.

- **Se já existe cultura estabelecida de identificação e reporte de riscos:** encerrar o diagnóstico e avançar para a fase DO do framework.
- **Se não existe:** seguir o item 12.1 abaixo.

---

### 12.1 Construindo a cultura preventiva

**O que fazer:**

- Treinar colaboradores de todas as áreas para identificar e reportar riscos — não apenas incidentes que já ocorreram
- Criar canal simples e acessível para reporte de riscos identificados (formulário, e-mail, canal interno)
- Reconhecer e valorizar colaboradores que identificam riscos antes que se materializem
- Integrar a identificação de riscos às rotinas das áreas — reuniões de equipe, revisões de projetos, onboarding de novos processos
- Comunicar regularmente os resultados do programa de gestão de riscos — mostrar que os reportes geram ação aumenta o engajamento

---

## Riscos críticos associados à ausência de gestão de riscos

Empresas sem programa estruturado de gestão de riscos estão sujeitas a:

- Perda irreversível de dados por ausência de backup testado
- Paralisação prolongada das operações sem plano de continuidade
- Ataques de ransomware sem capacidade de recuperação
- Multas e sanções por não conformidade com a LGPD e outras regulações
- Danos reputacionais irreparáveis em caso de vazamento de dados de clientes
- Decisões de negócio tomadas sem análise de impacto e sem preparo para consequências

---

*Documento gerado como parte do framework data-trust — fase PLAN / gestão de riscos e continuidade.*
