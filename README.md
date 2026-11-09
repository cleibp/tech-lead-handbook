# Tech Lead Handbook
> Guia prático de Engenharia de Software, Arquitetura e Liderança Técnica.

> Conhecimento compartilhado para profissionais que desejam evoluir de desenvolvedores para referências técnicas e líderes de engenharia.

> Português (Brasil) · Markdown · GitHub

# 🧠 Perguntas

## 1. O que significa ser um Tech Lead para você?

> Tech Lead não é simplesmente a pessoa que mais programa ou que possui mais conhecimento técnico no time.

> É alguém responsável por dar direção técnica, ajudar o time a tomar boas decisões e garantir que as soluções estejam alinhadas às necessidades do negócio.

> O Tech Lead precisa equilibrar três dimensões: tecnologia, pessoas e negócio.

> Eu vejo meu papel como alguém que cria contexto, reduz riscos técnicos, estabelece padrões e ajuda os desenvolvedores a evoluírem, sem centralizar todas as decisões em mim.

## 2. Qual a diferença entre um Tech Lead e um desenvolvedor sênior?
> Um desenvolvedor sênior normalmente possui grande capacidade técnica e consegue resolver problemas complexos de forma independente.

> O Tech Lead, além disso, precisa pensar no sistema como um todo e no impacto das decisões no time e no negócio.

> Por exemplo, um sênior pode desenvolver muito bem uma funcionalidade. Já o Tech Lead precisa questionar:
> - Essa arquitetura escala?
> - Essa decisão aumenta nossa dívida técnica?
> - Como isso impactará outros serviços?
> - Como vamos monitorar?
> - O time conseguirá manter essa solução?
> - Qual é o custo operacional?
> Portanto, o Tech Lead precisa ampliar a visão além do código.

## 3. Como você toma uma decisão arquitetural?
Resposta:
Eu procuro evitar decisões baseadas simplesmente em preferência pessoal ou em uma tecnologia que esteja na moda.

Primeiro procuro entender o problema, os requisitos funcionais e não funcionais, volume, disponibilidade, segurança, custo e capacidade do time.

Depois avalio alternativas, seus trade-offs e riscos.

Quando a decisão é relevante, gosto de documentá-la através de um ADR — Architecture Decision Record, deixando claro o problema, as alternativas consideradas, a decisão tomada e suas consequências.

## 4. Você prefere monólito ou microsserviços?
Resposta forte:
Não existe uma resposta universal.

Eu não começaria um projeto utilizando microsserviços apenas porque a arquitetura é considerada moderna.

Microsserviços aumentam a complexidade operacional: observabilidade, comunicação distribuída, deploy, tracing, consistência de dados, segurança e troubleshooting.

Se um monólito modular atende aos requisitos, pode ser uma excelente solução.

Eu consideraria microsserviços quando existirem necessidades reais relacionadas a escala independente, autonomia de domínio, times independentes, requisitos diferentes de disponibilidade ou evolução desacoplada.

Para mim, arquitetura é consequência do problema, não o contrário.

## 5. Como você lida com dívida técnica?
Resposta:
Eu não considero toda dívida técnica necessariamente ruim. Algumas dívidas são decisões conscientes para acelerar uma entrega.

O problema acontece quando a dívida deixa de ser controlada.

Eu procuro classificar a dívida pelo impacto: risco operacional, segurança, performance, produtividade do time e dificuldade de evolução.

Depois tento transformar a dívida técnica em itens visíveis no backlog, priorizando aquelas que representam maior risco para o negócio.

Também gosto de utilizar métricas e incidentes reais para demonstrar o custo daquela dívida.

## 6. Como você resolve um conflito técnico entre dois desenvolvedores?
Resposta:
Primeiro eu evitaria transformar a discussão em uma disputa de opinião.

Tentaria entender os argumentos de cada lado e trazer a discussão para critérios objetivos.

Por exemplo:
- performance;
- manutenção;
- segurança;
- custo;
- complexidade;
- experiência do time;
- impacto arquitetural.
Se necessário, podemos construir um pequeno POC para validar uma hipótese.

Depois da decisão, é importante que o time esteja alinhado e que a decisão seja documentada.

O objetivo não é descobrir quem estava certo, mas encontrar a melhor solução para o produto.

## 7. Como você lida com um desenvolvedor que discorda de você?
Resposta:
Eu considero saudável que um desenvolvedor discorde de mim.

