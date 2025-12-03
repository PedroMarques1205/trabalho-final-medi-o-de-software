## **1. Identificação básica**

**1.1 Título do experimento:**
**Automação Robótica para Análise de Logs e Monitoramento de Sistemas**

> O título reflete o foco do experimento: utilizar ferramentas de RPA para monitorar sistemas, identificar padrões de erro e automatizar ações corretivas, substituindo tarefas manuais repetitivas.

**1.2 ID / código:**
 v1.1

**1.3 Versão do documento e histórico de revisão:**

* **v1.0** – Criação inicial do plano de experimento

**1.4 Datas:**

* **Criação:** 21/11/2025
* **Última atualização:** 21/11/2025

**1.5 Autores:**

* Pedro Oliveira – Engenharia de Software – [pedrophmo1205@gmail.com](mailto:pedrophmo1205@gmail.com)

**1.6 Responsável principal:**

* Pedro Henrique Marques de Oliveira

**1.7 Projeto / produto / iniciativa relacionada:**

* Projeto de TCC de Engenharia de Software – Automatização de monitoramento e correção de logs de sistemas

## **2. Contexto e problema**

**2.1 Descrição do problema / oportunidade:**
Atualmente, a análise de logs de sistemas e a abertura de chamados de suporte são processos realizados manualmente por operadores. Esse fluxo é lento, suscetível a erros humanos e depende da disponibilidade da equipe, gerando atrasos na identificação de falhas críticas.
O experimento propõe implementar um **robô de software** capaz de:

* Coletar e analisar logs automaticamente;
* Classificar e priorizar erros críticos;
* Abrir chamados de suporte ou disparar scripts corretivos sem intervenção humana;
* Reduzir o tempo de resposta e aumentar a confiabilidade do monitoramento.

**2.2 Contexto organizacional e técnico:**

* **Ambiente de teste:** servidores de aplicação simulados, com geração de logs em tempo real;
* **Ferramentas:** Python, Robot Framework, Power Automate / N8N, APIs REST (ex.: Jira, ServiceNow);
* **Equipe:** 1 aluno de Engenharia de Software, atuando em laboratório acadêmico;
* **Objetivo técnico:** avaliar a viabilidade de automatizar a análise e correção de logs em ambientes controlados antes de aplicar em sistemas reais.

**2.3 Trabalhos e evidências prévias (internos e externos):**

* Pesquisas acadêmicas sobre aplicação de RPA em operações de TI;
* Estudos sobre automação de monitoramento de sistemas via scripts e Machine Learning;
* Experimentos prévios em laboratórios de Engenharia de Software com fluxos repetitivos automatizados;
* Relatórios internos sobre tempo médio de resolução de incidentes e erros críticos recorrentes.

**2.4 Referencial teórico e empírico essencial:**

* **RPA (Robotic Process Automation):** conceitos, frameworks e melhores práticas para automação de tarefas repetitivas;
* **Observabilidade e monitoramento:** logs, métricas e alertas;
* **Machine Learning básico:** classificação de logs e detecção de padrões de erro;
* **Integração de sistemas via API:** uso de REST APIs para automação de chamados e notificações.

# **3. Objetivos e questões (Goal / Question / Metric)**

## **3.1 Objetivo geral (modelo GQM)**

O experimento tem como objetivo **avaliar se a automação robótica (RPA)** é capaz de melhorar o processo, atualmente humana, de análise de logs, detecção de erros e acionamento de respostas, com a intenção de reduzir esforço manual e tempo de reação, sob a visão dos **operadores e equipe técnica**, dentri de um ambiente acadêmico controlado que tenta simular, da forma mais realista possível, situações de análise de logs e correção de erros em códigos fonte
 

## **3.2 Objetivos específicos**

**O1 — Detectar erros de forma mais rápida e consistente.**
**O2 — Automatizar ações corretivas e abertura de chamados.**
**O3 — Reduzir falhas humanas no processo de monitoramento.**
**O4 — Avaliar estabilidade, capacidade e integração da automaçãp com sistemas externos.**

 
## **3.3 Questões de pesquisa**

