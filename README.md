# Bootcamp_DIO
Repositório dedicado ao estudo aprofundado de Inteligência Artificial Generativa, LLMs e Engenharia de Prompt. Contém curadoria de fontes, experimentações com prompts, análises técnicas e um guia estruturado para aplicação prática de IA em contextos acadêmicos e profissionais.

Caderno Temático: Ideologia de Investimentos e Metodologia de Benjamin Graham
--Image of: --NotebookLM --Image of: --GitHub --Image of: --DIO

1. Contexto e Objetivos
Contexto
O presente projeto foi desenvolvido como entrega do Desafio de Projeto da plataforma DIO (Digital Innovation One), com o objetivo de explorar o uso da Inteligência Artificial como uma ferramenta de aprendizagem ativa, curadoria de fontes e organização do conhecimento utilizando o NotebookLM.

O domínio de estudo escolhido aborda a Ideologia de Investimentos e Metodologia de Benjamin Graham, pai do Value Investing (Investimento em Valor) e mentor de Warren Buffett. A partir de uma análise quantitativa e qualitativa rigorosa das obras clássicas de Graham (Security Analysis e The Intelligent Investor), este material organiza os princípios teóricos, operacionais e de avaliação de empresas (valuation) desenvolvidos pelo autor.

**Objetivos**
- _Distinguir Investimento de Especulação:_ Estabelecer a fronteira conceitual entre operações de investimento fundamentadas e atividades especulativas de mercado.
- _Compreender a Psicologia do Sr. Mercado:_ Analisar a metáfora do "Sr. Mercado" e a importância da disciplina emocional no comportamento do investidor.
- _Mapear Perfis de Investidores:_ Detalhar as diretrizes operacionais, limites de risco e alocação de ativos para os perfis Defensivo (Passivo) e Empreendedor (Ativo).
- _Dominar Fórmulas e Métricas de Valuation:_ Sistematizar o cálculo e a aplicação do Número de Graham, da Fórmula de Graham (Clássica e Revisada) e do método Net-Net (NCAV).
- _Documentar a Engenharia de Prompts:_ Registrar a evolução dos testes de prompts no NotebookLM, evidenciando as estratégias de extração de conhecimento e resoluções de inconsistências (troubleshooting).

**Curadoria de Fontes**
Para garantir uma base documental sólida e devidamente fundamentada no caderno de estudos, foram selecionadas e analisadas 5 fontes abertas em texto, artigos e vídeos sobre a metodologia de Benjamin Graham:

Fonte / Documento	Tipo / Formato	Descrição / Tópicos Cobertos
_Metodologia de Investimento de Benjamin Graham:_ Fundamentos Teóricos, Diretrizes Operacionais e Validação Empírica	Markdown	Análise exaustiva dos fundamentos teóricos, diferenciação de perfis (Defensivo vs. Empreendedor), modelagens matemáticas ($V$, Número de Graham, Net-Net), sinais contábeis e validações empíricas.
Fórmula Benjamin Graham: Cálculo e Método - Investing.com	Artigo Web	Apresentação detalhada da fórmula básica $V = LPA \times (8,5 + 2g)$ e da fórmula revisada com a taxa de títulos corporativos $Y$, com exemplos práticos.
_Benjamin Graham's 7 Stock Criteria for Defensive Investors	Bajaj Finance_	Artigo Web
O Investidor Inteligente, de Benjamin Graham - Finanças Pessoais & Literacia Financeira	Artigo Web	Síntese sobre os conceitos de valor intrínseco, margem de segurança, psicologia do investidor e a metáfora do Sr. Mercado.
O Método de Benjamin Graham para Ações de Valor - ivalor	Artigo Web	Explanação sobre a margem de segurança, a fórmula do Número de Graham $\sqrt{22,5 \times LPA \times VPA}$ e para quais tipos de empresas o método se aplica.

**Engenharia de Prompts e "Cicatrizes" (Troubleshooting)**
Nesta seção, documentam-se as estratégias de formulação de perguntas e a evolução dos prompts utilizados para instruir a Inteligência Artificial no NotebookLM, destacando os desafios encontrados e como foram superados.

**Perguntas Estratégicas Elaboradas**
"Qual é a definição exata de investimento para Benjamin Graham e como ela se difere da especulação?"
"Quais são os 7 filtros quantitativos exigidos para o Investidor Defensivo e como eles se comparam com os filtros do Investidor Empreendedor?"
"Como calcular o Valor Intrínseco usando a Fórmula de Graham Clássica, a Fórmula Revisada de 1974 e o Número de Graham? Explicite a origem das constantes."
"Como a alegoria do Sr. Mercado e o conceito de Margem de Segurança se integram no processo de tomada de decisão de investimento?"

**Testes de Prompts e Variações**

