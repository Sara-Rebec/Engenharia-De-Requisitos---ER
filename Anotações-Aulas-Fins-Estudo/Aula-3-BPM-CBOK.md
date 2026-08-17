# Gerenciamento de Processos de Negócio (BPM) — Guia BPM CBOK
**Disciplina:** Engenharia de Requisitos | **Aula 03** | Profa. Kadidja Valéria

---

## 🪼⋆.ೃ࿔*:･ 1. Contexto e ideia central da aula

A aula introduz o **Guia BPM CBOK®** (*Business Process Management Common Body of Knowledge*), publicado pela ABPMP (Association of Business Process Management Professionals). Esse guia é o documento de referência que organiza, em nove áreas de conhecimento, tudo o que um profissional de processos precisa dominar — e é também a base para a certificação **CBPP™** (Certified Business Process Professional).

A frase de abertura, atribuída a Bill Gates, resume por que estudar processos *antes* de automatizar é tão importante: automatizar um processo eficiente amplia a eficiência, mas automatizar um processo ruim só amplia o problema em maior velocidade. Essa é a justificativa central de todo o conteúdo: **não adianta implantar tecnologia (ERP, sistema, BPMS) sobre um processo mal desenhado** — primeiro entende-se e organiza-se o processo, depois se pensa em ferramenta.

> 💡 **Por que isso importa na Engenharia de Requisitos:** antes de levantar requisitos de um sistema, o analista precisa entender o processo de negócio que o sistema vai apoiar. Requisito mal levantado costuma ser sintoma de processo mal mapeado.

---

## ──★˙🍓̟!! 2. Conceitos fundamentais

### 2.1 Negócio
Conjunto de pessoas que interagem para executar atividades que **entregam valor a clientes** e geram retorno às partes interessadas. O termo é amplo: vale para empresas com ou sem fins lucrativos, inclusive órgãos governamentais.

### 2.2 Processo (definição genérica)
Várias definições clássicas convergem para a mesma ideia: um processo é um **conjunto de atividades inter-relacionadas que transforma entradas (insumos) em saídas (produtos/serviços)**, seguindo uma sequência lógica, para gerar valor a um grupo específico de clientes (Hammer & Champy; ISO; Pfleeger).

Esquema mental simples:

```
ENTRADA  →  [ Processo: atividades, tarefas, responsáveis,
              ferramentas, recursos, regras, documentos,
              metas e indicadores ]  →  SAÍDA
```

### 2.3 Processo de Negócio (definição específica de BPM)
No contexto de BPM, processo de negócio é um trabalho **"ponta a ponta" (end-to-end)** que entrega valor ao cliente. Duas características o distinguem de um processo genérico:

1. **Inter-funcionalidade** — a maioria dos processos importantes (principalmente os primários) **atravessa vários departamentos/áreas funcionais**, em vez de ficar contido em um só setor.
2. **Tem clientes** (internos ou externos) — o resultado do processo sempre é entregue a alguém. Por isso a organização pode ser vista como uma coleção de fluxos de valor voltados a satisfazer grupos de clientes.

**Aprofundando:** essa é a diferença conceitual mais cobrada em prova — um departamento (ex.: Contabilidade) executa **funções contínuas**, mas não "possui" sozinho o processo ponta a ponta; ele apenas **suporta** processos de negócio que atravessam vários departamentos (veja seção 4).

### 2.4 Por que processos são importantes
- Definem a forma básica de organizar pessoas e recursos.
- São fonte de vantagem competitiva (Keen, 1997): impactam estratégia, produtos e estrutura.
- Caso citado na aula: indústrias japonesas investiam ~70% do orçamento de P&D em **inovação de processo**, enquanto empresas americanas investiam a mesma proporção em **desenvolvimento de produto** — isso ajuda a explicar a eficiência operacional japonesa em áreas como logística e manufatura.

---

## ˖ ࣪ ꉂ🗯˙🫐⃟.꩜‹— 3. Tipos de Processo de Negócio