### **O1 — Detecção de erros**

**Q1.1.** O robô desenvolvido é capaz de acha os erros mais rápido do que uma pessoa que tá lendo o log na mão?
**Q1.2.** Ele consegue pegar erros críticos sem deixar passar detalhes técnicos?
**Q1.3.** O tempo de detecção fica consistente mesmo quando os logs começam a aparecer mais rápido?


### **O2 — Ações automatizadas**

**Q2.1.** A automação abre chamados mais rápido que o processo manual?
**Q2.2.** O robô executa ações corretivas sem precisar ficar pedindo atenção humana?
**Q2.3.** Quando o sistema tá mais carregado, o tempo de resposta da automação continua aceitável, ou gera gargalo?


### **O3 — Redução de falhas humanas**

**Q3.1.** A automação evita erros de operador, como por exemplo esquecer de registrar um incidente?
**Q3.2.** O robô ajuda a padronizar o processo, evitando interpretações diferentes entre operadores?
**Q3.3.** A qualidade final dos registros de incidentes melhora com a automação?


### **O4 — Estabilidade e integração**

**Q4.1.** O robô consegue rodar contínuamente sem travar?
**Q4.2.** A integração com APIs (Jira, ServiceNow etc.) funciona corretamente com a automação?
**Q4.3.** Em picos de log, o robô continua operando bem ou começa a derrapar?

 

# **3.4 Tabela GQM — Objetivos, Perguntas e Métricas**

| Objetivo | Pergunta | Métricas associadas                                                                   |
|   -- |   -- |                             - |
| **O1**   | Q1.1     | M1 – Tempo de detecção; M2 – Precisão de detecção                                     |
| **O1**   | Q1.2     | M2 – Precisão de detecção; M3 – Taxa de falsos negativos                              |
| **O1**   | Q1.3     | M1 – Tempo de detecção; M4 – Variação de desempenho                                   |
| **O2**   | Q2.1     | M5 – Tempo para abrir chamado; M6 – Tempo total até ação                              |
| **O2**   | Q2.2     | M7 – Taxa de ações automatizadas bem-sucedidas; M8 – Intervenções humanas necessárias |
| **O2**   | Q2.3     | M6 – Tempo total até ação; M9 – Degradação em carga                                   |
| **O3**   | Q3.1     | M10 – Erros humanos evitados; M11 – Conformidade com processo                         |
| **O3**   | Q3.2     | M11 – Conformidade com processo; M12 – Padronização de registros                      |
| **O3**   | Q3.3     | M12 – Padronização; M13 – Qualidade dos incidentes registrados                        |
| **O4**   | Q4.1     | M14 – Estabilidade (crashes); M4 – Variação de desempenho                             |
| **O4**   | Q4.2     | M15 – Sucesso de integração; M8 – Intervenções humanas                                |
| **O4**   | Q4.3     | M4 – Variação de desempenho; M9 – Degradação em carga                                 |

 
# **Tabela completa de métricas (descrição + unidade)**

