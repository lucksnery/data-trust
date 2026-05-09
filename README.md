# data-trust

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-blue)
![Licença](https://img.shields.io/badge/licença-MIT-green)
![Tema](https://img.shields.io/badge/tema-governança%20de%20dados-informational)
![LGPD](https://img.shields.io/badge/LGPD-Lei%2013.709%2F2018-blueviolet)
![Framework](https://img.shields.io/badge/framework-PDCA-orange)

> Framework estruturado para governança de dados, adequação à LGPD e segurança da informação — do diagnóstico inicial à melhoria contínua.

---

## 📌 Sobre o Projeto

O **data-trust** é um framework prático e completo que orienta empresas na implementação de um programa de governança de dados e segurança da informação. O projeto nasceu da necessidade real de oferecer um caminho estruturado para organizações que precisam se adequar à LGPD, controlar acessos, educar colaboradores e gerenciar riscos — sem depender de consultorias caras ou ferramentas complexas.

A abordagem é sequencial e orientada à execução: cada módulo começa com um diagnóstico do cenário atual, identifica lacunas e direciona para ações concretas com responsáveis, prazos e referências legais. O executor não precisa saber o que fazer — o framework mostra o caminho.

---

## ⚠️ Problema

Muitas empresas operam sem qualquer estrutura de governança de dados, expondo-se a riscos legais, operacionais e reputacionais que poderiam ser evitados:

- Sem controle sobre quem acessa quais dados e sistemas
- Sem mapeamento dos dados pessoais coletados e tratados
- Sem padrões, políticas e processos formalizados
- Sem plano de resposta a incidentes de segurança
- Baixa visibilidade sobre riscos e nível de conformidade
- Colaboradores sem treinamento sobre segurança da informação e LGPD
- Ausência de DPO nomeado ou canal de atendimento ao titular

---

## 💡 Solução

Um framework baseado no ciclo **PDCA** que combina guias de diagnóstico e ação, templates de documentos, checklists práticos e uma interface visual de acompanhamento de progresso.

O data-trust é estruturado em quatro grandes módulos, cada um com seu guia principal, materiais de apoio e exemplos práticos:

| Módulo | O que cobre |
|---|---|
| **01 — Adequação à LGPD** | Diagnóstico completo de conformidade com a Lei nº 13.709/2018, desde presença digital até plano de resposta a incidentes |
| **02 — Controle de Acessos** | Implementação de RBAC, MFA, gestão de identidades, ciclo de vida de acessos e modelo Zero Trust |
| **03 — Cultura e Educação** | Políticas de uso, classificação da informação, treinamentos, simulações de phishing e campanhas de conscientização |
| **04 — Gestão de Riscos** | Metodologia de gestão de riscos, backup, BCP, Disaster Recovery, proteção contra malware e segurança em nuvem |

---

## 🔄 Ciclo PDCA

O projeto segue o modelo de melhoria contínua, garantindo que a governança de dados seja tratada como um processo evolutivo — não uma ação pontual.

```
PLAN → DO → CHECK → ACT → (reinicia)
```

| Fase | O que acontece |
|---|---|
| **Plan** | Diagnóstico do cenário atual, mapeamento de dados, identificação de lacunas e definição das ações de adequação |
| **Do** | Implementação de políticas, controles de acesso, treinamentos e planos de resposta a incidentes |
| **Check** | Monitoramento dos processos, auditorias internas e validação das práticas adotadas |
| **Act** | Ajustes, correções e melhorias com base nos resultados e riscos identificados |

---

## 🗂️ Estrutura do Projeto

```
/01-adequacao-lgpd
    adequacoes-lgpd.md            ← guia principal de diagnóstico e ação
    /exemplos                     ← prints e referências visuais de boas práticas
    /referencias                  ← links e materiais externos de apoio
    /templates
        modelo-politica-privacidade.md
        modelo-nomeacao-dpo.md
        modelo-inventario-dados.md
        modelo-dpa.md
        modelo-politica-retencao-descarte.md
        playbook-resposta-incidentes.md

/02-controle-de-acessos
    controle-de-acessos.md        ← guia principal (modelo Zero Trust)

/03-cultura-e-conscientizacao
    cultura-educacao.md           ← guia principal de conscientização

/04-gestao-de-riscos
    gestao-de-riscos.md           ← guia principal de riscos e continuidade

/05-progresso
    index.html                    ← dashboard interativo de progresso (GitHub Pages)
```

---

## 📋 O que está incluído em cada módulo

### 🔒 01 — Adequação à LGPD

Guia sequencial de diagnóstico e ação baseado na [Lei nº 13.709/2018](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm), cobrindo:

- Presença digital: banner de cookies, política de privacidade, formulários e canal do titular
- DPO: nomeação formal, publicação do contato e atribuições operacionais
- Mapeamento de dados: inventário (data mapping), bases legais, retenção e descarte
- Compartilhamento com terceiros: inventário de operadores e DPA
- Controles de acesso e plano de resposta a incidentes
- Treinamento e conscientização dos colaboradores

**Templates incluídos:**
- Modelo de Política de Privacidade
- Modelo de Nomeação do DPO
- Inventário de Dados (data mapping) com exemplos por processo
- Modelo de DPA (Data Processing Agreement)
- Política de Retenção e Descarte de Dados
- Playbook de Resposta a Incidentes

---

### 👤 02 — Controle de Acessos

Guia baseado no modelo [Zero Trust](https://en.wikipedia.org/wiki/Zero_trust_security_model) e nos frameworks [ISO 27001](https://pt.wikipedia.org/wiki/ISO/IEC_27001), [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) e [CIS Controls](https://www.cisecurity.org/cis-controls), cobrindo:

- Mapeamento de acessos e Matriz de Controle de Acessos
- Perfis por função — modelo RBAC (Role-Based Access Control)
- Princípio do menor privilégio
- Controle de acesso físico a áreas restritas
- Política de senhas e autenticação multifator (MFA)
- Gestão de contas privilegiadas (PAM)
- Ciclo de vida de acessos: onboarding, revisão periódica e offboarding
- Controle de acesso em ambientes cloud e plataformas SaaS
- Política formal de controle de acessos

---

### 🎓 03 — Cultura e Educação em Segurança da Informação

Programa completo de conscientização em segurança da informação, cobrindo:

- Política de uso aceitável de recursos de TI
- Classificação da informação (público, interno, confidencial, restrito)
- Gestão de senhas e autenticação multifator
- Mesa limpa e tela limpa
- Descarte seguro de informações físicas e digitais
- Uso seguro de e-mail e comunicadores corporativos
- Redes sociais e exposição de informações corporativas
- Engenharia social e phishing — como reconhecer e o que fazer
- Reporte de incidentes e cultura de não punição ao erro
- BYOD — uso de dispositivos pessoais
- Trabalho remoto e redes seguras
- Segurança em viagens corporativas
- Onboarding de segurança para novos colaboradores
- Trilha de treinamento periódico e reciclagem

**Atividades proativas incluídas:**
- Simulações de phishing com domínio falso e página educativa no clique (guia com GoPhish)
- Newsletter interna com lista de 16 temas sugeridos
- Campanha temática mensal com calendário anual completo
- Plataformas de e-learning gamificadas — comparativo de opções gratuitas e pagas
- Recompensa simbólica por reporte de phishing real
- Vídeos curtos internos no formato reels

---

### ⚠️ 04 — Gestão de Riscos e Continuidade

Guia baseado em [ISO/IEC 27005](https://www.iso.org/standard/75281.html) e [NIST SP 800-30](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final), cobrindo:

- Metodologia de gestão de riscos (qualitativa/quantitativa)
- Inventário e classificação de ativos críticos
- Identificação de ameaças e vulnerabilidades
- Risk Register com critérios de probabilidade e impacto
- Matriz de risco com tabela visual de criticidade
- Apetite de risco e governança com a liderança
- Estratégias de tratamento: mitigar, aceitar, transferir, evitar
- **Backup:** tipos (completo, incremental, diferencial), regra 3-2-1, RTO/RPO e testes de restauração
- **BCP (Business Continuity Plan):** BIA, processos críticos, RTO/RPO e comunicação em crise
- **Disaster Recovery:** estratégias cold, warm e hot standby com tabela comparativa
- Gestão de vulnerabilidades e patches
- Proteção multicamada contra malware e ransomware
- Segurança em ambientes de nuvem (AWS, Azure, GCP)
- Integração entre gestão de riscos e resposta a incidentes
- Cultura de gestão de riscos e conscientização

---

### 📊 05 — Dashboard de Progresso

Interface web interativa em HTML puro, hospedável no **GitHub Pages**, com:

- Hero section com identidade visual do projeto
- Barra de progresso geral fixa que acompanha o scroll
- 4 cards de módulos com barras de progresso individuais, contadores e alertas de itens obrigatórios em aberto
- Checklists interativos completos dos 4 módulos (57 itens no total)
- Tags de prioridade (obrigatório, recomendado, opcional) com tooltips explicativos ao passar o mouse
- Animação de fogos e confetes ao atingir 100% de conclusão

---

## 🚀 Por onde começar

**Para usar o framework completo:**

1. Clone ou faça fork do repositório
2. Acesse `/01-adequacao-lgpd/adequacoes-lgpd.md` e responda o diagnóstico sequencialmente
3. Use os templates em `/templates` para criar os documentos que o guia solicitar
4. Avance para `/02-controle-de-acessos`, `/03-cultura-e-conscientizacao` e `/04-gestao-de-riscos` na ordem
5. Acompanhe o progresso pelo dashboard em `/05-progresso/index.html`

**Para usar apenas o dashboard:**

1. Abra `/05-progresso/index.html` no navegador ou acesse via GitHub Pages
2. Marque os itens conforme a empresa implementa cada controle
3. O progresso é visual e em tempo real — sem necessidade de cadastro ou backend

---

## 🎯 Público-Alvo

- Empresas em processo de adequação à LGPD
- Profissionais de governança, dados, compliance e segurança da informação
- DPOs (Encarregados de Proteção de Dados) e consultores de privacidade
- Times operacionais e de tecnologia responsáveis por implementar controles
- Consultores e analistas que acompanham clientes no processo de conformidade

---

## 📐 Referências e Frameworks Utilizados

| Referência | Aplicação no projeto |
|---|---|
| [LGPD — Lei nº 13.709/2018](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) | Base legal do módulo de adequação |
| [ISO/IEC 27001:2022](https://pt.wikipedia.org/wiki/ISO/IEC_27001) | Controles de segurança da informação e acesso |
| [ISO/IEC 27005](https://www.iso.org/standard/75281.html) | Gestão de riscos em segurança da informação |
| [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | Controles de acesso e segurança |
| [NIST SP 800-30](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final) | Avaliação de riscos |
| [CIS Controls v8](https://www.cisecurity.org/cis-controls) | Controles prioritários de segurança |
| [Zero Trust Architecture — NIST SP 800-207](https://csrc.nist.gov/publications/detail/sp/800-207/final) | Modelo orientador do controle de acessos |
| [PDCA — ISO 9001](https://pt.wikipedia.org/wiki/Ciclo_PDCA) | Estrutura de melhoria contínua do framework |

---

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

---

*data-trust — framework de governança de dados, adequação à LGPD e segurança da informação.*