Três categorias básicas — **decore a lógica, não só o nome**:

| Categoria | O que caracteriza | Exemplos |
|---|---|---|
| **Processos Primários (essenciais)** | Atuação-fim da empresa; resultam no produto/serviço entregue ao **cliente externo**; são suportados por outros processos | Vendas, desenvolvimento de produto, distribuição, atendimento de pedidos |
| **Processos de Suporte (secundários/auxiliares)** | Centralizados na organização; viabilizam o funcionamento coordenado dos subsistemas; **não geram valor direto ao cliente externo**, mas sustentam quem gera | Compras, recrutamento e seleção, orçamento empresarial, treinamento |
| **Processos de Gerenciamento (gerenciais)** | Focados nos gestores e em suas relações; envolvem planejamento, medição e ajuste de desempenho | Planejamento estratégico, fixação de metas, alocação de recursos, avaliação de resultado |

**Aprofundando (raciocínio útil para identificar a categoria de um processo em prova/exercício):** pergunte "quem recebe o resultado direto deste processo?"
- Se é o **cliente externo** → primário.
- Se é **outro processo interno** → suporte.
- Se é a **própria gestão/direção** (decisão, controle) → gerenciamento.

---

## ˙ . ꒷🍙 . 𖦹˙— 🐈‍⬛ 4. Visão Tradicional × Visão por Processos

| Atributo | Visão Tradicional (funcional) | Visão por Processos |
|---|---|---|
| Foco | Chefe | Cliente |
| Relacionamento primário | Cadeia de comando | Cliente / Fornecedor |
| Orientação | Hierárquica | Processo |
| Quem toma decisão | Gerência | Todos os participantes |
| Estilo | Autoritário | Participativo |

### Estrutura por processos vs. estrutura funcional ("efeito chaminé")
Na organização funcional clássica (dominante no séc. XX), a empresa é dividida em **silos verticais** (áreas/departamentos) que operam quase isolados, em paralelo, com pouca interligação horizontal — a chamada **abordagem das chaminés**. O problema: os processos de negócio, por serem inter-funcionais, **precisam atravessar essas fronteiras**, e é exatamente aí que se perde tempo, qualidade e capacidade de atendimento (retrabalho, filas entre setores, informação que não flui).

A organização orientada a processos (defendida como tendência dominante já a partir do fim do séc. XX/início do XXI) inverte a lógica: os recursos e fluxos são organizados **ao longo do processo**, não da função.

### Processo × Função — o exemplo do Departamento de Contabilidade
Este exemplo é ótimo para fixar a diferença:
- **Função** = grupo de atividades ligadas a uma tarefa específica, executada de forma **contínua e permanente** por especialistas (ex.: monitorar, medir e reportar informações financeiras).
- **Processo de negócio** = foca transações **ponta a ponta** que agregam valor ao cliente, e normalmente **atravessa** várias funções — a Contabilidade *participa* e *dá suporte* a processos de negócio (ex.: "Atender Pedido do Cliente"), mas não é dona sozinha do processo ponta a ponta.

Decorrência prática:
- **Gestão por Processos de Negócio (BPM)** = comprometimento **permanente e contínuo** da organização em gerenciar seus processos.
- **Iniciativas de Melhoria de Processos** = projetos pontuais (com início/fim) de redesenho ou ajuste de um processo específico.

> Vale reter essa distinção: BPM não é um projeto único — é uma disciplina de gestão contínua. Um projeto de melhoria é *um evento dentro* dessa disciplina, não o todo.

---

## 𖦹 ׂ 𓈒 🥞 ／ ⋆ ۪ 5. Medição e Desempenho

Frase-chave da aula (ideia central, geralmente atribuída a W. Edwards Deming, embora o slide credite "William Edwards"): não se gerencia o que não se mede, não se mede o que não se define, não se define o que não se entende, e por isso não há sucesso onde não há gerenciamento. **Essa cadeia lógica (entender → definir → medir → gerenciar) é o argumento central de por que BPM sempre trabalha junto de indicadores.**

