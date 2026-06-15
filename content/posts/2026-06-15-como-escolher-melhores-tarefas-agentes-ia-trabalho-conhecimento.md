+++
title = "Por que agentes de IA funcionam tão bem para código e o que podemos aprender com isso"
date = 2026-06-15T08:00:00-03:00
draft = false
summary = "O que o sucesso dos agentes de IA em tarefas de código ensina sobre como aplicar agentes ao trabalho de conhecimento."
tags = ["IA", "agentes de IA", "trabalho de conhecimento", "enterprise AI", "automação"]
topics = ["AI"]
+++

*English version: [Why AI Agents Work So Well for Code and What We Can Learn From It](/gabriel-dornella-blog/posts/2026-06-15-how-to-choose-best-tasks-ai-agents-knowledge-work/).* 

Por que agentes de IA funcionam tão bem para tarefas de código mas ainda tem desafios para outras áreas.

No artigo anterior, escrevi sobre o ganho de produtividade que os desenvolvedores estão tendo ao adotar IA para codificação (especialmente agentes de IA) e sobre como podemos aplicar essa mesma lógica a outros tipos de tarefa, desde que criemos o ambiente correto tanto para os humanos quanto para os agentes.

Nas últimas semanas, dois dos criadores mais inovadores desse novo momento, Peter Steinberger, criador do OpenClaw, e Boris Cherny, criador do Claude Code, elevaram esse conceito e disseram que já não escrevem prompts diretamente para seus agentes. Agora, eles escrevem loops que geram prompts e interagem com os agentes. Esses loops são processos que dão contexto, recebem respostas, verificam resultados e seguem avançando continuamente.

Isso representa um ganho gigantesco de produtividade e escala, porque eles deixam de ser o gargalo do processo de escrever cada prompt. A implicação dessa nova arquitetura é que os agentes passam a operar com mais autonomia dentro do ambiente correto para executar suas tarefas: sistemas compostos por loops, ferramentas, contexto, validação e agentes trabalhando em ciclos cada vez mais longos e autônomos.

No desenvolvimento de software, isso já está gerando ganhos expressivos. A pergunta que me interessa é: como aplicar essa mesma lógica ao trabalho do conhecimento em outras áreas da empresa?

A resposta curta é que dá para fazer, mas não basta copiar o modelo usado por engenheiros de software. O ambiente é diferente, os riscos são diferentes e a forma de escolher os casos de uso precisa ser mais cuidadosa.

## Por que agentes de IA funcionam tão bem para software

Antes de pensar em marketing, finanças, RH ou operações, vale entender porque agentes funcionam tão bem para desenvolvimento de software.

O primeiro ponto é que código é uma linguagem muito natural para LLMs. É texto, tem estrutura, tem padrões, tem dependências explícitas e pode ser lido, escrito, comparado, refatorado e analisado pelo próprio agente. O artefato com que o humano trabalha é o mesmo artefato que o agente consegue manipular.

O segundo ponto é que o ambiente de software oferece feedback rápido e objetivo. O teste passa ou falha. A aplicação compila ou quebra. Um endpoint retorna o resultado esperado ou não. Um erro aparece no log. Um componente visual pode ser comparado com uma referência.

Isso cria ciclos de aprendizado muito poderosos. O agente não depende apenas da opinião de alguém para saber se está avançando. Ele consegue executar uma ação, observar o resultado, corrigir o caminho e tentar novamente.

Também existe uma noção relativamente clara de conclusão. Em muitas tarefas de programação, é possível verificar se o trabalho foi feito: o bug foi reproduzido e corrigido, os testes passaram, o endpoint respondeu corretamente, a performance melhorou ou a interface ficou igual ao esperado.

Além disso, os agentes de software têm acesso a ferramentas poderosas. Eles podem ler arquivos, editar código, executar comandos, pesquisar no repositório, chamar APIs, abrir pull requests e rodar testes. O contexto inteiro do trabalho costuma estar disponível dentro do próprio ambiente: código-fonte, documentação, testes, logs, configurações, issues e histórico do Git.

E talvez o mais importante: a experimentação é relativamente segura.

Git, branches, diffs, pull requests, code review e rollback criam uma camada de controle. O agente pode propor mudanças, mas elas ficam visíveis. Humanos podem revisar. Testes podem validar. Se algo der errado, é possível voltar atrás.

Em outras palavras, agentes para código funcionam bem porque operam em um ambiente com quatro características muito fortes:

**contexto amplo + acesso amplo a ferramentas + ações reversíveis + verificação objetiva.**

![Por que a engenharia de software é amigável para agentes](/gabriel-dornella-blog/images/posts/ai-agents-knowledge-work/engenharia-software-amigavel-agentes-pt.jpg)

Esse conjunto é o que torna o desenvolvimento de software um dos melhores ambientes para agentes de IA hoje.