Um Tech Lead que nunca é questionado provavelmente está criando um ambiente onde as pessoas não se sentem confortáveis para contribuir.

Eu procuro ouvir o argumento, analisar evidências e, se o argumento for melhor, mudar minha decisão.

Liderança técnica não significa estar sempre certo. Significa criar condições para que o time tome decisões melhores.

## 8. Como você faz code review?
Resposta:
Eu procuro evitar que o code review seja uma avaliação pessoal do desenvolvedor.

Meu foco é verificar:
- corretude;
- segurança;
- legibilidade;
- manutenibilidade;
- testes;
- performance quando relevante;
- padrões arquiteturais;
- impacto em outros componentes.
Também tento automatizar o que for possível através de linters, testes, SonarQube, pipelines e ferramentas de análise estática.

Code review deve ser uma ferramenta de qualidade e também de compartilhamento de conhecimento.

## 9. O que você faz quando um desenvolvedor entrega uma solução tecnicamente ruim?
Resposta:
Primeiro procuro entender por que aquela solução foi construída daquela maneira.

Pode existir uma restrição que eu desconheça.

Depois conversaria com o desenvolvedor individualmente, explicaria os riscos e construiríamos uma alternativa.

Se for algo crítico, posso solicitar a alteração antes do merge.

Porém, também verificaria se o problema é individual ou se existe uma deficiência de processo, documentação ou conhecimento no time.

## 10. Como você garante qualidade técnica sem virar um gargalo?
Resposta:
Esse é um ponto muito importante.

O Tech Lead não pode ser o único responsável por revisar tudo ou tomar todas as decisões.

Eu procuro criar padrões, documentação, guidelines, automações e distribuir conhecimento dentro do time.

Por exemplo, em vez de todas as decisões passarem por mim, podemos estabelecer padrões arquiteturais e permitir que o próprio time tome decisões dentro desses limites.

Meu objetivo é aumentar a autonomia do time.

## 11. Como você conduziria a arquitetura de uma nova API?
Resposta:
Eu começaria entendendo o domínio e os requisitos.

Depois avaliaria:

API
- REST ou outro protocolo;
- contratos;
- versionamento;
- autenticação/autorização;
- idempotência.
Aplicação
- separação de responsabilidades;
- domínio;
- persistência;
- integração.
Infraestrutura
- containers;
- Kubernetes ou serverless;
- banco;
- cache;
- filas;
- observabilidade.
Operação
- logs;
- métricas;
- tracing;
- alertas;
- CI/CD.
E principalmente: quais são os requisitos de disponibilidade, escala, segurança e custo.

## 12. Como você projetaria uma API que precisa suportar milhões de requisições?
Resposta:
Primeiro eu evitaria assumir que simplesmente aumentar servidores resolverá o problema.

Eu analisaria onde está o gargalo.

Poderíamos utilizar:
- load balancing;
- escalabilidade horizontal;
- cache;
- CDN;
- bancos com réplicas;
- particionamento;
- processamento assíncrono;
- filas;
- otimização de queries;
- connection pooling.
Também considero fundamental medir o sistema com testes de carga e observar métricas como latência, throughput, erro e saturação.

Escalabilidade precisa ser baseada em evidências.

## 13. Quando você usaria Kafka?
Resposta:
Kafka é interessante quando precisamos trabalhar com event streaming, alto volume de eventos, desacoplamento entre produtores e consumidores ou processamento assíncrono.

Porém, não utilizaria Kafka simplesmente para substituir uma chamada HTTP.

Se tenho uma operação simples e síncrona, REST pode ser suficiente.

Se tenho vários consumidores interessados no mesmo evento e preciso de processamento desacoplado e resiliente, Kafka passa a fazer muito mais sentido.

## 14. Kafka ou SQS?
Resposta:
Depende do problema.

O SQS é excelente para filas gerenciadas e processamento assíncrono, principalmente dentro do ecossistema AWS.

Kafka é mais adequado quando tenho uma necessidade de streaming de eventos, retenção, replay, múltiplos consumidores e alto throughput.

Eu avaliaria também custo operacional, necessidade de retenção, modelo de consumo, ordering e experiência do time.