- _Teste 1:_ Comparativo de Perfis de Investidor
Prompt Inicial (Simples): "Qual a diferença entre investidor defensivo e empreendedor segundo Graham?"
Resultado Obtido: Uma explicação superficial citando que um é passivo e o outro é ativo.
Refinamento (Prompt Estruturado): "Compare em formato de tabela as diretrizes operacionais do Investidor Defensivo (Cap. 14) e do Investidor Empreendedor (Cap. 15), detalhando os critérios de tamanho de empresa, liquidez corrente, estrutura de dívida, P/L e P/VP segundo as fontes do caderno."
Resultado Refinado: Retorno de uma matriz comparativa completa com os parâmetros quantitativos de ambos os perfis.

- _Teste 2:_ Esclarecimento da Fórmula e Constante 22,5
Prompt Inicial: "Qual a fórmula do valor intrínseco de Graham?"
Resultado Obtido: Apresentou a fórmula $\sqrt{22,5 \times LPA \times VPA}$ sem explicar a origem da constante 22,5 nem mencionar a fórmula de crescimento $V = LPA \times (8,5 + 2g)$.
Refinamento ("Troubleshooting"): "Explique as duas modelagens de Graham para valuation: (1) O Número de Graham $\sqrt{22,5 \times LPA \times VPA}$, demonstrando como se chega na constante 22,5 a partir de $P/L \le 15$ e $P/VP \le 1,5$; e (2) A fórmula $V = LPA \times (8,5 + 2g)$, esclarecendo o significado das variáveis e como a versão de 1974 ajusta o rendimento dos títulos corporativos $Y$."
Resultado Refinado: Explicação matemática precisa, detalhando que $15 \times 1,5 = 22,5$ e que a versão de 1974 inclui a taxa básica de juros/títulos corporativos AAA ($Y$) para considerar o valor do dinheiro no tempo.

**"Cicatrizes" e Dificuldades Encontradas (Troubleshooting)**
Inconsistência entre Métricas Antigas e Atualizações Modernas:
Problema: As fontes históricas citavam faturamentos mínimos de US$ 100 milhões para empresas industriais (edição de 1973), enquanto fontes modernas ajustavam esses valores para US$ 1 bilhão ou US$ 2 bilhões em market cap.
Solução: Estruturou-se o prompt para solicitar explicitamente a distinção entre a base histórica original de Graham e as adaptações contemporâneas recomendadas por analistas modernos (como Jason Zweig).
Confusão entre Preço de Mercado e Valor Intrínseco:
Problema: Em algumas consultas, a IA misturava a volatilidade da cotação com a perda real de patrimônio.
Solução: O prompt foi ajustado para forçar a diferenciação fundamentada na alegoria do Sr. Mercado e no conceito de Margem de Segurança, ressaltando que oscilações temporárias de cotação não representam perda permanente de capital se os fundamentos do negócio se mantiverem hígidos.

**Miniguia de Estudo**
Este Miniguia consolida o conhecimento extraído das fontes, organizado de forma estruturada para rápida consulta e revisão.

**Resumos Estruturados do Assunto**
**A.** Investimento vs. Especulação e a Psicologia do Sr. Mercado
Operação de Investimento: Operação que, mediante análise financeira exaustiva, promete a segurança do capital principal e um retorno adequado. Qualquer operação que não atenda a essas condições cumulativas é caracterizada como especulativa.
A Alegoria do Sr. Mercado: O mercado acionário é personificado como um sócio de negócios que, diariamente, oferece preços para comprar ou vender participações na empresa. Ele oscila entre a euforia e o pessimismo profundo. O investidor racional utiliza as oscilações irracionais do Sr. Mercado a seu favor — comprando quando ele está euforicamente deprimido e vendendo quando ele está excessivamente otimista.
**B.** O Conceito Fundamental da Margem de Segurança (Margin of Safety)
Definição: É a diferença positiva entre o valor intrínseco de uma empresa (baseado em seus ativos, lucros e fluxos de caixa) e o seu preço de mercado.
Função Prática: Atua como um colchão de proteção contra erros analíticos, variações imprevisíveis da economia ou reveses operacionais da empresa. Permite obter assimetria favorável entre risco e retorno.
**C.** Perfis de Investidores e Filtros Quantitativos de Graham
- Investidor Defensivo (Passivo)
Objetivo: Segurança do capital, simplicidade de acompanhamento e ausência de estresse com o mercado.
Alocação Recomendada: Divisão inicial de 50% em ações de empresas líderes e 50% em títulos de renda fixa de alta qualidade (variando de 25% a 75% conforme a valoração do mercado).
Rebalanceamento: Ajustar o portfólio periodicamente (ex: semestralmente ou quando a alocação desviar para 60/40) para restaurar a proporção desejada.
Os 7 Filtros do Investidor Defensivo:
Tamanho Adequado: Empresas de grande porte (faturamento/vendas expressivos).
Condição Financeira Forte: Liquidez Corrente $\ge 2,0$ ($\frac{\text{Ativo Circulante}}{\text{Passivo Circulante}} \ge 2,0$) e Dívida de Longo Prazo $\le$ Capital de Giro Líquido.
Estabilidade de Lucros: Lucro líquido positivo ininterrupto nos últimos 10 anos.
Histórico de Dividendos: Pagamento contínuo de dividendos por pelo menos 20 anos consecutivos.
Crescimento de Lucros: Crescimento acumulado do LPA de pelo menos 33% nos últimos 10 anos (utilizando médias de 3 anos no início e no fim).
Múltiplo P/L Moderado: Preço da ação no máximo 15 vezes a média dos lucros dos últimos 3 anos.
Múltiplo P/VP Moderado: Preço em relação ao Valor Patrimonial (P/VP) no máximo 1,5.