## O problema de aplicar a mesma lógica ao trabalho do conhecimento

Quando saímos do software e olhamos para outras áreas da empresa, essas condições começam a desaparecer.

Pense em marketing, finanças, RH, operações ou vendas. Essas áreas também executam trabalho intelectual, tomam decisões, produzem documentos, analisam informações e coordenam processos. Em tese, parecem ótimas candidatas para agentes de IA.

Mas o ambiente onde esse trabalho acontece é muito menos estruturado.

A linguagem do negócio nem sempre é nativa para os modelos. Parte da informação está em textos, mas muita coisa vive em apresentações, planilhas, fluxos, dashboards, conversas, reuniões, imagens, diagramas e conhecimento tácito das pessoas. O agente pode ler alguns desses artefatos, mas raramente entende o contexto completo apenas olhando para os arquivos disponíveis.

O feedback também costuma ser mais lento e subjetivo. Como saber se um briefing de campanha está realmente bom antes de ele ser usado pelos times criativos? Como saber se uma análise financeira levou em conta todas as nuances de uma negociação? Como saber se um dashboard responde às perguntas certas antes de ele ser usado em uma reunião executiva?

Em muitos casos, “concluído” não é tão fácil de verificar. Um documento pode estar completo, mas incompleto do ponto de vista do negócio. Uma recomendação pode estar bem escrita, mas errada em relação ao contexto. Uma decisão pode parecer razoável hoje e só revelar seu impacto semanas depois.

Também existe o problema das ferramentas. O trabalho do conhecimento acontece em sistemas espalhados: CRM, ERP, ferramentas de workflow, e-mail, mensagens, documentos, planilhas, apresentações e sistemas internos. Mesmo quando essas ferramentas têm APIs, conectá-las de forma segura e útil exige um modelo de dados consistente, permissões adequadas e uma visão clara do processo.

E há uma questão de acesso que não pode ser tratada como detalhe. Um agente de RH pode ter acesso a dados sensíveis de funcionários. Um agente financeiro pode acessar informações de caixa, margem, crédito ou salário. Um agente comercial pode ver negociações estratégicas. Dar autonomia sem desenhar bem os limites pode criar riscos importantes.

Por fim, a maioria dos workflows empresariais não tem o equivalente a Git. Uma campanha aprovada não vive em uma branch. Uma negociação comercial não tem rollback simples. Um briefing ruim pode gerar trabalho desperdiçado em cadeia. Uma decisão financeira errada pode afetar caixa, margem ou relacionamento com clientes.

Isso não significa que agentes de IA não funcionem para trabalho do conhecimento. Significa que precisamos escolher melhor onde usá-los.

## Agentes executam tarefas, não trabalhos inteiros

Um erro comum é imaginar que um agente de IA deve assumir um trabalho inteiro. “Vamos criar um agente de marketing.” “Vamos criar um agente financeiro.” “Vamos criar um agente de RH.”

Essa forma de pensar é ampla demais para o estágio atual da tecnologia. Agentes são muito mais úteis quando pensamos em tarefas específicas dentro de um trabalho maior.

O trabalho de marketing, por exemplo, pode ser descrito como criar e capturar demanda qualificada. Mas isso se desdobra em vários trabalhos menores: criar campanhas, fortalecer posicionamento, acelerar ciclos de vendas, segmentar clientes, produzir ativos criativos, analisar performance e assim por diante.

Cada um desses trabalhos menores contém tarefas: escrever um briefing, pesquisar referências, definir mensagens, montar uma segmentação, revisar peças, consolidar resultados, preparar uma apresentação.

A mesma lógica vale para finanças. O trabalho de finanças pode ser garantir que os recursos sejam alocados, protegidos e otimizados para sustentar crescimento, rentabilidade e previsibilidade. Mas esse trabalho inclui tarefas muito diferentes: analisar fluxo de caixa, revisar exceções comerciais, aprovar condições especiais, consolidar dados, acompanhar indicadores, preparar cenários e apoiar decisões.

A pergunta certa não é “qual área podemos automatizar com agentes?”. A pergunta certa é: “quais tarefas dentro dessa área têm as condições necessárias para um agente atuar com autonomia?”.

## Um método simples para escolher bons casos de uso

Para escolher onde aplicar agentes de IA no trabalho do conhecimento, eu começaria pelo *job to be done* da área e depois quebraria esse trabalho em tarefas.

A partir daí, avaliaria cada tarefa com sete perguntas:

1. A linguagem dessa tarefa é natural para o agente?
2. É possível dar feedback imediato sobre a qualidade do que está sendo produzido?
3. É possível verificar se a tarefa foi concluída?
4. As ferramentas necessárias estão disponíveis para o agente?
5. Todo o contexto necessário está disponível?
6. O agente pode ter acesso às informações necessárias ou há controles especiais?
7. É possível desfazer, revisar ou corrigir o que o agente fez?