| Código  | Métrica                              | Descrição                                                 | Unidade               |
|   - |              |                     |         |
| **M1**  | Tempo de detecção                    | Tempo entre o erro ocorrer e o robô detectar              | segundos              |
| **M2**  | Precisão de detecção                 | Percentual de erros detectados corretamente               | %                     |
| **M3**  | Taxa de falsos negativos             | Erros que o robô deixou passar                            | % / quantidade        |
| **M4**  | Variação de desempenho               | Mudança do tempo de detecção em diferentes cargas         | %                     |
| **M5**  | Tempo para abrir chamado             | Tempo entre detecção e criação do ticket                  | segundos/minutos      |
| **M6**  | Tempo total até ação                 | Tempo entre o erro ocorrer e a ação final                 | minutos               |
| **M7**  | Sucesso das ações automatizadas      | Ações realizadas sem falha                                | %                     |
| **M8**  | Intervenções humanas necessárias     | Quantidade de vezes que alguém teve que ajudar            | nº de ocorrências     |
| **M9**  | Degradação em carga                  | Quanto o sistema piora em pico                            | % de aumento no tempo |
| **M10** | Erros humanos evitados               | Diferença entre processo manual e automatizado            | nº                    |
| **M11** | Conformidade com processo            | Aderência às regras do fluxo                              | %                     |
| **M12** | Padronização de registros            | Avaliação qualitativa da consistência dos logs/incidentes | índice / nota         |
| **M13** | Qualidade dos incidentes registrados | Clareza, completude e precisão                            | nota (1–5)            |
| **M14** | Estabilidade do robô                 | Quantidade de travamentos e falhas                        | nº de eventos         |
| **M15** | Sucesso de integração                | Taxa de respostas OK das APIs                             | %                     |

 

# **4. Escopo e contexto do experimento**

## **4.1 Escopo funcional / de processo**

### **Incluído**

* Coleta e análise automática de logs.
* Classificação de erros (crítico, aviso, info…).
* Abertura automática de chamados e/ou scripts corretivos.
* Integração com APIs externas.
* Testes de carga leve e moderada.
* Avaliação de estabilidade da automação.

### **Excluído**

* Correções manuais complexas.
* Logs reais de alta criticidade empresarial.
* IA avançada para predição.
* Segurança profunda.

 

## **4.2 Contexto**

Ambiente acadêmico, equipe pequena, simulação controlada, ferramentas acessíveis (Python, RPA, N8N etc.).
Participantes com níveis diferentes de experiência — alguns ainda se atrapalhando um pouco, mas é normal.

 

## **4.3 Premissas**

* Ambiente funcionando (pela maior parte do tempo).
* Geração regular de logs.
* APIs externas disponíveis.
* Acesso do robô garantido.

 

## **4.4 Restrições**

* Tempo curto para desenvolvimento.
* Infra simples.
* Pouca mão de obra.
* Ferramentas limitadas.

 
## **4.5 Limitações previstas**

* Resultados podem não generalizar pra empresas enormes.
* Amostra pequena.
* Logs simulados não cobrem toda a realidade.

Aqui estão os tópicos organizados conforme solicitado:


## **5. Stakeholders e impacto esperado**

### **5.1 Stakeholders principais**

* Operadores/analisadores de logs.
* Equipe técnica acadêmica (orientadores/professores que avaliam a viabilidade do experimento).
* Ferramentas/serviços externos integrados via API (ex.: plataformas de chamados como Jira, ServiceNow etc.).
* Comunidade acadêmica interessada em automação de processos de TI.

### **5.2 Interesses e expectativas dos stakeholders**

* **Operadores/estudantes:** reduzir esforço manual, obter detecção mais rápida de erros e menos falhas de acompanhamento.
* **Equipe técnica acadêmica:** evidências concretas sobre viabilidade, estabilidade e ganhos reais da automação antes da aplicação em ambientes reais.
* **APIs externas:** validação de integração correta, volume de chamadas sustentado sem falhas relevantes.
* **Comunidade acadêmica:** extração de insights e contribuição para estudos sobre automatização de operações de TI.

### **5.3 Impactos potenciais no processo / produto**

* Possível aceleração do fluxo de monitoramento e abertura de tickets.
* Redução de variação e inconsistências no processo de detecção e registro.
* Aumento da carga de requisições automatizadas às APIs externas durante testes.
* Diminuição do esforço humano necessário por sessão de análise de log.
* Nenhum impacto em produção, pois o ambiente é controlado e isolado.


## **6. Riscos de alto nível, premissas e critérios de sucesso**

### **6.1 Riscos de alto nível**

