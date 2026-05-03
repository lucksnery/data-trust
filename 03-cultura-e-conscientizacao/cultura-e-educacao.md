# Cultura e Educação em Segurança da Informação

Este documento orienta o executor do projeto na estruturação e implementação de um programa de conscientização em segurança da informação. A abordagem é modular: cada tema traz uma explicação objetiva do que é, por que importa e como agir. O objetivo não é apenas informar colaboradores, mas construir uma cultura organizacional onde a segurança é praticada no dia a dia — e não tratada como responsabilidade exclusiva do time de TI.

---

## Módulo 1 — Fundamentos e Políticas

### 1.1 Política de uso aceitável de recursos de TI

A política de uso aceitável define as regras de como os recursos tecnológicos da empresa — computadores, celulares corporativos, sistemas, redes, softwares e dados — podem e não podem ser utilizados pelos colaboradores.

Ela existe porque o uso inadequado de recursos de TI é uma das principais portas de entrada para incidentes de segurança: instalação de softwares não autorizados, acesso a sites maliciosos, uso de dispositivos corporativos para fins pessoais sem controle, entre outros.

**O que deve estar coberto pela política:**

- Uso de equipamentos corporativos (computadores, notebooks, celulares)
- Instalação de softwares e aplicativos — o que é permitido e o que precisa de aprovação
- Acesso à internet e a sites durante o expediente
- Uso de e-mail e ferramentas de comunicação corporativas
- Armazenamento e compartilhamento de arquivos e dados
- Uso de dispositivos externos (pendrives, HDs externos)
- Acesso remoto a sistemas da empresa
- Proibições explícitas: pirataria, acesso a conteúdo ilegal, compartilhamento de credenciais

**Como agir:**

- A política deve ser apresentada no onboarding de todo novo colaborador
- O colaborador deve assinar um termo de ciência e aceite
- A política deve estar disponível em local de fácil acesso (intranet, drive interno)
- Revisão mínima anual ou sempre que houver mudança relevante no ambiente tecnológico da empresa

---

### 1.2 Classificação da informação

Nem toda informação tem o mesmo nível de sensibilidade — e tratá-las da mesma forma é um erro. A classificação da informação é o processo de definir categorias para os dados da empresa e estabelecer regras de manuseio para cada uma delas.

Sem classificação, qualquer informação pode ser compartilhada com qualquer pessoa, armazenada em qualquer lugar e descartada sem cuidado — o que representa risco direto para a empresa, seus clientes e parceiros.

**Os quatro níveis de classificação:**

| Nível | O que é | Exemplos | Quem pode acessar |
|---|---|---|---|
| **Público** | Informações que podem ser divulgadas livremente sem qualquer risco | Site institucional, comunicados de imprensa, material de marketing aprovado | Qualquer pessoa, incluindo o público externo |
| **Interno** | Informações de uso interno que não devem sair da empresa, mas sem alto grau de sensibilidade | Procedimentos internos, comunicados gerais, organogramas, políticas internas | Todos os colaboradores |
| **Confidencial** | Informações sensíveis cujo vazamento pode causar danos significativos à empresa ou a terceiros | Dados de clientes, contratos, informações financeiras, estratégias comerciais, dados de RH | Colaboradores com necessidade direta de acesso (need-to-know) |
| **Restrito** | Informações de altíssima sensibilidade, acesso extremamente limitado | Segredos industriais, fusões e aquisições, dados de acesso a sistemas críticos, investigações internas | Apenas pessoas explicitamente autorizadas |

**Como agir:**

- Ao criar ou receber um documento, identificar a qual nível ele pertence
- Respeitar as regras de compartilhamento do nível: não encaminhar um documento confidencial por e-mail sem criptografia, não publicar internamente o que é restrito
- Ao descartar, seguir o processo adequado para o nível (ver item 2.3)
- Em caso de dúvida sobre a classificação, consultar o gestor ou o time de segurança antes de agir

---

## Módulo 2 — Comportamentos Seguros no Dia a Dia

### 2.1 Gestão de senhas e autenticação

Senhas fracas ou reutilizadas são a causa de uma parcela significativa dos acessos não autorizados a sistemas corporativos. A gestão adequada de senhas é uma das medidas mais simples e mais eficazes de proteção.