![Metodologia para definição de agentes de IA](/gabriel-dornella-blog/images/posts/ai-agents-knowledge-work/metodologia-definicao-agentes-ia-pt.jpg)

Essas perguntas ajudam a separar tarefas onde o agente pode ter mais autonomia de tarefas onde ele deve atuar apenas como apoio para um humano.

O objetivo não é encontrar tarefas sem nenhum risco. Isso provavelmente não existe. O objetivo é encontrar tarefas em que o risco é compreensível, o contexto é suficiente, o resultado é verificável e o escopo pode ser aumentado com segurança.

## Dois exemplos: briefing de campanha e aprovação financeira

Imagine duas tarefas diferentes.

A primeira é criar um briefing de campanha de marketing. A missão do agente seria produzir um documento completo para orientar times criativos, comunicação, mídia e outros envolvidos na execução da campanha.

A segunda é aprovar uma condição especial de pagamento para um cliente. A missão do agente seria avaliar uma exceção solicitada pelo time comercial, considerando o impacto financeiro, o risco, o fluxo de caixa e a probabilidade de fechamento do negócio.

As duas tarefas são importantes. As duas envolvem texto, análise e decisão. Mas elas não têm o mesmo perfil para autonomia.

No caso do briefing de campanha, a linguagem é principalmente texto. O agente pode trabalhar com templates, histórico de campanhas, documentação de marca, posicionamento, características de produtos e informações sobre o público. É possível comparar o briefing produzido com um modelo esperado. Outro LLM ou um processo de revisão pode avaliar se o documento está completo, claro e alinhado ao objetivo.

A conclusão também é verificável: o briefing existe, cobre os campos necessários e pode ser revisado antes de gerar trabalho downstream. As ferramentas necessárias são relativamente simples: leitura, escrita, busca, recuperação de contexto e edição de documentos. Se algo não estiver bom, é possível revisar antes de publicar ou enviar para execução.

Esse é um bom candidato para mais autonomia.

Já a aprovação de uma condição especial de pagamento é diferente. A linguagem pode até ser textual, mas o contexto necessário é mais complexo. Parte da informação está no CRM, parte está em dados financeiros, parte está em trocas de e-mail ou mensagens, e parte pode estar na cabeça das pessoas que participaram da negociação.

O feedback não é imediato. Uma decisão pode parecer correta no momento e só mostrar seus efeitos semanas ou meses depois. O impacto no caixa, na margem, no comportamento do cliente e na previsibilidade financeira pode demorar a aparecer.

A tarefa pode ser concluída formalmente: aprovar ou rejeitar a exceção, mas isso não significa que a decisão foi boa. E, dependendo do caso, desfazer a decisão pode ser difícil ou politicamente caro.

Nesse cenário, o agente ainda pode ser muito útil. Ele pode consolidar informações, destacar riscos, comparar políticas, sugerir perguntas e preparar uma recomendação. Mas a decisão final provavelmente deve continuar com um humano no loop.

A diferença entre os dois casos mostra a principal decisão: o ganho de produtividade não vem apenas de colocar agentes em qualquer processo. Ele vem de escolher processos onde os agentes podem operar com contexto, ferramentas, feedback e controle suficientes para terem ou não autonomia.

## Comece pequeno, teste e aumente o escopo

Agentes de IA terão um impacto enorme no trabalho do conhecimento. Mas a forma correta de aplicá-los fora do desenvolvimento de software exige mais desenho operacional do que simplesmente mais prompts.

O caminho mais seguro é começar por tarefas específicas, com critérios claros de sucesso, contexto disponível, revisão possível e baixo custo de erro. Depois, testar o agente em um escopo limitado, observar onde ele falha, melhorar o contexto, ajustar ferramentas, criar mecanismos de feedback e só então aumentar sua autonomia.

Essa lógica é parecida com o que funcionou no desenvolvimento de software, mas precisa ser adaptada ao ambiente de cada área.

No software, os agentes encontraram um terreno fértil porque o trabalho já tinha muitos dos elementos necessários: contexto documentado, ferramentas integradas, feedback rápido, versionamento e validação objetiva.

No trabalho do conhecimento, esses elementos precisam ser construídos.

E talvez essa seja a principal lição: antes de perguntar como criar agentes para uma área da empresa, precisamos perguntar se aquela área oferece as condições para que agentes trabalhem bem.

Quando essas condições existem, os ganhos podem ser expressivos. Quando não existem, o papel do agente deve ser mais assistivo, com humanos mantendo julgamento, responsabilidade e controle.

A oportunidade é grande. Mas ela não está em automatizar trabalhos inteiros. Está em redesenhar tarefas, criar ambientes mais agent-friendly e dar autonomia aos agentes onde o contexto, o feedback e o risco permitem.