## 15. Como você desenharia uma aplicação resiliente?
Resposta:
Eu trabalharia com vários mecanismos:
- timeout;
- retry com backoff;
- circuit breaker;
- idempotência;
- filas;
- dead-letter queue;
- health checks;
- observabilidade;
- graceful degradation.
Mas é importante tomar cuidado com retry. Um retry mal implementado pode aumentar ainda mais a sobrecarga de um sistema que já está com problema.

## 16. Como você trabalha com observabilidade?
Resposta:
Eu considero três pilares principais:

Logs, métricas e traces.

Logs precisam ser estruturados e conter informações úteis para investigação.

Métricas permitem acompanhar comportamento do sistema, como latência, throughput, taxa de erro e utilização de recursos.

Tracing é especialmente importante em arquiteturas distribuídas para acompanhar uma requisição entre diferentes serviços.

Além disso, alertas precisam estar relacionados a sintomas relevantes para o negócio e não simplesmente a qualquer métrica que ultrapasse um limite.

## 17. Um sistema está apresentando lentidão. O que você faria?
Resposta:
Eu não começaria alterando código imediatamente.

Primeiro tentaria identificar onde está o gargalo.

Analisaria:
1. métricas;
2. logs;
3. traces;
4. banco de dados;
5. infraestrutura;
6. dependências externas;
7. filas;
8. mudanças recentes.
A partir das evidências, formularia uma hipótese e validaria.

Depois aplicaria a correção e acompanharia as métricas para confirmar se o problema realmente foi resolvido.

## 18. Como você lida com incidentes em produção?
Resposta:
Primeiro vem a estabilização do sistema.

Durante um incidente, o objetivo inicial não é descobrir o culpado, mas reduzir o impacto para os usuários.

Dependendo do caso podemos fazer rollback, desabilitar uma feature, reduzir carga ou aplicar alguma mitigação.

Depois da estabilização, fazemos a investigação da causa raiz e um post-mortem, buscando entender não apenas o erro técnico, mas também por que nossos mecanismos de prevenção não detectaram ou evitaram o problema.

## 19. O que é mais importante: entregar rápido ou entregar com qualidade?
Resposta:
Eu evitaria tratar como uma escolha binária.

O objetivo é entregar valor rapidamente com um nível de qualidade compatível com o risco.

Uma funcionalidade experimental pode aceitar mais riscos do que uma operação financeira crítica.

O papel do Tech Lead é ajudar o time e o produto a entenderem esses trade-offs.

Velocidade sem qualidade gera dívida e incidentes. Qualidade excessiva sem entrega também pode gerar desperdício.

## 20. Como você mede o sucesso de um time de engenharia?
Resposta:
Eu não avaliaria apenas pela quantidade de tarefas entregues.

Consideraria indicadores como:
- lead time;
- frequência de deploy;
- taxa de falha de mudanças;
- tempo de recuperação;
- incidentes;
- qualidade;
- satisfação do time;
- previsibilidade;
- impacto das entregas no negócio.
Métricas devem ajudar o time a melhorar, não servir simplesmente como mecanismo de cobrança.

## 21. Como você trabalha com produto?
Resposta:
Eu acredito que Tech Lead e Product Manager precisam trabalhar muito próximos.

O Tech Lead contribui trazendo conhecimento sobre viabilidade, riscos, arquitetura, esforço e alternativas técnicas.

Porém, não devemos transformar toda decisão de produto em uma decisão técnica.

O produto define o problema e o valor esperado; engenharia ajuda a encontrar a melhor forma de construir a solução dentro das restrições existentes.

## 22. O Product Manager pede algo tecnicamente muito ruim. O que você faz?
Resposta:
Eu não responderia simplesmente "não dá".

Primeiro tentaria entender o objetivo por trás da solicitação.

Depois explicaria os riscos técnicos e apresentaria alternativas.

Por exemplo:

"Podemos fazer dessa forma, mas teremos determinado risco. Outra alternativa é essa, que atende 80% da necessidade com menor complexidade."

Dessa maneira, a conversa deixa de ser "tecnologia contra produto" e passa a ser uma discussão sobre trade-offs.

## 23. Como você prioriza uma melhoria técnica?
Resposta:

Eu avaliaria:
Impacto × Risco × Custo × Urgência.

Uma dívida técnica que pode causar indisponibilidade ou incidente de segurança possui prioridade muito maior do que uma melhoria puramente estética no código.

Também tento relacionar a melhoria técnica aos objetivos do produto.

## 24. Como você desenvolve pessoas?
Resposta:
Eu procuro entender o nível e os objetivos de cada profissional.