* Indisponibilidade do ambiente de logs simulados.
* APIs externas fora do ar durante os testes.
* Desempenho do robô degradar excessivamente sob picos de logs.
* Possível aumento de falsos negativos se o classificador for impreciso.
* Limitações de tempo e infraestrutura restringirem a abrangência do experimento.

### **6.2 Critérios de sucesso globais (go / no-go)**

O experimento será considerado **go** se:

* O robô detectar erros mais rápido que o processo manual com variação aceitável.
* A precisão de detecção (M2) se mantiver alta com baixa taxa de falsos negativos (M3).
* A automação abrir chamados e/ou executar scripts sem demandar intervenção frequente (M7 e M8).
* A estabilidade (M14) e a integração com APIs (M15) se mantiverem funcionais mesmo em cargas moderadas.
* O tempo total até ação (M6) for significativamente inferior ao manual sem gargalos críticos (M9).

Será **no-go** se:

* O robô tiver instabilidade recorrente, baixa precisão ou gargalos críticos que invalidem a viabilidade da automação proposta.

### **6.3 Critérios de parada antecipada**

O experimento deve ser **adiado/cancelado antes de começar** se:

* O ambiente de logs não estiver operacional.
* APIs externas necessárias para integração estiverem indisponíveis.
* Faltarem recursos mínimos para instrumentação das métricas.
* O contexto do problema mudar drasticamente antes da execução.


## **7. Modelo conceitual e hipóteses**

### **7.1 Modelo conceitual do experimento**

Acredita-se que:

* A aplicação de **RPA + classificadores automatizados** reduz o tempo de detecção (M1) e aumenta a precisão (M2) em comparação ao processo manual, com menor variação e erros operacionais.
* A automação elimina atrasos dependentes de humanos e padroniza registros, o que melhora a qualidade dos incidentes (M13) e reduz falhas humanas (M10).
* Sob picos, espera-se que o desempenho degrade menos que o manual, mas pode haver algum aumento moderado no tempo (M9), que deve se manter dentro de limites aceitáveis.

### **7.2 Hipóteses formais**

| Objetivo focado              | Hipótese nula (H0)                              | Hipótese alternativa (H1 – direção esperada)                                                  |
| ---------------------------- | ----------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Detecção (O1)                | O tempo e precisão do robô são iguais ao manual | O robô detecta *mais rápido* e *com maior precisão* que o manual                              |
| Ações (O2)                   | A automação não reduz tempo nem intervenções    | A automação reduz o tempo de abertura/ação e requer *menos intervenção humana*                |
| Falhas humanas (O3)          | O número de falhas evitadas é insignificante    | A automação evita *mais falhas humanas* e aumenta a padronização/qualidade                    |
| Integração/estabilidade (O4) | O robô não sustenta cargas sem falhas           | O robô opera de forma *estável* e com *alta taxa de sucesso de integração* sob carga moderada |

### **7.3 Nível de significância e considerações de poder**

* **Nível de significância:** α = 0,05 (5%).
* **Poder estatístico:** esperado moderado, pois a amostra é pequena (laboratório acadêmico), mas suficiente para avaliar viabilidade inicial (não para generalização industrial).
* **Atenuação:** poderá ser analisada a variação de desempenho intra-sessões para compensar o baixo N amostral.

## **8. Variáveis, fatores, tratamentos e objetos de estudo**

### **8.1 Objetos de estudo**

* Arquivos de log simulados em servidores acadêmicos.
* Classificador/robô que identifica erros e dispara respostas.
* Chamadas realizadas a APIs externas de criação de tickets ou scripts corretivos.
* Sessões de análise comparativa (manual vs automatizada).

### **8.2 Sujeitos / Participantes (visão geral)**

* Estudantes/participantes simulando operadores de logs (incluindo o autor como executor do experimento).
* Níveis heterogêneos de experiência, característica que será usada como variável de controle.

### **8.3 Variáveis independentes (fatores) e níveis**

