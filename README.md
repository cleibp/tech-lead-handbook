# 📘 Tech Lead Handbook
> **Guia prático de Engenharia de Software, Arquitetura e Liderança Técnica**
> 
> *Conhecimento compartilhado para profissionais que desejam evoluir de desenvolvedores para referências técnicas e líderes de engenharia.*

---

| Metadado | Detalhe |
| :--- | :--- |
| **Idioma** | Português (Brasil) · `pt-BR` |
| **Formato** | Markdown |
| **Plataforma** | GitHub / Documentation Hub |

---

## 📌 Sumário

- [Módulo 1: O Papel do Tech Lead](#-módulo-1-o-papel-do-tech-lead)
  - [1. O que significa ser um Tech Lead para você?](#1-o-que-significa-ser-um-tech-lead-para-você)
  - [2. Qual a diferença entre um Tech Lead e um desenvolvedor sênior?](#2-qual-a-diferença-entre-um-tech-lead-e-um-desenvolvedor-sênior)
- [Módulo 2: Arquitetura & Decisões Técnicas](#-módulo-2-arquitetura--decisões-técnicas)
  - [3. Como você toma uma decisão arquitetural?](#3-como-você-toma-uma-decisão-arquitetural)
  - [4. Você prefere monólito ou microsserviços?](#4-você-prefere-monólito-ou-microsserviços)
  - [5. Como você lida com dívida técnica?](#5-como-você-lida-com-dívida-técnica)
- [Módulo 3: Gestão de Pessoas, Conflitos & Autonomia](#-módulo-3-gestão-de-pessoas-conflitos--autonomia)
  - [6. Como você resolve um conflito técnico entre dois desenvolvedores?](#6-como-você-resolve-um-conflito-técnico-entre-dois-desenvolvedores)
  - [7. Como você lida com um desenvolvedor que discorda de você?](#7-como-você-lida-com-um-desenvolvedor-que-discorda-de-você)
  - [8. Como você faz code review?](#8-como-você-faz-code-review)
  - [9. O que você faz quando um desenvolvedor entrega uma solução tecnicamente ruim?](#9-o-que-você-faz-quando-um-desenvolvedor-entrega-uma-solução-tecnicamente-ruim)
  - [10. Como você garante qualidade técnica sem virar um gargalo?](#10-como-você-garante-qualidade-técnica-sem-virar-um-gargalo)
- [Módulo 4: Design de Sistemas, Escalabilidade & Observabilidade](#-módulo-4-design-de-sistemas-escalabilidade--observabilidade)
  - [11. Como você conduziria a arquitetura de uma nova API?](#11-como-você-conduziria-a-arquitetura-de-uma-nova-api)
  - [12. Como você projetaria uma API que precisa suportar milhões de requisições?](#12-como-você-projetaria-uma-api-que-precisa-suportar-milhões-de-requisições)
  - [13. Quando você usaria Kafka?](#13-quando-você-usaria-kafka)
  - [14. Kafka ou SQS?](#14-kafka-ou-sqs)
  - [15. Como você desenharia uma aplicação resiliente?](#15-como-você-desenharia-uma-aplicação-resiliente)
  - [16. Como você trabalha com observabilidade?](#16-como-você-trabalha-com-observabilidade)
  - [17. Um sistema está apresentando lentidão. O que você faria?](#17-um-sistema-está-apresentando-lentidão-o-que-você-faria)
  - [18. Como você lida com incidentes em produção?](#18-como-você-lida-com-incidentes-em-produção)
- [Módulo 5: Processos, Produto & Métricas](#-módulo-5-processos-produto--métricas)
  - [19. O que é mais importante: entregar rápido ou entregar com qualidade?](#19-o-que-é-mais-importante-entregar-rápido-ou-entregar-com-qualidade)
  - [20. Como você mede o sucesso de um time de engenharia?](#20-como-você-mede-o-sucesso-de-um-time-de-engenharia)
  - [21. Como você trabalha com produto?](#21-como-você-trabalha-com-produto)
  - [22. O Product Manager pede algo tecnicamente muito ruim. O que você faz?](#22-o-product-manager-pede-algo-tecnicamente-muito-ruim-o-que-você-faz)
  - [23. Como você prioriza uma melhoria técnica?](#23-como-você-prioriza-uma-melhoria-técnica)
- [Módulo 6: Perfil Pessoal & Pitch Profissional](#-módulo-6-perfil-pessoal--pitch-profissional)
  - [24. Como você desenvolve pessoas?](#24-como-você-desenvolve-pessoas)
  - [25. Qual é seu maior ponto forte como Tech Lead?](#25-qual-é-seu-maior-ponto-forte-como-tech-lead)
  - [26. Qual é seu ponto fraco?](#26-qual-é-seu-ponto-fraco)
  - [27. Você ainda programa como Tech Lead?](#27-você-ainda-programa-como-tech-lead)
  - [28. Você prefere ser especialista ou generalista?](#28-você-prefere-ser-especialista-ou-generalista)
  - [29. Como você lida com pressão?](#29-como-você-lida-com-pressão)
  - [30. Por que deveríamos contratar você como Tech Lead?](#30-por-que-deveríamos-contratar-você-como-tech-lead)

---

## 🧠 Módulo 1: O Papel do Tech Lead

### 1. O que significa ser um Tech Lead para você?

> Tech Lead não é simplesmente a pessoa que mais programa ou que possui mais conhecimento técnico no time. É quem dá direção técnica, apoia decisões estratégicas e garante o alinhamento com os objetivos do negócio.

O Tech Lead opera no equilíbrio de **três dimensões fundamentais**:
* **Tecnologia:** Garantir padrões, reduzir riscos e desenhar a arquitetura correta.
* **Pessoas:** Desenvolver o time, dar contexto e promover autonomia.
* **Negócio:** Traduzir necessidades funcionais em soluções viáveis e sustentáveis.

---

### 2. Qual a diferença entre um Tech Lead e um desenvolvedor sênior?

> O desenvolvedor sênior resolve problemas complexos de forma independente. O Tech Lead amplia o foco para o **sistema como um todo**, avaliando o impacto das decisões no time e na empresa.

Ao encarar um problema, o Tech Lead deve fazer perguntas sistêmicas:
* *Essa arquitetura escala?*
* *Essa decisão aumenta nossa dívida técnica?*
* *Como isso impactará outros serviços e qual o custo operacional?*
* *O time conseguirá manter essa solução com facilidade?*

---

## 📐 Módulo 2: Arquitetura & Decisões Técnicas

### 3. Como você toma uma decisão arquitetural?

> Evito decisões baseadas em preferência pessoal ou "hypes" tecnológicos. Arquitetura deve ser orientada a contexto e resolução de problemas reais.

**Processo de decisão:**
1. Mapeamento de requisitos funcionais e não funcionais (*volume, disponibilidade, segurança, custos e capacidade do time*).
2. Avaliação de alternativas, *trade-offs* e riscos.
3. Formalização via **ADR (Architecture Decision Record)**, documentando contexto, opções descartadas, decisão final e suas consequências.

---

### 4. Você prefere monólito ou microsserviços?

> 💡 **Diretriz:** Não existe resposta universal. Arquitetura é consequência do problema, não o contrário.

* **Monólito Modular:** Excelente ponto de partida. Evita a complexidade operacional precoce (*observabilidade distribuída, tracing, consistência de dados e deploys complexos*).
* **Microsserviços:** Recomendável apenas diante de necessidades reais de escalabilidade independente, limites explícitos de domínio, autonomia de times distintos ou requisitos operacionais heterogêneos.

---

### 5. Como você lida com dívida técnica?

> Nem toda dívida técnica é ruim; algumas são decisões conscientes para acelerar valor ao negócio. O perigo é a **perda de controle**.

**Estratégia de Gestão:**
* **Classificação por Impacto:** Avaliar risco operacional, falhas de segurança, gargalos de performance e perda de produtividade.
* **Visibilidade:** Converter dívidas em itens visíveis no backlog, priorizando o risco relativo ao negócio.
* **Justificativa Quantitativa:** Utilizar dados de incidentes e métricas de sistema para demonstrar o custo real da não resolução.

---

## 👥 Módulo 3: Gestão de Pessoas, Conflitos & Autonomia

### 6. Como você resolve um conflito técnico entre dois desenvolvedores?

> Elimino discussões baseadas em opinião pessoal trazendo o debate para **critérios objetivos**.

**Matriz de Avaliação de Soluções:**
* Manutenibilidade e Legibilidade
* Performance e Segurança
* Complexidade de Implementação e Custos
* Experiência e Curva de Aprendizado do Time

*Dica:* Quando necessário, constrói-se uma pequena **POC (Proof of Concept)**. O objetivo não é determinar quem está certo, mas identificar a solução ideal para o produto.

---

### 7. Como você lida com um desenvolvedor que discorda de você?

> Um ambiente onde o Tech Lead nunca é questionado é um sinal de alerta de falta de segurança psicológica.

* **Escuta Ativa:** Analisar os argumentos e as evidências apresentadas.
* **Flexibilidade:** Se a proposta do desenvolvedor for superior, mudo minha decisão sem hesitar.
* **Princípio:** Liderar não é ter a palavra final, mas garantir que a melhor decisão seja tomada pelo time.

---

### 8. Como você faz code review?

> Code review deve ser uma ferramenta de **garantia de qualidade e compartilhamento de conhecimento**, nunca uma avaliação ad hominem.

* **Checklist Humano:** Corretude lógica, segurança, manutenibilidade, cobertura de testes e aderência arquitetural.
* **Automação:** Delegar regras de sintaxe, formatação e falhas estáticas para *linters*, pipelines de CI e ferramentas como SonarQube.

---

### 9. O que você faz quando um desenvolvedor entrega uma solução tecnicamente ruim?

1. **Investigar o Contexto:** Entender o motivo da escolha (pode haver restrições de prazo ou escopo desconhecidas).
2. **Alinhamento Individual:** Explicar os riscos da abordagem em um alinhamento 1:1 e desenhar alternativas em conjunto.
3. **Análise Sistêmica:** Avaliar se a falha é pontual ou indica necessidade de melhoria na documentação, nos *guidelines* ou nos treinamentos do time.

---

### 10. Como você garante qualidade técnica sem virar um gargalo?

> O Tech Lead não deve ser o único aprovador de mudanças ou tomador de decisões.

---

## 🚀 Módulo 4: Design de Sistemas, Escalabilidade & Observabilidade

### 11. Como você conduziria a arquitetura de uma nova API?

| Camada | Elementos Chave |
| :--- | :--- |
| **Interface / Contrato** | Padrões REST (ou gRPC/GraphQL), versionamento, auth (OAuth2/JWT) e idempotência. |
| **Aplicação** | Separação clara de responsabilidades, Clean/Hexagonal Architecture e persistência. |
| **Infraestrutura** | Conteinerização (Docker/K8s), estratégias de cache, bancos de dados e filas. |
| **Operação** | Telemetria (Logs estruturados, Métricas, Traces) e esteiras robustas de CI/CD. |

---

### 12. Como você projetaria uma API que precisa suportar milhões de requisições?

> ⚠️ Escalabilidade deve ser baseada em **evidências e testes de carga**, não em suposições.

* **Estratégias de Borda & Carga:** CDNs para assets estáticos, *Load Balancers* e Escalabilidade Horizontal.
* **Otimização de Dados:** Aplicação de Caches (ex: Redis), read-replicas de banco de dados, particionamento e otimização avançada de queries.
* **Assincronismo:** Desacoplamento de operações pesadas por meio de mensageria e queues.
* **Métricas Principais:** Acompanhar latência (p95/p99), *throughput*, taxas de erro e saturação.

---

### 13. Quando você usaria Kafka?

> O Kafka se destaca em ecossistemas de **Event Streaming**, alto volume de dados e necessidade de múltiplos consumidores desacoplados.

* **Usar:** Processamento de eventos assíncronos em larga escala, *replay* de mensagens, retenção e desacoplamento severo.
* **Não Usar:** Chamadas simples e síncronas requisição/resposta (onde REST/gRPC resolvem com menor complexidade).

---

### 14. Kafka ou SQS?

* **AWS SQS:** Excelente opção para gerenciamento simplificado de filas de mensagens, processamento de tarefas assíncronas e baixa complexidade operacional no ecossistema AWS.
* **Apache Kafka:** Ideal para *log* de eventos distribuído, ordenação estrita por partição, alta retenção histórica e múltiplos *subscribers* consumindo o mesmo fluxo.

---

### 15. Como você desenharia uma aplicação resiliente?

* **Circuit Breakers & Retries:** Implementar *retries* acompanhados de *backoff exponencial* (atentando-se para evitar *retry storms*) e *Circuit Breakers*.
* **Isolamento de Falhas:** Uso de *Dead-Letter Queues (DLQ)* e degradação graciosa (*graceful degradation*).
* **Verificações:** Realização de *Health Checks* ativos e rotinas limpas de desligamento (*graceful shutdown*).

---

### 16. Como você trabalha com observabilidade?

> **Logs, Métricas e Traces** são os pilares indispensáveis da observabilidade moderna.

* **Logs:** Centralizados e estruturados (ex: formato JSON) com IDs de correlação (*Correlation IDs*).
* **Métricas:** Painéis focados nos indicadores chave (Latência, Erros, Tráfego e Saturação).
* **Tracing:** Rastreamento distribuído de ponta a ponta em arquiteturas baseadas em microsserviços.
* **Alertas:** Direcionados aos **sintomas com impacto real no negócio**, evitando a fadiga de alertas por variações irrelevantes.

---

### 17. Um sistema está apresentando lentidão. O que você faria?

```
[1. Coleta de Evidências] ➔ [2. Formulação de Hipótese] ➔ [3. Aplicação do Fix] ➔ [4. Validação]
```
1. **Análise de Métricas:** Inspecionar APM, logs, consumo de banco de dados, latência de rede e dependências externas antes de alterar qualquer código.
2. **Isolamento do Gargalo:** Identificar o ponto exato de contenção (ex: *queries* travadas, vazamento de memória ou esgotamento de conexões).
3. **Resolução e Monitoramento:** Aplicar a correção e auditar a curva de métricas para garantir o reestabelecimento do padrão normal.

---

### 18. Como você lida com incidentes em produção?

* **Fase 1: Estabilização (Mitigação Imediata)**  
  O foco é **reduzir o impacto ao usuário final** (ex: *rollback*, acionamento de *feature flags* ou limitação de tráfego). A busca por culpados é proibida.
* **Fase 2: Análise e Causa Raiz**  
  Investigação pós-estabilização para entender o problema técnico e falhas em nossos mecanismos de prevenção.
* **Fase 3: Post-Mortem Blameless**  
  Documentação transparente sobre o aprendizado, gerando ações corretivas preventivas no backlog.

---

## 📈 Módulo 5: Processos, Produto & Métricas

### 19. O que é mais importante: entregar rápido ou entregar com qualidade?

> Velocidade e qualidade não são mutuamente exclusivas; o objetivo é entregar **valor rapidamente com o nível de qualidade adequado ao risco**.

* **Projetos Experimentais/POCs:** Toleram maior risco e priorizam velocidade de validação.
* **Sistemas Críticos/Financeiros:** Exigem rigor máximo de qualidade, automação de testes e baixa tolerância a falhas.

---

### 20. Como você mede o sucesso de um time de engenharia?

Evito utilizar volume de linhas de código ou tarefas como métricas de performance. Priorizo **Métricas DORA** e impacto estratégico:

* **Lead Time for Changes** (Tempo de ciclo)
* **Deployment Frequency** (Frequência de implantação)
* **Change Failure Rate** (Taxa de falha em alterações)
* **Mean Time to Restore (MTTR)** (Tempo médio de recuperação)
* **Indicadores Qualitativos:** Previsibilidade de entregas, satisfação da equipe e geração de valor de negócio.

---

### 21. Como você trabalha com produto?

> Tech Lead e Product Manager atuam em parceria contínua.

* **Product Manager:** Define o **problema** e o valor esperado para o negócio.
* **Tech Lead:** Traz viabilidade, riscos arquiteturais, estimativas de esforço e alternativas operacionais para viabilizar a entrega.

---

### 22. O Product Manager pede algo tecnicamente muito ruim. O que você faz?

> Substituo o "não dá" por uma **discussão transparente de trade-offs**.

1. Compreender a real dor ou objetivo de negócio por trás do pedido.
2. Apresentar os riscos operacionais e propor alternativas viáveis.
3. *Exemplo:* "A abordagem X traz um risco Y de instabilidade. Conseguimos atender 80% do resultado esperado entregando a opção Z com a metade da complexidade."

---

### 23. Como você prioriza uma melhoria técnica?

> **Fórmula de Priorização:** $\text{Prioridade} = \text{Impacto} \times \text{Risco} \times \text{Urgência} / \text{Custo}$

Melhorias técnicas que evitem **indisponibilidade do sistema** ou **vulnerabilidades de segurança** possuem prioridade máxima frente a otimizações estéticas de código.

---

## 🎭 Módulo 6: Perfil Pessoal & Pitch Profissional

### 24. Como você desenvolve pessoas?

* Mapeamento de senioridade e objetivos individuais de carreira.
* Combinação de reuniões 1:1, *code reviews* orientativos, *pair programming* e delegação gradual de responsabilidades.
* **Indicador de Sucesso:** O time se tornar autossuficiente em decisões que antes dependiam exclusivamente do Tech Lead.

---

### 25. Qual é seu maior ponto forte como Tech Lead?

> **Trânsito Multidisciplinar:** Capacidade de alternar com facilidade entre discussões de código em baixo nível, arquitetura de sistemas, infraestrutura/cloud e alinhamento estratégico de negócios.

Atuo cobrindo todo o fluxo da solução (Backend, Bancos de Dados, DevOps e Arquitetura), focando sempre em multiplicar conhecimento com a equipe em vez de centralizar a execução.

---

### 26. Qual é seu ponto fraco?

> **Ponto de Atenção:** A tendência a me aprofundar em detalhes técnicos que poderiam ser totalmente delegados.

**Ação de Melhoria:** Venho exercitando ativamente a delegação consciente e o fortalecimento da autonomia do time, entendendo que a prioridade do líder técnico é **escalar a capacidade do time** e não centralizar tarefas complexas.

---

### 27. Você ainda programa como Tech Lead?

> **Sim**, porém a atuação no código varia com o momento do time.

Manter contato direto com a base de código é essencial para manter a visão prática dos desafios do time. No entanto, o papel principal não é medido por volume de *pull requests*, mas sim por remover impedimentos, desenhar arquiteturas e destravar o time.

---

### 28. Você prefere ser especialista ou generalista?

> Perfil **T-Shaped**: Profundidade técnica em Backend e Arquitetura de Sistemas, com forte amplitude em Cloud, DevOps, Banco de Dados e Frontend.

---

### 29. Como você lida com pressão?

1. **Desacoplamento:** Separar pressão externa de urgência técnica real.
2. **Priorização Clara:** Mapear o impacto de cada item e estruturar um plano de ação objetivo.
3. **Comunicação Transparente:** Manter *stakeholders* constantemente atualizados para reduzir a ansiedade do negócio e garantir o foco da engenharia.

---

### 30. Por que deveríamos contratar você como Tech Lead?

> "Porque consigo combinar **profundidade técnica**, **visão sistêmica** e **gestão orientada a pessoas**."

Minha bagagem prática me permite transitar da implementação de código à tomada de decisão arquitetural e de infraestrutura. Mais do que deter conhecimento, minha meta como Tech Lead é construir um ambiente técnico seguro, onde o time evolua com autonomia e entregue valor consistente ao negócio.


## Contatos

[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/cleibp)](https://github.com/cleibp)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/cleitonpaiva/)](https://www.linkedin.com/in/cleitonpaiva/)
[![Whatsapp Badge](https://img.shields.io/badge/-Whatsapp-4CA143?style=flat-square&labelColor=4CA143&logo=whatsapp&logoColor=white&link=https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)](https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:cleibp@gmail.com)](mailto:cleibp@gmail.com)

[Pague-me um ☕](https://www.buymeacoffee.com/cleibp)

Feito com muito ❤️☕👨🏻‍💻 por Cleiton Paiva