Algumas pessoas precisam de mais orientação técnica; outras precisam de mais autonomia.

Utilizo code review, pairing, feedbacks, discussões arquiteturais e compartilhamento de conhecimento.

Também procuro delegar responsabilidades progressivamente.

Um dos maiores sinais de sucesso de um Tech Lead é quando o time consegue resolver problemas que antes dependiam exclusivamente dele.

## 25. Qual é seu maior ponto forte como Tech Lead?
Resposta-modelo para seu perfil:
Meu principal ponto forte é conseguir transitar entre diferentes níveis de discussão.

Consigo entrar em detalhes técnicos quando necessário, mas também consigo discutir arquitetura, infraestrutura, riscos e impacto para o negócio.

Tenho experiência trabalhando com backend, frontend, banco de dados, cloud e infraestrutura, então consigo enxergar bastante do fluxo completo de uma solução.

Ao mesmo tempo, procuro não centralizar o conhecimento e estimular o time a crescer junto.

## 26. Qual é seu ponto fraco?
Essa é uma pergunta perigosa.

Evite:
"Sou perfeccionista."

Prefira algo real + ação de melhoria.

Resposta:
Um ponto que venho trabalhando é evitar entrar profundamente em problemas técnicos que poderiam ser delegados.

Por ter bastante interesse técnico, existe o risco de eu querer participar de determinadas decisões ou implementações que poderiam ser conduzidas por outros membros do time.

Tenho trabalhado justamente na delegação e na criação de autonomia, entendendo que o papel do Tech Lead é multiplicar conhecimento e não centralizá-lo.

## 27. Você ainda programa como Tech Lead?
Resposta:
Sim, mas meu nível de envolvimento depende do contexto.

Eu acredito que um Tech Lead precisa manter proximidade com o código para não perder contato com a realidade técnica.

Porém, minha responsabilidade não pode ser medida pela quantidade de linhas de código produzidas.

Em alguns momentos posso atuar diretamente em uma implementação crítica ou POC. Em outros, meu trabalho mais importante será definir uma arquitetura, remover um impedimento ou ajudar o time a tomar uma decisão.

## 28. Você prefere ser especialista ou generalista?
Resposta:
Eu acredito que um Tech Lead precisa ter profundidade em algumas áreas e visão suficientemente ampla das demais.

Não é necessário ser especialista em absolutamente tudo.

Meu perfil tende a ser mais T-shaped: tenho profundidade em determinadas áreas de desenvolvimento e arquitetura, mas também tenho visão de cloud, DevOps, banco, frontend e infraestrutura.

Isso me ajuda a enxergar as consequências das decisões de forma mais ampla.

29. Como você lida com pressão?
Resposta:
Eu procuro separar pressão de urgência.

Em situações críticas, primeiro estabeleço prioridades, impacto e próximos passos.

Evito tomar decisões importantes simplesmente porque existe pressão.

Comunicação também é fundamental: manter stakeholders informados reduz ansiedade e evita que várias pessoas trabalhem em direções diferentes.

## 30. Por que deveríamos contratar você como Tech Lead?
Resposta forte para entrevista:
Porque acredito que consigo combinar três aspectos importantes para essa posição: profundidade técnica, visão sistêmica e capacidade de trabalhar com pessoas.

Minha experiência me permite atuar desde a implementação até decisões de arquitetura, cloud, integração, banco de dados e infraestrutura.

Mas acredito que o principal papel de um Tech Lead não é ser a pessoa que sabe tudo.

É criar um ambiente onde o time consiga tomar boas decisões técnicas, evoluir profissionalmente e entregar valor para o negócio com qualidade.

É esse tipo de liderança técnica que eu procuro exercer.


## Contatos

[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/cleibp)](https://github.com/cleibp)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/cleitonpaiva/)](https://www.linkedin.com/in/cleitonpaiva/)
[![Whatsapp Badge](https://img.shields.io/badge/-Whatsapp-4CA143?style=flat-square&labelColor=4CA143&logo=whatsapp&logoColor=white&link=https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)](https://api.whatsapp.com/send?phone=5516988368457&text=Ola!)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:cleibp@gmail.com)](mailto:cleibp@gmail.com)

[Pague-me um ☕](https://www.buymeacoffee.com/cleibp)

Feito com muito ❤️☕👨🏻‍💻 por Cleiton Paiva