| Fator (Variável Independente) | Níveis                                                           |
| ----------------------------- | ---------------------------------------------------------------- |
| Forma de análise              | Manual / Automatizada                                            |
| Velocidade de geração de logs | Baixa / Moderada / Pico (simulado)                               |
| Integração com API            | Ativada / Desativada (quando aplicável a testes de carga locais) |

### **8.4 Tratamentos (condições experimentais)**

1. **Controle:** análise manual de logs por pessoas em diferentes cargas.
2. **T1:** robô coletando e classificando logs, sem integração com APIs.
3. **T2:** robô completo (detecção + abertura de tickets/scripts) integrado via API.
4. **T3 (cenário de carga):** T1 e T2 rodando em logs de baixa, moderada e alta velocidade para observar M4, M9 e M14.

### **8.5 Variáveis dependentes (respostas)**

| Variável Dependente                  | Métrica vinculada |
| ------------------------------------ | ----------------- |
| Tempo de detecção                    | M1                |
| Precisão da detecção                 | M2, M3, M4        |
| Tempo de abertura/ação               | M5, M6            |
| Necessidade de ajuda humana          | M8                |
| Taxa de sucesso da automação         | M7, M15           |
| Estabilidade operacional             | M14               |
| Qualidade/padronização dos registros | M12, M13          |

### **8.6 Variáveis de controle / bloqueio**

* Experiência do operador (monitorada e distribuída entre sessões).
* Infraestrutura e tipo de servidor (mantidos constantes).
* Formato dos logs (fixo no experimento).
* Lógica de priorização (fixa por versão testada).

### **8.7 Possíveis variáveis de confusão conhecidas**

* Motivação e ritmo de leitura do humano no manual.
* Cobertura da simulação não refletir 100% de casos reais.
* APIs externas sofrerem latência variável na internet.
* Limitações de hardware do laboratório influenciarem picos extremos.


## **9. Desenho experimental**

### **9.1 Tipo de desenho**

* **Completamente randomizado com blocos simples**
  (blocos = nível de experiência; tratamentos = manual vs automação T1/T2 em diferentes cargas).

### **9.2 Randomização e alocação**

* Será randomizado: **ordem das sessões, distribuição de logs entre cargas e tratamento manual vs automatizado T1/T2 (quando houver humanos em comparações).**
* A randomização prática será feita via scripts de ordem aleatória e revezamento das condições por sessão, garantindo misturas de carga e tratamento.

### **9.3 Balanceamento e contrabalanço**

* **Balanceamento:** logs e sessões distribuídos de forma equivalente para cada carga e condição.
* **Contrabalanço:** o humano não analisará sempre primeiro nem sempre o mesmo volume em picos, evitando viés de aprendizagem/cansaço entre sessões.

### **9.4 Número de grupos e sessões**

* **Grupos:** 1 grupo de operadores manuais (simulado por humanos), 1 robô em T1, 1 robô em T2.
* **Sessões por condição:** mínimo 6 a 9 rodadas no total, alternando carga e tratamento.

 # 10. População, sujeitos e amostragem

## 10.1 População-alvo

Operadores de monitoramento e profissionais de operações/DevOps/SRE que realizam análise de logs e respondem a incidentes em equipes de produto (times de médio porte) — em contexto prático representado por estudantes e técnicos de laboratório para fins de validação acadêmica.

## 10.2 Critérios de inclusão de sujeitos

* Ter experiência mínima com leitura de logs (p. ex. já ter executado troubleshooting em aplicações ou servidores).
* Idade ≥ 18 anos.
* Disponibilidade para participar de todas as sessões do experimento (tempo total estimado por sujeito: ~2–3 horas, incluindo treinamentos e entrevistas).
* Consentimento escrito informado (ter assinado termo de consentimento).

## 10.3 Critérios de exclusão de sujeitos

* Conflito de interesse direto (p. ex. pessoa envolvida no desenvolvimento do robô que vai avaliar).
* Falta de conhecimentos básicos necessários para as tarefas (por exemplo, nunca ter lido logs).
* Restrições legais ou éticas (recusa em assinar consentimento).
* Condição que impeça cumprimento do protocolo (falta de disponibilidade nas datas).