**Boas práticas obrigatórias:**

- Use senhas longas e únicas para cada sistema — mínimo de 12 caracteres, combinando letras maiúsculas, minúsculas, números e símbolos
- Nunca reutilize a mesma senha em sistemas diferentes
- Nunca compartilhe sua senha com colegas, mesmo em situações de urgência
- Troque senhas imediatamente caso suspeite de comprometimento
- Não anote senhas em papéis, post-its ou arquivos de texto sem proteção
- Utilize um gerenciador de senhas para armazenar e gerar credenciais com segurança (ex: Bitwarden, 1Password, Keeper)

**Autenticação de dois fatores (2FA):**

- Ative o 2FA em todos os sistemas que oferecerem essa opção, especialmente e-mail corporativo, VPN e sistemas críticos
- Prefira aplicativos autenticadores (Google Authenticator, Microsoft Authenticator, Authy) em vez de SMS, que é menos seguro
- Nunca compartilhe códigos de autenticação com ninguém — nenhum sistema legítimo pedirá esse código por telefone ou e-mail

---

### 2.2 Mesa limpa e tela limpa

A política de mesa limpa e tela limpa garante que informações sensíveis não fiquem expostas fisicamente ou em telas quando não estão sendo utilizadas. É uma medida simples, mas frequentemente ignorada.

**Mesa limpa — ao sair da estação de trabalho:**

- Guarde documentos físicos em gavetas ou armários, especialmente os de classificação confidencial ou restrita
- Destrua rascunhos e impressões desnecessárias imediatamente (ver item 2.3)
- Não deixe senhas anotadas, crachás de acesso ou cartões sobre a mesa
- Remova pendrives, HDs externos e mídias físicas dos equipamentos

**Tela limpa — ao se ausentar do computador:**

- Bloqueie a tela sempre que se afastar, mesmo por poucos minutos (atalho: `Win + L` no Windows, `Ctrl + Cmd + Q` no Mac)
- Configure o bloqueio automático de tela em no máximo 5 minutos de inatividade
- Nunca deixe sistemas internos, e-mails ou documentos confidenciais abertos em telas visíveis a outras pessoas

---

### 2.3 Descarte seguro de informações físicas e digitais

Informações descartadas de forma inadequada são um vetor real de vazamento de dados — seja por documentos jogados no lixo sem destruição, seja por dispositivos vendidos ou descartados sem formatação adequada.

**Informações físicas:**

- Documentos com qualquer tipo de dado corporativo, mesmo que aparentemente irrelevantes, devem ser destruídos em fragmentadora antes do descarte
- Nunca jogue documentos com nomes, CPFs, contratos, dados financeiros ou qualquer dado corporativo diretamente no lixo
- Em ambientes de trabalho compartilhado, use as caixas de descarte seguro disponíveis

**Informações digitais:**

- Antes de descartar, reformatar ou transferir um dispositivo (computador, notebook, smartphone, HD externo, pendrive), realize a limpeza segura dos dados — a simples exclusão de arquivos não é suficiente
- Para dispositivos da empresa, acionar o time de TI para o processo formal de descarte ou reutilização
- E-mails e arquivos com dados sensíveis não devem ser simplesmente deletados da caixa de entrada — seguir o processo interno de descarte definido pelo time de segurança

---

### 2.4 Uso seguro de e-mail e comunicadores corporativos

O e-mail e os comunicadores corporativos são os principais canais de comunicação — e também os principais alvos de ataques de phishing, engenharia social e vazamento acidental de dados.

**Boas práticas no e-mail:**

- Verifique sempre o endereço completo do remetente antes de clicar em qualquer link ou abrir anexos
- Desconfie de e-mails com urgência excessiva, erros de português, links encurtados ou solicitações fora do padrão
- Nunca encaminhe informações confidenciais por e-mail sem criptografia ou aprovação do gestor
- Evite usar o e-mail corporativo para cadastros em serviços pessoais
- Não responda a e-mails suspeitos — em caso de dúvida, reporte ao time de segurança (ver item 3.2)

**Boas práticas em comunicadores (Slack, Teams, WhatsApp corporativo):**