Duas dimensões de desempenho — **essa dupla cai muito em prova**:

| Dimensão | Pergunta que responde | Foco |
|---|---|---|
| **Eficácia** | Estou atingindo a meta/o resultado esperado? | "Fazer as coisas certas" |
| **Eficiência** | Estou usando bem os recursos para chegar lá? | "Fazer bem as coisas" |

**Aprofundando a diferença (fora do slide, mas essencial para não confundir):** um processo pode ser **eficiente e ineficaz** ao mesmo tempo — por exemplo, produzir muito rápido e barato (eficiência alta) um produto que o cliente não queria (eficácia baixa, meta não atingida). O ideal em BPM é buscar as duas simultaneamente, mas quando há trade-off, geralmente a eficácia (fazer a coisa certa) deve vir antes da eficiência (fazer certo a coisa).

Formas típicas de reporte de desempenho, coletadas em pontos-chave do processo:
- Métricas de custo
- Tempo de conclusão de tarefas (lead time / tempo de ciclo)
- Alertas de variação de desempenho
- Gargalos (*bottlenecks*)
- Atrasos

---

## ﹒⌗﹒🦇﹒౨ৎ˚₊‧ 6. BPM CBOK® — as 9 áreas de conhecimento

O Guia BPM CBOK organiza o conhecimento em **9 áreas**, divididas em duas grandes perspectivas:

**Perspectiva Organizacional** (visão de cima, portfólio):
1. **Gerenciamento Corporativo de Processos** — maximiza os resultados dos processos alinhando-os às estratégias organizacionais; gerencia o portfólio de processos.
2. **Organização do Gerenciamento de Processos** — papéis, responsabilidades e estrutura de reporte para sustentar uma organização orientada a processos (cultura, desempenho de equipe).

**Perspectiva de Processo** (visão do processo em si, do início ao fim do seu ciclo de vida):
3. **Gerenciamento de Processos de Negócio** — conceitos essenciais: definições, processos ponta a ponta, valor ao cliente, natureza inter-funcional do trabalho; introduz tipos de processo, componentes e o ciclo de vida.
4. **Modelagem de Processos** — habilidades para representar, comunicar e avaliar os componentes do processo (ex.: notação BPMN).
5. **Análise de Processos** — entender eficiência/eficácia do processo atual; decomposição de componentes, técnicas analíticas, padrões.
6. **Desenho de Processos** — especificar o processo dentro do contexto de metas de negócio; define fluxos, regras e como sistemas/dados/controles interagem.
7. **Gerenciamento de Desempenho de Processos** — monitoramento formal da execução para decidir melhorar, redesenhar ou eliminar processos.
8. **Transformação de Processos** — mudanças no processo (melhoria, redesenho, reengenharia) dentro do ciclo de vida.
9. **Tecnologias de BPM** — ferramentas (BPMS, aplicações, infraestrutura, dados) que dão suporte a todas as fases anteriores.

**Aprofundando — por que essa ordem não é acidental:** repare que a sequência das áreas 3 a 9 segue quase exatamente as fases do **ciclo de vida BPM** (próxima seção): primeiro entende-se o conceito, depois modela-se, analisa-se, desenha-se, mede-se o desempenho, transforma-se, e por fim usa-se tecnologia para sustentar tudo isso. Isso ajuda a memorizar as 9 áreas relacionando cada uma a uma fase do ciclo de vida.

---

## ˚ ༘ 🦕𖦹⋆｡˚ 7. Ciclo de Vida BPM (6 fases)

O ciclo de vida é **contínuo** (não linear com fim definido) e representado como um círculo:

```
        Planejamento
             ↓
        Refinamento ←──────────┐
             ↑                 ↓
   Monitoramento &         Análise
      Controle                 ↓
             ↑            Desenho
             └── Implementação ←┘
```
*(sentido horário: Planejamento → Análise → Desenho → Implementação → Monitoramento & Controle → Refinamento → volta para Planejamento)*

