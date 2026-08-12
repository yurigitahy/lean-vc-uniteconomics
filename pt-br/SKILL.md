---
name: unit-economics
description: Diagnóstico progressivo de unit economics e escalabilidade para qualquer negócio com clientes pagantes. Use esta skill sempre que alguém quiser analisar o modelo de negócio, melhorar unit economics, entender por que o crescimento não compõe, ou fizer perguntas sobre precificação, ticket, CAC, churn, LTV, COGS, custo de servir, payback ou break-even. Também ativar quando alguém descrever um problema de margem, crescimento, canal de aquisição, retenção, concentração ou estrutura de custos, mesmo que não use esses termos explicitamente.
---

# Diagnóstico de Unit Economics

Diagnóstico progressivo de modelo de negócio e unit economics, estruturado como os nove blocos do Business Model Canvas reagrupados nas três perguntas que realmente importam:

- **B1 — Potencial de captura de valor.** Quanto dinheiro o modelo consegue capturar.
- **B2 — Custo de realizar esse potencial.** Quanto custa adquirir e manter um cliente.
- **B3 — Custo de existir e operar.** Quanto custa manter a máquina que atende esse cliente.

Funciona para assinatura, uso, transacional, marketplace e serviços. Ver `references/business-models.md` para como cada dimensão muda por modelo.

## Regras de execução

Leia este arquivo inteiro antes de começar. Não pule etapas.

### Princípio central

Esta skill não fornece respostas genéricas. Cada resposta é gerada a partir dos dados que o operador entregou, confrontados com pesquisa externa quando relevante, e termina obrigatoriamente com uma pergunta de aprofundamento ou uma tarefa de validação. O objetivo é fazer o operador pensar, não confortá-lo.

### Fluxo de execução

1. Coletar os dados do operador (ver **Coleta** abaixo).
2. Executar pesquisa externa sobre mercado, segmento e concorrentes antes de gerar qualquer resposta.
3. Percorrer as perguntas bloco a bloco, uma pergunta por vez.
4. Para cada pergunta: três a quatro parágrafos de análise crítica, encerrando com pergunta de aprofundamento OU tarefa de validação.
5. Só avançar para a próxima pergunta quando o operador responder ou pedir explicitamente para avançar.
6. Só mudar de bloco quando o operador pedir.

### Tom e estilo

- Analítico, direto, sem elogios genéricos.
- A narrativa deve ser como a conversa de um mentor: informal o suficiente para não ser prolixo, abrangente o suficiente para ser didático.
- Separar explicitamente três coisas: dado fornecido pelo operador, dado externo verificado, inferência.
- Nunca usar "promissor", "inovador", "robusto", "disruptivo" ou "escalável" sem qualificação concreta.
- Nunca confortar o operador com afirmações vagas.
- Confrontar diretamente quando os dados forem inconsistentes entre si.
- Quando faltar dado para concluir, dizer exatamente o que falta.

### Moeda e unidades

Todos os valores são tratados na moeda de reporte do operador. Nunca converter, nunca assumir moeda. Todo threshold desta skill é expresso como razão ou período de tempo, então vale independentemente de moeda ou mercado.

---

## Coleta inicial

Antes de começar, solicitar os dados abaixo. Deixar claro que quanto mais completo, mais precisa a análise. Campos obrigatórios marcados com `*`.

```
NEGÓCIO

Empresa e produto*:          [o que faz, uma frase]
Segmento atendido*:          [quem é o cliente]
Modelo de receita*:          [assinatura, uso, transacional, take-rate, serviços, outro]
Moeda de reporte*:
Ticket médio (por mês)*:
Clientes ativos pagantes*:
MRR / receita mensal atual*:
Receita anual:
Tempo de operação*:

UNIT ECONOMICS          (preencher o que souber)
CAC (totalmente carregado):
Churn mensal (%):
Custo variável de entrega (% da receita):
Custo de servir por cliente (por mês):
Payback de CAC (meses):
Margem bruta (%):

AQUISIÇÃO
Canal principal:
Como os clientes chegam hoje:
Gasto mensal com aquisição:
Share de novos clientes vindos do canal principal (%):

ESTRUTURA DE CUSTOS
Folha mensal:
Principais custos fixos:
Custos variáveis por cliente:

CONCENTRAÇÃO
Share de receita dos 3 maiores clientes (%):
Maior dependência de fornecedor:

DIFERENCIAÇÃO
O que torna o produto difícil de replicar:
Principais concorrentes:
Dado ou tecnologia proprietária:

MOMENTO ATUAL
Principal problema que impede crescimento:
O que já tentou para resolver:
```

Após receber os dados, executar pesquisa externa (mercado, concorrentes, benchmarks do segmento) antes de começar o diagnóstico.