- Não compartilhe senhas, tokens de acesso ou dados confidenciais por mensagem, mesmo em canais internos
- Confirme a identidade do interlocutor antes de executar qualquer solicitação recebida por mensagem, especialmente pedidos de transferência, acesso ou aprovação
- Lembre-se: comunicadores corporativos podem ser auditados — use-os de forma profissional

---

### 2.5 Redes sociais e exposição de informações corporativas

Colaboradores são, involuntariamente, uma das principais fontes de vazamento de informações corporativas nas redes sociais. Fotos de escritório, prints de sistemas, menções a clientes ou projetos, comentários sobre decisões internas — tudo isso pode comprometer a empresa.

**O que evitar:**

- Publicar fotos do ambiente de trabalho que exponham telas, documentos, quadros de tarefas ou dados de clientes
- Comentar publicamente sobre projetos, clientes, parcerias ou decisões estratégicas ainda não divulgadas oficialmente
- Reclamar de processos internos, colegas ou liderança em redes públicas
- Mencionar a empresa em contextos que possam gerar associação negativa de imagem

**O que fazer:**

- Em caso de dúvida sobre o que pode ser compartilhado publicamente, consultar o gestor ou o time de comunicação
- Entender que mesmo perfis pessoais podem associar o colaborador à empresa, e que essa associação traz responsabilidade

---

## Módulo 3 — Ameaças e Como Agir

### 3.1 Engenharia social e phishing — como reconhecer e o que fazer

Engenharia social é a manipulação psicológica de pessoas para que realizem ações ou forneçam informações que não deveriam. O phishing é a forma mais comum: e-mails, mensagens ou ligações que imitam fontes confiáveis para roubar credenciais, instalar malware ou induzir transferências.

**Como reconhecer:**

- **Urgência artificial:** "Sua conta será bloqueada em 24 horas", "Ação imediata necessária"
- **Remetente suspeito:** o nome exibido parece legítimo, mas o endereço de e-mail real é diferente (ex: suporte@empresa-segura.com.br em vez de @empresa.com.br)
- **Links disfarçados:** o texto do link parece correto, mas ao passar o cursor o endereço real é diferente
- **Anexos inesperados:** arquivos .exe, .zip, .docm ou PDFs não solicitados
- **Solicitações incomuns:** pedidos de senha, transferência financeira, acesso a sistemas ou dados fora do processo normal
- **Erros de português ou formatação diferente do padrão da empresa**

**O que fazer ao receber algo suspeito:**

1. Não clique em links, não abra anexos e não responda
2. Reporte imediatamente ao time de segurança (ver item 3.2)
3. Se já clicou ou forneceu alguma informação: reporte ainda mais rápido — ação imediata limita o dano
4. Em caso de ligação suspeita: desligue e ligue de volta para o número oficial da empresa ou pessoa

---

### 3.2 Reporte de incidentes — cultura de não punição ao erro

Um incidente de segurança reportado rapidamente pode ser contido. Um incidente escondido por medo de punição pode se tornar uma crise. A cultura de não punição ao erro é um pilar fundamental de qualquer programa de segurança maduro.

**O que deve ser reportado:**

- Clique acidental em link suspeito ou download de arquivo não intencional
- Perda ou roubo de dispositivo corporativo
- Suspeita de acesso não autorizado a conta ou sistema
- Compartilhamento acidental de informação confidencial
- Comportamento anômalo em sistema ou equipamento
- Tentativa de engenharia social recebida (mesmo que não tenha funcionado)

**Como reportar:**

- Canal direto com o time de segurança (e-mail, chamado interno ou canal dedicado — definir internamente)
- Comunicar também ao gestor imediato
- Fornecer o máximo de contexto possível: o que aconteceu, quando, por qual meio

**Princípio da não punição:**

Reportar um erro não gera punição — esconder gera. A empresa trata incidentes como oportunidades de aprendizado e melhoria, não como falha individual passível de sanção. O colaborador que reporta uma tentativa de phishing ou um clique acidental está protegendo a empresa, não se incriminando.

---

## Módulo 4 — Ambientes e Contextos Específicos

### 4.1 Uso de dispositivos pessoais (BYOD)