| # | Fase | O que acontece |
|---|---|---|
| 1 | **Planejamento** | Desenvolve-se plano e estratégia dirigidos a processos; parte do entendimento das estratégias/metas da organização; define papéis, patrocínio executivo, metas e metodologias. Objetivo: entender como o processo se relaciona com o ambiente externo. |
| 2 | **Análise** | Entende-se os processos atuais no contexto das metas desejadas, usando planos estratégicos, modelos de processo, medições de desempenho e mudanças externas como insumo. |
| 3 | **Desenho e Modelagem** | Desenho intencional de como o trabalho ponta a ponta deve ocorrer para entregar valor. Envolve modelagem do processo e avaliação de fatores ambientais. Para organizações menos maduras, pode ser a **primeira vez** que o processo é documentado. |
| 4 | **Implementação** | Coloca em prática o desenho aprovado: procedimentos e fluxos de trabalho documentados, testados e operacionais; implanta políticas novas/revisadas. Pressupõe que as fases anteriores já geraram especificações completas — por isso só pequenos ajustes devem ocorrer aqui. |
| 5 | **Monitoramento e Controle** | Medição contínua fornece informação de desempenho via métricas ligadas às metas e ao valor gerado. A análise dessas informações **alimenta** decisões de melhoria, redesenho ou reengenharia. |
| 6 | **Refinamento** | Ajustes e melhorias pós-implementação com base nos indicadores coletados; fecha o ciclo, retroalimentando o Planejamento. |

Fatores que **habilitam ou restringem** a passagem do processo pelo ciclo: **valores, crenças, liderança e cultura** organizacional — ou seja, o ciclo não é puramente técnico, depende do ambiente humano/cultural da empresa.

**Aprofundando:** note que este é essencialmente um ciclo **PDCA aplicado a processos** (Planejar → Fazer/Desenhar-Implementar → Checar/Monitorar → Agir/Refinar). Se você já conhece PDCA (Plan-Do-Check-Act) de gestão da qualidade, pode mapear: Planejamento≈Plan, Desenho+Implementação≈Do, Monitoramento≈Check, Refinamento≈Act. Isso ajuda a entender por que o BPM CBOK trata gestão de processos como algo cíclico e nunca "terminado".

---

## ༄˖°.🍂.ೃ࿔*:･ 8. Mapeamento de Processos de Negócio

### 8.1 O que é e por que importa
**Fluxograma** = método para descrever graficamente um processo (existente ou proposto) usando símbolos, linhas e palavras, mostrando atividades e sua sequência. É a ferramenta mais simples e mais usada para entender o funcionamento interno e os relacionamentos entre processos.

Importância do fluxograma:
- Mostra como os elementos se relacionam.
- Permite comparar com o processo real (o que "deveria ser" vs. o que "é de fato").
- Ajuda a identificar como melhorar a atividade.
- Facilita a comunicação entre áreas.

### 8.2 Elementos de um Mapeamento de Processos
- **Raia** (*lane/pool*) — representa quem executa (papel, área ou sistema).
- **Stakeholders** envolvidos.
- **Início e fim** de cada processo.
- **Atividades** de cada participante.
- **Regras** para execução das atividades.
- **Sequência** das atividades.

### 8.3 Símbolos básicos de fluxograma
| Símbolo | Significado |
|---|---|
| Círculo/oval | Início / Fim |
| Seta | Sentido/fluxo da atividade |
| Retângulo | Atividade |
| Losango | Tomada de decisão (com saídas Sim/Não) |

### 8.4 Como conduzir uma sessão de mapeamento
Uma sessão de mapeamento é uma **reunião de trabalho com pessoas-chave** que dominam o processo, com o objetivo de definir e criticar o processo, identificar regras de trabalho e oportunidades de melhoria. Devem participar gestores **e** colaboradores de perfis diferentes na execução, buscando consenso sobre o melhor modelo.