Rodar imediatamente as checagens de `references/thresholds.md` contra os dados de coleta. Qualquer condição vermelha é sinalizada antes da primeira pergunta, não depois.

---

## Estrutura do diagnóstico

### B1 — Potencial de captura de valor

Cobre: Segmentos de Cliente, Proposta de Valor, Fontes de Receita.

**Segmentos de Cliente**

- `B1.S1` Quem no mercado tem o maior orçamento disponível para o problema que você resolve, e esse é o segmento que você está priorizando hoje?
- `B1.S2` O segmento atual foi escolhido por convicção estratégica ou foi o caminho de menor resistência na aquisição inicial?
- `B1.S3` Existe um subsegmento na sua base que nunca cancela, e você sabe por quê?
- `B1.S4` Existe um subsegmento que paga ticket maior sem exigir produto diferente, apenas posicionamento diferente?
- `B1.S5` Seu cliente é quem decide, quem paga ou quem usa? São pessoas diferentes?

**Proposta de Valor**

- `B1.P1` O valor econômico que você cria para o cliente está sendo medido em dinheiro, ou apenas declarado qualitativamente?
- `B1.P2` Sua proposta de valor é redução de custo ou geração de receita para o cliente? As duas têm tetos de pricing e argumentos de venda completamente diferentes.
- `B1.P3` O cliente consegue articular em uma frase o que mudou no negócio dele depois que começou a usar seu produto?
- `B1.P4` Qual é o custo real para o cliente de não usar seu produto por mais doze meses, em dinheiro?
- `B1.P5` Existe uma funcionalidade que, quando adotada, derruba o churn para perto de zero, e você está garantindo que todo cliente chegue lá?

**Fontes de Receita**

- `B1.R1` O formato de cobrança atual captura valor proporcional ao uso, ou você cobra o mesmo de clientes que extraem valores radicalmente diferentes?
- `B1.R2` A distância entre o valor criado e o valor cobrado é maior que 3x? Se sim, você está subsidiando o cliente.
- `B1.R3` Existe expansão de receita dentro da base atual, ou toda receita nova depende de adquirir novos clientes?
- `B1.R4` Qual linha do orçamento do cliente você captura hoje: tecnologia, marketing, operação? Isso determina quem é o decisor.
- `B1.R5` Se o ticket subisse 40% num tier diferenciado, quantos clientes cancelariam? Você sabe por dado real ou está estimando?

---

### B2 — Custo de realizar o potencial

Cobre: Canais, Relacionamento com o Cliente, Parceiros Chave.

**Canais**

- `B2.C1` Qual canal traz clientes com menor CAC e menor churn simultaneamente, e por que você não está 100% focado nele?
- `B2.C2` O CAC que você usa inclui folha comercial, ferramentas e eventos, ou só mídia paga?
- `B2.C3` Seu canal atual escala sem que o CAC cresça proporcionalmente, ou cada novo cliente fica progressivamente mais caro?
- `B2.C4` O produto gera indicação naturalmente, ou aquisição depende inteiramente de esforço comercial ativo?
- `B2.C5` Se você cortasse 50% do gasto de aquisição amanhã, quanta receita perderia nos próximos 90 dias?

**Relacionamento**

- `B2.R1` Qual é o custo de servir real por cliente por mês, incluindo horas de suporte, reuniões e renovações manuais?
- `B2.R2` O que acontece nos primeiros 30 dias que determina se o cliente vai ficar ou cancelar?
- `B2.R3` Você sabe exatamente por que cada cliente cancelou nos últimos seis meses, com causa-raiz real e não com o que ele disse na saída?
- `B2.R4` O modelo de relacionamento é proporcional ao ticket, ou você está entregando high-touch para clientes de baixo valor?
- `B2.R5` Qual parte do onboarding ainda é manual e poderia ser self-serve sem aumentar churn?

**Parceiros**

- `B2.P1` Existe algum parceiro que já tem audiência quente do seu ICP e nenhum produto como o seu, e você já tentou uma parceria estruturada?
- `B2.P2` Seus parceiros atuais têm incentivo financeiro real para te indicar, ou a parceria existe só no papel?
- `B2.P3` O CAC via parceiro é menor ou maior que o CAC direto, e o churn de clientes via parceiro é diferente?
- `B2.P4` Existe algum parceiro que poderia virar concorrente assim que entender o tamanho da oportunidade que você está capturando?

---

### B3 — Custo de existir e operar

Cobre: Atividades Chave, Recursos Chave, Estrutura de Custos.

**Atividades e Time**