BYOD — Bring Your Own Device — é a prática de utilizar dispositivos pessoais (notebooks, smartphones, tablets) para acessar sistemas, e-mails ou dados corporativos. Quando não controlado, o BYOD representa um risco significativo: dispositivos pessoais raramente têm o mesmo nível de controle e proteção dos equipamentos corporativos.

**Riscos do BYOD sem controle:**

- Dispositivos sem atualização de sistema operacional ou antivírus
- Aplicativos pessoais com acesso aos mesmos dados corporativos
- Perda ou roubo sem possibilidade de bloqueio ou limpeza remota pela empresa
- Mistura de dados pessoais e corporativos sem separação clara

**O que a empresa deve definir:**

- Quais dispositivos e sistemas operacionais são permitidos para acesso corporativo
- Requisitos mínimos de segurança: senha de bloqueio, criptografia de disco, sistema operacional atualizado
- Quais sistemas e dados podem ser acessados por dispositivos pessoais
- Processo de desvinculação do dispositivo em caso de desligamento do colaborador

**O que o colaborador deve fazer:**

- Manter o dispositivo atualizado e com antivírus ativo
- Não instalar aplicativos de fontes desconhecidas
- Ativar bloqueio por senha ou biometria
- Comunicar imediatamente ao time de TI em caso de perda ou roubo

---

### 4.2 Trabalho remoto e redes seguras

O trabalho remoto expande o perímetro de segurança da empresa para fora do escritório — e com isso surgem novos vetores de risco, especialmente relacionados à rede utilizada pelo colaborador.

**Riscos do trabalho remoto:**

- Redes Wi-Fi domésticas sem configuração adequada de segurança
- Uso de redes públicas (cafeterias, aeroportos, hotéis) sem proteção
- Acesso a sistemas críticos sem VPN
- Ausência de separação física entre ambiente pessoal e profissional

**Boas práticas:**

- Utilize sempre a VPN corporativa ao acessar sistemas internos da empresa, independentemente da rede
- Em redes Wi-Fi domésticas, configure o roteador com senha forte e protocolo WPA3 ou WPA2
- Nunca acesse sistemas corporativos em redes públicas abertas sem VPN ativa
- Mantenha o roteador doméstico com firmware atualizado
- Separe o ambiente de trabalho: não use o mesmo dispositivo para trabalho e uso pessoal intenso de forma simultânea, se possível

---

### 4.3 Segurança em viagens corporativas

Dispositivos em trânsito são alvos. Em aeroportos, hotéis e eventos, as chances de roubo, perda e interceptação de comunicações aumentam consideravelmente. Cruzar fronteiras com dispositivos corporativos também exige atenção especial.

**Antes da viagem:**

- Faça backup completo dos dados do dispositivo
- Avalie se é necessário levar o dispositivo corporativo ou se um dispositivo limpo e temporário é mais adequado (especialmente para viagens internacionais a países com alto risco de espionagem)
- Instale e ative a VPN corporativa
- Habilite a opção de limpeza remota do dispositivo

**Durante a viagem:**

- Nunca deixe dispositivos corporativos sem supervisão em quartos de hotel, veículos ou locais públicos
- Não use carregadores USB públicos (USB charging stations em aeroportos e hotéis) — utilize sempre seu próprio carregador na tomada. O ataque via USB é conhecido como "juice jacking"
- Evite conectar-se ao Wi-Fi do hotel para acessar sistemas corporativos sem VPN ativa
- Em reuniões externas, atenção ao que está na tela — em locais públicos, considere o uso de filtro de privacidade (película anti-espião)
- Não discuta informações confidenciais em locais públicos (voos, lobbies, restaurantes)

**Ao cruzar fronteiras:**

- Em alguns países, autoridades podem exigir acesso a dispositivos na imigração. Consulte o time de segurança antes de viajar a destinos de risco
- Minimize os dados armazenados localmente no dispositivo — prefira acesso via nuvem corporativa com VPN quando necessário
- Ao retornar, comunique o time de TI se o dispositivo ficou fora de sua posse por qualquer período

---

## Módulo 5 — Integração e Capacitação Contínua

### 5.1 Onboarding de segurança para novos colaboradores