Duas fases:
1. **Mapeamento em Grupo** — foco gerencial ou operacional; busca identificar características e necessidades do processo sob a visão de **cada papel envolvido**, buscando consenso entre os participantes.
2. **Mapeamento Individual** — foco mais operacional; detalha, especifica, exemplifica e valida o que foi levantado em grupo; o analista de processos documenta os aspectos operacionais e particularidades junto aos representantes dos principais papéis.

**Aprofundando:** essa lógica "grupo → individual" existe porque em grupo é fácil alinhar o entendimento geral (visão macro, consenso), mas é no levantamento individual, um a um, que aparecem exceções, regras de negócio escondidas e detalhes operacionais que ninguém menciona em reunião coletiva (por vergonha, esquecimento ou porque "acha óbvio"). É uma boa prática de elicitação de requisitos, não só de BPM.

### 8.5 Perguntas norteadoras (técnica 5W2H aplicada a processos)
Para cada atividade, questionar: por quê deve ser feita, o que faz e para quem, o que recebe e de quem, se realmente é necessária, quando deve ser feita, se as regras podem ser questionadas, se há recursos, se exige técnica/ferramenta, quem deve realizá-la, se a informação poderia seguir outro fluxo, onde deve ser executada, quanto pode custar.

O slide organiza isso em um quadro estruturado — essencialmente uma variação do **5W2H** (What, Who, When, Where, Why, How, How much):

| Pergunta | O que investiga |
|---|---|
| **Quem?** | Cliente/usuário/beneficiário, quem executa, quem gerencia, quem fornece, quem decide |
| **O quê?** | Entradas, saídas, indicadores, metas, recursos/ferramentas, problemas, pontos positivos, métodos/tecnologias |
| **Quando?** | Quando é planejado, executado, avaliado |
| **Onde?** | Onde é planejado, executado, avaliado |
| **Por quê?** | Por que/para que o processo existe |
| **Como?** | Como é planejado, executado, avaliado, como as informações são registradas/disseminadas, como se avalia satisfação do cliente e desempenho |

> Essa é literalmente a checklist que um engenheiro de requisitos usa para levantar um processo de negócio antes de especificar um sistema — vale guardar como roteiro de entrevista.

### 8.6 Hierarquia de Processos
A aula apresenta uma pirâmide com 5 níveis, do mais amplo/estratégico ao mais granular:

```
        Processos Empresariais   (crítico para o negócio e satisfação do cliente)
               ↓
            Processos            (conjunto de atividades que iniciam e terminam com o cliente externo)
               ↓
          Sub-processos          (grupos de atividades que envolvem 1+ departamentos)
               ↓
           Atividades            (trabalho tipicamente executado por um departamento/pessoa)
               ↓
            Tarefas               (ações realizadas dentro de uma atividade)
```

Definições formais complementares:
- **Processo** — conjunto de atividades inter-relacionadas que transformam entradas em saídas.
- **Sub-processo** — mesma definição, em escala menor; segundo o material, é reaproveitável e tem certa independência em relação aos processos que o contêm; **ao terminar, sempre remete de volta ao processo principal**.
- **Atividade** — ações realizadas dentro dos processos/sub-processos na transformação de entrada em saída.
- **Tarefa** — ações realizadas dentro das atividades; nível mais granular, com objetivos e prazos bem definidos. A granularidade escolhida para definir uma atividade depende do nível de controle gerencial desejado sobre o processo. Podem ser manuais ou automatizadas (parcial ou totalmente) — quando manual, deve **obrigatoriamente** ter um responsável (pessoa ou papel/role) associado.
- **Regra** — condição que norteia ou permite desvios na execução de atividades/tarefas; conjunto de informações do mesmo domínio e tamanho.

### 8.7 Rotas de fluxo (usadas ao desenhar o processo)
| Tipo de rota | Comportamento |
|---|---|
| **Sequencial** | As atividades ocorrem uma após a outra, em ordem única |
| **Paralela** | Duas ou mais atividades ocorrem ao mesmo tempo, sem dependência entre si |
| **Condicional** | O fluxo se bifurca conforme uma condição (regra), seguindo apenas um dos caminhos |