- Investidor Empreendedor (Ativo)
Objetivo: Obter retorno acima da média aplicando maior esforço analítico na busca por barganhas e situações especiais.
Filtros Flexibilizados do Empreendedor:
Tamanho da Empresa: Faturamento anual $\ge$ US$ 500 milhões (ajustado por inflação).
Liquidez Corrente: $\ge 1,5$.
Estrutura de Dívida: Dívida de Longo Prazo $\le 110%$ do Capital de Giro Líquido.
Estabilidade de Lucros: Lucro líquido positivo nos últimos 5 anos consecutivos.
Dividendos: Pagamento regular de dividendos correntes.
Crescimento de Lucros: LPA atual superior ao registrado há 5 anos.
Múltiplo P/L: $P/L \le 10,0$ (ou no decil mais barato do mercado).
Múltiplo P/VP: $P/VPA \text{ tangível} < 1,2$

**Modelos Matemáticos de Valuation de Graham**
_Modelo de Valuation	Equação / Fórmula	Descrição e Parâmetros_
Número de Graham	$\text{Preço Máximo} = \sqrt{22,5 \times \text{LPA} \times \text{VPA}}$	Determina o preço teto para compra defensiva. A constante 22,5 decorre do produto de um $P/L \le 15$ por um $P/VP \le 1,5$ ($15 \times 1,5 = 22,5$).
Fórmula Clássica de Graham	$V = \text{LPA} \times (8,5 + 2g)$	$V$ = Valor Intrínseco; $\text{LPA}$ = Lucro Por Ação dos últimos 12 meses; $8,5$ = P/L base de uma empresa sem crescimento ($g=0$); $g$ = taxa percentual de crescimento esperada dos lucros.
Fórmula Revisada de Graham (1974)	$V = \frac{\text{LPA} \times (8,5 + 2g) \times 4,4}{Y}$	Incorpora $4,4$ (rendimento médio dos títulos corporativos AAA na década de 1960) e $Y$ (rendimento atual dos títulos corporativos AAA) para refletir o custo de oportunidade e o valor do dinheiro no tempo.
Ativo Circulante Líquido (Net-Net / NCAV)	$\text{NCAV/Ação} = \frac{\text{Ativo Circulante} - \text{Passivos Totais} - \text{Ações Pref.}}{\text{Ações em Circulação}}$	A abordagem mais conservadora de Graham ("bituca de charuto"). Recomenda compra quando $\text{Preço} \le \frac{2}{3} \times \text{NCAV}$.

**Glossário com os Principais Conceitos Aprendidos**
Valor Intrínseco ($V$): O valor real estimado de um negócio fundamentado em seus ativos contábeis, lucros normalizados, dividendos e capacidade de geração de caixa futura, independentemente da cotação momentânea do mercado.
Margem de Segurança (Margin of Safety): Princípio central do investimento racional que exige a compra de um ativo a um preço substancialmente inferior ao seu valor intrínseco para mitigar riscos de erros de projeção ou oscilações de mercado.
Sr. Mercado (Mr. Market): Alegoria criada por Graham para representar a insanidade e a volatilidade emocional do mercado de ações, que diariamente oferece preços de compra e venda movidos por euforia ou pânico.
Investidor Defensivo: Perfil de investidor focado na preservação de capital, simplicidade de gestão e retornos moderados, utilizando seleções diversificadas em empresas consolidadas e títulos de renda fixa.
Investidor Empreendedor: Perfil de investidor ativo disposto a despender elevado esforço de pesquisa e análise financeira para capturar barganhas subavaliadas e situações especiais.
Lucro Por Ação (LPA): Indicador que representa a parcela do lucro líquido atribuída a cada ação ordinária em circulação de uma companhia.
Valor Patrimonial por Ação (VPA): Indicador que mede a fração do patrimônio líquido contábil pertencente a cada ação da empresa.
Índice P/L (Preço / Lucro): Múltiplo que indica quantos anos de lucros correntes o mercado está pagando pela ação de uma empresa.
Índice P/VP (Preço / Valor Patrimonial): Múltiplo que compara a cotação de mercado de uma ação com o seu valor patrimonial contábil.
Net-Net / NCAV (Net Current Asset Value): Técnica de valoração ultra-conservadora desenvolvida por Graham que avalia a empresa apenas pelos seus ativos circulantes líquidos após a quitação de todas as suas dívidas e obrigações totais.