O onboarding é o momento mais crítico para estabelecer a cultura de segurança. Um novo colaborador que começa com boas práticas tende a mantê-las — um que começa sem nenhuma orientação cria hábitos difíceis de corrigir.

**O que deve ser coberto no onboarding de segurança:**

- Apresentação da política de uso aceitável de TI e assinatura do termo de aceite
- Explicação dos níveis de classificação da informação
- Configuração inicial segura: senha forte, 2FA, bloqueio de tela
- Apresentação dos canais de reporte de incidentes
- Instruções sobre o que pode e não pode ser compartilhado externamente
- Demonstração prática: como identificar um e-mail de phishing

**Formato sugerido:**

- Sessão síncrona de 30 a 60 minutos com o time de segurança ou TI nos primeiros dias
- Módulo assíncrono na plataforma de e-learning (ver item 6.1) a ser concluído na primeira semana
- Checklist de configurações de segurança a ser validado pelo gestor ou TI

---

### 5.2 Trilha de treinamento periódico e reciclagem

A conscientização não é um evento único — é um processo contínuo. Ameaças evoluem, colaboradores mudam de função, e boas práticas precisam ser reforçadas regularmente para se tornarem comportamento consolidado.

**Estrutura da trilha:**

- **Módulo base:** obrigatório para todos os colaboradores, cobrindo os fundamentos de segurança (módulos 1 a 3 deste documento)
- **Módulos específicos por perfil:** colaboradores com acesso a dados confidenciais, gestores, time de TI, equipe de vendas com acesso a dados de clientes
- **Reciclagem anual:** revisão do módulo base com conteúdo atualizado, cobrindo ameaças e situações novas surgidas no último período
- **Reciclagem pontual:** sempre que houver incidente relevante, mudança de política ou nova ameaça identificada no setor

**Registro e controle:**

- Registrar a conclusão de cada módulo por colaborador com data e versão do treinamento
- Gestor deve acompanhar a conclusão de sua equipe
- Treinamentos não concluídos dentro do prazo devem gerar alerta ao RH e ao gestor

---

## Módulo 6 — Atividades de Engajamento

### 6.1 Plataforma de e-learning gamificada com ranking de pontuação

Uma plataforma de e-learning gamificada transforma o treinamento obrigatório em experiência mais engajante — com pontuação, conquistas, ranking entre colegas e trilhas com progressão visível. O formato combina aprendizado com competição saudável, aumentando a taxa de conclusão e retenção do conteúdo.

**Exemplos de plataformas disponíveis no mercado:**

| Plataforma | Destaque | Modelo |
|---|---|---|
| **KnowBe4** | Especializada em security awareness, com simulações de phishing integradas | Pago |
| **Proofpoint Security Awareness** | Trilhas personalizáveis, integração com simulações | Pago |
| **Mimecast Awareness Training** | Vídeos curtos, quizzes e relatórios por departamento | Pago |
| **Cofense** | Foco em phishing e resposta a incidentes | Pago |
| **TalentLMS** | Plataforma genérica de LMS com suporte a gamificação, usada para construir trilhas customizadas | Pago (plano gratuito limitado) |
| **iSpring Learn** | Criação de cursos próprios com gamificação e relatórios | Pago |
| **Moodle** | Open source, altamente customizável, exige configuração interna | Gratuito |

---

### 6.2 Quiz mensal com ranking entre departamentos

Um quiz mensal de 5 a 10 perguntas sobre o tema de segurança do mês, distribuído por e-mail ou intranet, com ranking público entre departamentos. Simples de executar e altamente eficaz para manter o tema vivo entre os treinamentos formais.

**Como funciona:**

- Perguntas baseadas no tema da campanha mensal (ver item 6.5)
- Prazo de 5 a 7 dias úteis para responder
- Ranking divulgado internamente ao final do prazo — por departamento, não individualmente
- Pequena recompensa simbólica para o departamento vencedor (ver item 6.7)

---

### 6.3 Simulações de phishing com página educativa no clique

A simulação de phishing é a forma mais eficaz de medir e melhorar a resiliência dos colaboradores contra ataques reais. Consiste em enviar e-mails falsos, criados internamente ou via plataforma especializada, e monitorar quem clica, quem reporta e quem ignora.