## 10.4 Tamanho da amostra planejado (por grupo)

* **Planejado (prático/acadêmico):** 12–18 participantes no total.

  * Se for desenho *within-subjects* (mesmos sujeitos fazem manual e automatizado): **n = 12–18** participantes.
  * Se for desenho *between-subjects* (grupos separados): dividir em **2 grupos** com **6–9** participantes cada.
* **Justificativa:** limite imposto por recursos laboratoriais; amostra relativamente pequena adequada para estudo de viabilidade e estimação de efeito inicial. Espera-se potência moderada; resultados servirão para estimar variância e planejar estudo maior posterior.

## 10.5 Método de seleção / recrutamento

* Amostra de conveniência: convocação entre estudantes da disciplina, monitores de laboratório e voluntários do departamento.
* Complementarmente, convite via e-mail para técnicos do laboratório (se disponível).
* Registrar motivos de recusa para avaliar viés de seleção.

## 10.6 Treinamento e preparação dos sujeitos

* Sessão de nivelamento (~45–60 min) cobrindo: objetivo do estudo, leitura rápida de logs (formato usado), uso do ambiente de teste, instruções para tarefas manuais e checklist do que registrar.
* Material entregue por escrito: manual rápido (1–2 páginas), roteiro da sessão, formulário de contato para dúvidas.
* Teste prático curto (5–10 min) para confirmar compreensão; se necessário, repetir trecho do treinamento.

# 11. Instrumentação e protocolo operacional

## 11.1 Instrumentos de coleta

* **Gerador de logs controlado** (scripts que emitem eventos em diferentes taxas e padrões): fonte primária de estímulos.
* **Robô/automação (versões T1/T2)** instrumentado para coletar métricas internas (timestamp de recebimento, decisão, ações, respostas API).
* **Sistema de coleta de métricas central** (script/serviço que grava M1..M15 em banco de dados/CSV).
* **Formulários pré/per/post-experimento** (questionários eletrônicos): perfil do participante, percepção de workload (NASA-TLX curto), satisfação, qualidade percebida dos registros.
* **Planilha de observação/registro do experimento** (researcher log) para anotações de eventos imprevistos.
* **Screen recording / video opcional** (com consentimento) para auditoria de comportamento humano durante tarefas manuais.
* **Logs das APIs externas** (respostas HTTP, latência) para auditoria de integração.
* **Questionário semiestruturado de entrevista** para opinião qualitativa pós-sessão.

## 11.2 Materiais de suporte (instruções, guias)

* Instrução passo-a-passo em PDF para participantes (cenario, tarefas, critérios de sucesso).
* Guia do experimentador (checklist de preparação do ambiente, sequência de passos a executar, backup).
* Fichas rápidas de decisão (o que fazer em caso de falha técnica, cancelamento de rodada).
* Script de consentimento e formulário de coleta de dados pessoais (anônimos quando possível).

## 11.3 Procedimento experimental (protocolo – visão passo a passo)

1. **Convite e triagem:** confirmar elegibilidade e agendar.
2. **Consentimento informado:** ler e assinar; explicar anonimização.
3. **Pré-questionário:** perfil, experiência, expectativa.
4. **Treinamento:** 45–60 min (ver 10.6).
5. **Sessão piloto curta (se aplicável):** testar ambiente com 1–2 runs (ver 11.4).
6. **Execução – fase A (baseline manual):** participante analisa logs gerados por X minutos/rodadas; registra incidentes e tempo até identificação; experimentador registra métricas. Ordem das cargas randomizada.
7. **Pausa breve (5–10 min).**
8. **Execução – fase B (automação):** iniciar robô na condição correspondente (T1/T2); coletar métricas automáticas (detecção, ações, latência). Em desenho within-subjects alternar ordem (contrabalançar) para evitar ordem fixa.
9. **Registro de eventos excepcionais:** anotar quedas, erros do robô, falhas de API.
10. **Pós-questionário e entrevista semiestruturada:** avaliar percepção, qualidade dos registros, confiança na automação.
11. **Despedida e compensação (se aplicável).**
12. **Backup de dados:** exportar logs, planilhas e gravações para repositório seguro.