Cuidado especial ao desenhar rotas paralelas/condicionais: identificar o **domínio dos dados alterados**, as **precedências** entre atividades e a **junção posterior** dos fluxos (onde e como os caminhos se reencontram).

### 8.8 Exemplo prático trabalhado em aula — "Controlar Vendas"
Narrativa do processo: o cliente seleciona o produto e faz o pedido → o atendente cadastra o pedido e verifica a forma de pagamento → se não for em dinheiro, solicita autorização (aciona sub-processo "Analisar Crédito") → recebe o pagamento → entrega a mercadoria → verifica o estoque → se estiver baixo, aciona o processo de compra.

Esse exemplo simples é usado para demonstrar, camada por camada, os conceitos acima:
- O fluxo principal é o **processo** "Controlar Vendas".
- "Analisar Crédito" é um **sub-processo** acionado condicionalmente (pagamento ≠ dinheiro).
- Cada caixa do fluxo (cadastrar pedido, receber pagamento, entregar mercadoria, verificar estoque) é uma **atividade**.
- Dentro de "Analisar Crédito", aparecem tarefas mais granulares (efetuar triagem, autorizar cartão, pesquisar cadastro).
- A integração tecnológica é citada como exemplo de automação: dependendo da ferramenta usada, a checagem de estoque pode disparar programas/scripts automaticamente.

### 8.9 Notação BPMN
BPMN (*Business Process Model and Notation*) é citada como a notação usada para desenhar processos de forma padronizada, com elementos como:
- **Raias/lanes** (quem faz o quê, ex.: "Usuário", "Grupo de aprovação").
- **Eventos** (círculos — início em verde, fim em vermelho).
- **Tarefas** (retângulos com cantos arredondados).
- **Gateways** (losangos, ex.: com "X" para decisão exclusiva) — pontos de decisão que direcionam o fluxo conforme uma condição.

O exemplo de aula mostra um processo de "baixa manual" com várias raias (Usuário, Grupo de aprovação, Lane 1), decisão de autorização (gateway) e dois desfechos possíveis (baixa autorizada / baixa recusada) — ilustrando na prática os conceitos de rota condicional e responsável por atividade manual vistos antes.

---

## ℳ𝑦 ℒ𖹭𝑣𝑒 9. Síntese — conectando tudo

1. **Negócio** entrega valor via **processos**; processos de negócio são **ponta a ponta** e **inter-funcionais**.
2. Processos se dividem em **primários, de suporte e gerenciais**; e se organizam numa **hierarquia** (processo → sub-processo → atividade → tarefa → regra).
3. Gerenciar processos bem exige medir **eficácia** (meta certa) e **eficiência** (uso certo de recursos).
4. O **BPM CBOK** organiza esse conhecimento em **9 áreas**, que seguem a lógica do **ciclo de vida BPM** (Planejamento → Análise → Desenho → Implementação → Monitoramento → Refinamento), um ciclo contínuo, não um projeto único.
5. Na prática, tudo isso se materializa através do **mapeamento de processos** (fluxogramas, notação BPMN), guiado por perguntas estruturadas (quem, o quê, quando, onde, por quê, como) para levantar o processo real junto às pessoas que o executam.

---

## ִֶָ𓂃 ࣪ ִֶָ🐇་༘࿐ 10. Referências citadas na aula
**Básica:** Baldam et al. (2007) — *Gerenciamento de Processos de Negócios: BPM*; Oliveira, S. B. (2006) — *Gestão por Processos*; Stair & Reynolds (2006) — *Princípios de Sistemas de Informação*; McGee & Prusak (2000) — *Gerenciamento Estratégico da Informação*.
**Complementar:** Batista (2004); Oliveira, D. P. R. (2000) — *Sistemas, Organização e Métodos*; Beal (2004); Oliveira, J. F. (2004).