**Como executar uma simulação:**

1. **Contratar um domínio de simulação:** registre um domínio que imite o da empresa com pequena variação (ex: empresa-suporte.com.br, empresasegura.com). Use registradores como Registro.br, GoDaddy ou Cloudflare.

2. **Criar o e-mail de phishing simulado:** imite comunicações reais da empresa (RH, TI, financeiro). Inclua um link apontando para o domínio de simulação. Elementos típicos: urgência, pedido de atualização de senha, confirmação de dados, boleto em anexo.

3. **Configurar a página de destino:** quando o colaborador clicar no link, em vez de uma página maliciosa, ele verá uma página educativa explicando:
   - Que acabou de ser alvo de uma simulação
   - Quais sinais indicavam que o e-mail era falso
   - O que fazer quando receber um e-mail assim de verdade
   - Link para reportar à equipe de segurança

4. **Coletar métricas:** registrar taxa de cliques, taxa de fornecimento de credenciais (se houver formulário na página) e taxa de reporte ao time de segurança.

5. **Agir sobre os resultados:**
   - Colaboradores que clicaram: encaminhar para módulo de reforço imediato na plataforma de e-learning
   - Colaboradores que reportaram corretamente: reconhecimento (ver item 6.7)
   - Resultados agregados por departamento: compartilhar com gestores para ação direcionada

6. **Frequência recomendada:** de 2 a 4 simulações por ano, variando os formatos (e-mail de RH, falsa notificação de sistema, link compartilhado por comunicador interno).

> **Atenção:** A simulação deve ser conduzida com critério ético. Colaboradores devem saber que simulações existem (sem saber quando), e os resultados individuais não devem ser usados para punição — apenas para aprendizado e reforço.

---

### 6.4 Newsletter interna periódica sobre temas de segurança

Uma newsletter interna leve, com periodicidade quinzenal ou mensal, mantém o tema de segurança presente no cotidiano dos colaboradores sem a formalidade de um treinamento. O tom deve ser acessível, com linguagem simples e conteúdo aplicável ao dia a dia.

**Lista de temas para pautar ao longo do ano:**

- Como criar e gerenciar senhas fortes — e por que seu nome + ano de nascimento não funciona
- O que é phishing e como ele evoluiu: do e-mail genérico ao ataque direcionado (spear phishing)
- Engenharia social no telefone: o golpe do "suporte técnico" e como se proteger
- Wi-Fi público: o que realmente acontece quando você se conecta sem VPN
- Classificação da informação: o que você pode e não pode compartilhar
- Segurança no home office: roteador, VPN e mesa limpa fora do escritório
- Golpes via WhatsApp e SMS (smishing): como reconhecer e o que fazer
- Senhas reutilizadas: por que uma senha vazada pode comprometer tudo
- Atualização de sistemas: por que o botão "lembrar mais tarde" é um risco
- Backup: o que acontece quando você não tem — e quando o ransomware chega
- Segurança em redes sociais: o que você publica pode comprometer a empresa
- QR Codes maliciosos: o novo vetor de phishing que passa despercebido
- Cuidados com dispositivos em viagens corporativas
- Como reportar um incidente: o que fazer nos primeiros minutos
- Deepfakes e IA em ataques: o próximo nível de engenharia social
- Segurança física: quem entrou no escritório atrás de você?

---

### 6.5 Campanha temática mensal — um tema por mês, comunicação progressiva

A campanha temática mensal concentra a comunicação interna de segurança em um único tema por mês, aprofundado progressivamente ao longo das semanas. Isso evita sobrecarga de informação e cria associação clara entre o período e o conteúdo.

**Sugestão de calendário anual:**

| Mês | Tema |
|---|---|
| Janeiro | Boas práticas para começar o ano: senhas e configurações seguras |
| Fevereiro | Engenharia social e phishing — como o ataque começa |
| Março | Classificação da informação — o que você pode compartilhar |
| Abril | Segurança no trabalho remoto e redes Wi-Fi |
| Maio | Mesa limpa, tela limpa e descarte seguro |
| Junho | BYOD — seu celular pessoal e os dados da empresa |
| Julho | Segurança em viagens corporativas |
| Agosto | Uso seguro de e-mail e comunicadores |
| Setembro | Mês da Conscientização em Cibersegurança (padrão global — outubro nos EUA, setembro no Brasil) |
| Outubro | Reporte de incidentes — cultura de não punição |
| Novembro | Redes sociais e exposição de informações corporativas |
| Dezembro | Revisão do ano: o que aprendemos e o que vem pela frente |