## 11.4 Plano de piloto (escopo e critérios de ajuste)

* **Piloto:** 2–3 participantes (preferencialmente com perfis distintos) antes das execuções formais.
* **Objetivos:** validar gerador de logs, mensuração de tempos, clareza das instruções, infraestrutura de coleta (scripts, banco CSV).
* **Critérios de ajuste:** corrigir falhas técnicas, ajustar templates de formulários, tempo por sessão, e clarificar instruções se ≥1 participante reportar confusão. Após piloto, registrar mudanças e reexecutar outro piloto rápido se mudanças forem substanciais.

# 12. Plano de análise de dados (pré-execução)

## 12.1 Estratégia geral de análise

* **Quantitativa:** comparar métricas primárias (M1 M2 M5 M6 M7 M8 M14 M15) entre condições (manual vs automação; e entre níveis de carga). Responder às questões Q1.x–Q4.x relacionando cada métrica correspondente.

  * Ex.: Para Q1.1 comparar M1 (tempo de detecção) entre manual e automatizado.
* **Qualitativa:** analisar respostas abertas e entrevistas para entender causas de falsos positivos/negativos, confiança do usuário e sugestões de melhoria.
* Fazer análises descritivas (médias, medianas, desvios, boxplots) e inferenciais (ver 12.2).
* Reportar intervalos de confiança e tamanhos de efeito além de p-values.
* Realizar análises de sensibilidade (com e sem outliers; com dados imputados vs exclusão) para verificar robustez.

## 12.2 Métodos estatísticos planejados

* **Verificações preliminares:** checar normalidade (Shapiro-Wilk) e homogeneidade de variância (Levene).
* **Comparações entre duas condições (within-subjects):** teste pareado t-test (se normal) ou Wilcoxon signed-rank (não paramétrico).
* **Comparações entre grupos independentes (between-subjects):** t-test independente ou Mann-Whitney U.
* **Comparações múltiplas (mais de 2 níveis, ex.: baixa/moderada/pico):** ANOVA de medidas repetidas (com correção de esfericidade) ou Friedman test (não paramétrico). Para between-subjects, ANOVA one-way ou Kruskal-Wallis.

## 12.3 Tratamento de dados faltantes e outliers

* **Dados faltantes:**

  * Se faltarem dados esporádicos (p. ex. um valor de tempo), usar **imputação simples** (mediana por condição) para análises descritivas e executar **análise de sensibilidade** com exclusão completa (listwise).
  * Se participante tiver >20% das medidas principais faltando, excluir o participante das análises quantitativas principais e documentar motivos.
* **Outliers:**

  * Definir outliers com antecedência: valores além de **3 z-scores** da média ou fora de **1.5×IQR**.
  * Analisar resultados com e sem outliers; reportar ambos e justificar qualquer exclusão. Não remover outliers automaticamente — só se houver evidência de erro de medição ou evento extraordinário não representativo (p. ex. falha técnica).

## 12.4 Plano de análise para dados qualitativos

* **Abordagem:** análise temática (thematic analysis).
* **Etapas:** transcrever entrevistas; leitura exploratória; codificação inicial (open coding); agrupar códigos em categorias temáticas; revisar e definir temas finais.
* **Confiabilidade:** pelo menos **2 codificadores** independentes codificarão uma amostra (20–30%) dos dados para medir **acordo inter-avaliador** (Cohen’s kappa). Em caso de divergência, discutir até consenso e refinar código.
* **Apresentação:** extrair citações representativas (anonimizadas) para ilustrar temas; relacionar temas às métricas quantitativas (triangulação).


