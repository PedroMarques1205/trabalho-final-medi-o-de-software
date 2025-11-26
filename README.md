## **1. Identificação básica**

**1.1 Título do experimento:**
**Automação Robótica para Análise de Logs e Monitoramento de Sistemas**

> O título reflete o foco do experimento: utilizar ferramentas de RPA para monitorar sistemas, identificar padrões de erro e automatizar ações corretivas, substituindo tarefas manuais repetitivas.

**1.2 ID / código:**
EXP-RPA-LOG-001

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