**Estrutura de comunicação por semana dentro do mês:**

- **Semana 1:** lançamento do tema — e-mail ou post na intranet com a contextualização
- **Semana 2:** aprofundamento — artigo na newsletter ou vídeo curto (ver item 6.8)
- **Semana 3:** quiz ou atividade prática relacionada ao tema
- **Semana 4:** encerramento — resultado do quiz, reforço da mensagem principal, reconhecimentos

---

### 6.6 Certificado de conclusão de trilhas

Certificados de conclusão de trilhas de treinamento incentivam o engajamento ao tornar o aprendizado reconhecível — tanto internamente quanto no perfil profissional do colaborador.

**Como estruturar:**

- Emitir certificado ao concluir a trilha base obrigatória e os módulos específicos de perfil
- O certificado deve conter: nome do colaborador, nome da trilha, carga horária, data de conclusão e assinatura do responsável pelo programa
- Disponibilizar em formato PDF para que o colaborador possa salvar e compartilhar no LinkedIn

**Plataformas com suporte a certificação:**

- KnowBe4, TalentLMS e iSpring emitem certificados automaticamente ao término das trilhas
- Para certificações externas de referência no mercado, indicar ao colaborador: Security+ (CompTIA), SANS Security Awareness Professional (SSAP), cursos certificados da ISACA

---

### 6.7 Recompensa simbólica para reporte de tentativas reais de phishing

Reconhecer quem reporta tentativas reais de phishing reforça dois comportamentos ao mesmo tempo: a prática de reportar e a vigilância ativa. A recompensa não precisa ser financeira — o reconhecimento público e simbólico já é altamente eficaz.

**Formatos de reconhecimento:**

- Menção pública no canal interno de comunicação (Slack, Teams, intranet) destacando o colaborador que identificou e reportou a tentativa
- Pontuação extra na plataforma de e-learning e ranking do quiz mensal
- Brinde simbólico (camisa, garrafa, voucher de valor baixo) para quem reportar ataques reais identificados pelo time de segurança como relevantes
- Destaque no relatório mensal de segurança enviado às lideranças

> Este programa é especialmente relevante para o time de tecnologia, que tem maior exposição a tentativas direcionadas e cujo reporte antecipado pode evitar incidentes de alto impacto.

---

### 6.8 Vídeos curtos internos (formato reels) sobre boas práticas

Vídeos curtos — entre 60 e 90 segundos — no formato vertical e dinâmico, produzidos internamente pelo próprio time ou em parceria com o time de marketing, são altamente eficazes para disseminar boas práticas de segurança de forma leve e memorável.

**Como produzir:**

- Roteiro simples: apresente um problema real em 15 segundos, mostre o comportamento errado, mostre o correto, encerre com a mensagem principal
- Gravação: pode ser feita com smartphone, boa iluminação e microfone de lapela — não é necessário estúdio
- Edição: CapCut, DaVinci Resolve ou Premiere para cortes rápidos, legendas automáticas e trilha de fundo
- Identidade visual: manter a linguagem visual da empresa para não parecer conteúdo externo

**Sugestões de temas para os primeiros vídeos:**

- "Você saberia identificar esse e-mail de phishing?"
- "O que acontece se você usar a mesma senha em tudo"
- "Por que você nunca deve usar o Wi-Fi do aeroporto sem VPN"
- "Mesa limpa: 30 segundos que podem salvar dados da empresa"
- "O golpe do suporte técnico — e como ele funciona"

**Distribuição:**

- Canal interno de comunicação (Slack, Teams)
- Intranet ou portal do colaborador
- Tela de boas-vindas em TVs corporativas, quando disponíveis

---

*Documento gerado como parte do framework data-trust — fase PLAN / Cultura e Educação em Segurança da Informação.*