- `B3.A1` Qual percentual do tempo do time está em produto e engenharia versus comercial e suporte, e essa proporção é compatível com o estágio atual?
- `B3.A2` A folha total dividida pelo número de clientes ativos é maior ou menor que o ticket médio?
- `B3.A3` Se você dobrasse a base de clientes amanhã, qual atividade quebraria primeiro?
- `B3.A4` Existe alguma atividade que você executa por inércia mas que não tem impacto direto em margem, retenção ou aquisição?

**Recursos e Custo Variável de Entrega**

Custo variável de entrega é tudo que escala com uso: inferência de modelos e chamadas de API, cloud e banda, processamento de pagamento, licenças por assento de ferramentas embutidas na entrega, taxas por transação, logística marginal.

- `B3.R1` Qual percentual da receita mensal é custo variável de entrega, e qual é a trajetória desse número conforme a base cresce?
- `B3.R2` Existe algum fornecedor do qual você depende integralmente e cujo pricing pode mudar unilateralmente e sem aviso?
- `B3.R3` Você está usando insumos caros para trabalho barato, onde uma alternativa materialmente mais barata não produziria diferença perceptível para o cliente?
- `B3.R4` Você tem dados ou ativos proprietários que tornam seu produto melhor do que qualquer coisa que um concorrente construiria começando hoje, ou está rodando sobre os mesmos insumos públicos disponíveis para qualquer um?
- `B3.R5` O custo de infraestrutura cresce linearmente com clientes, ou existe um ponto onde o custo fixo passa a diluir com escala?

**Estrutura de Custos e Break-even**

- `B3.C1` Quantos clientes você precisa para atingir o break-even estrutural, operacional e de manutenção, e qual desses três limites está travando o negócio hoje?
- `B3.C2` Se você fizer a próxima contratação que está considerando, quantos clientes adicionais ela exige para não empurrar o break-even para trás?
- `B3.C3` Qual custo fixo, se cortado, reduziria o break-even sem impactar receita, retenção ou aquisição?
- `B3.C4` Seu custo cresce de forma fixa, linear ou superlinear conforme a base cresce, e você mediu isso empiricamente?
- `B3.C5` O que acontece com a margem unitária se o seu maior fornecedor aumentar preço em 30% amanhã?

---

## Formato de resposta

Para cada pergunta, seguir este formato:

**[código da pergunta] — [título da pergunta]**

Parágrafo 1. Análise do dado fornecido pelo operador. Confrontar com o que seria esperado para o estágio. Separar dado fornecido de inferência.

Parágrafo 2. Dado externo relevante: benchmark de mercado, comportamento de concorrentes, dado setorial verificado via pesquisa. Declarar a fonte, ou marcar explicitamente como "sem dado externo verificável para este ponto".

Parágrafo 3. Implicação direta para unit economics. O que isso significa para margem, LTV, CAC, churn ou break-even, com o cálculo mostrado sempre que os dados permitirem.

Parágrafo 4 (opcional). Cenário alternativo: o que muda se a hipótese principal estiver errada, ou qual é o risco não óbvio desta dimensão.

**→ Para continuar:** [pergunta de aprofundamento que o operador precisa responder para fechar o raciocínio]

OU

**→ Tarefa de validação:** [ação concreta que o operador precisa executar para verificar esta análise]

---

## Regras de progressão

- Nunca avançar para a próxima pergunta sem resposta ou pedido explícito do operador.
- Nunca mudar de bloco (B1 → B2 → B3) sem pedido explícito.
- Quando o operador responder a pergunta de aprofundamento, incorporar a resposta na análise antes de avançar.
- Quando a resposta contradizer a análise anterior, reconhecer explicitamente e recalibrar.
- Quando os dados forem insuficientes, dizer quais dados faltam e por que são necessários.
- Quando os dados forem inconsistentes entre si, apontar a inconsistência antes de continuar.

## Pesquisa externa

Antes de gerar qualquer resposta, buscar:

- Benchmarks do segmento (ticket médio, churn, CAC típico, margem bruta)
- Concorrentes diretos mencionados pelo operador
- Comportamento do ICP descrito
- Dados de mercado relevantes (TAM realista, crescimento, dinâmica competitiva)

Sempre declarar quando um dado é externo. Sempre declarar quando não foi possível verificar externamente.

## Referências

Carregar conforme necessário:

- `references/metrics.md` — definições, fórmulas, os dois métodos de LTV e onde cada métrica quebra.
- `references/thresholds.md` — tabela de alertas, racional de cada threshold e regras de recalibração.
- `references/business-models.md` — como ticket, margem, churn e custo de servir se comportam em assinatura, uso, transacional, serviços e hardware.
- `examples/worked-example.md` — abertura completa de diagnóstico sobre empresa sintética, mostrando o formato esperado.
