# Compilador TINYPy

Um compilador para a linguagem simples [TINYPy](TINYPy.md).

O trabalho deve atender três componentes básicos de um compilador:

### Analisador Léxico

Componente responsável pela primeira fase de um compilador, chamada de *análise léxica* ou *leitura (scanning)*. O analisador léxico lê o fluxo de caracteres que compõem o programa fonte e os agrupa em sequências significativas, chamadas *lexemas*. Para cada lexema o analisador léxico produz como saída um *token* no formato `<nome-token, valor-atributo>` que é passado para a fase subsequente, a análise sintática. O primeiro componente de um token, *nome-token*, é um símbolo abstrato usado durante a análise sintática; já o segundo componente, *valor-atributo*, aponta para uma entrada na tabela de símbolos referente a esse token.

### Analisador Sintático

Componente responsável pela segunda fase do compilador, a *análise sintática*. O analisador sintático utiliza os primeiros componentes dos tokens produzidos pelo analisador léxico para criar uma representação intermediária tipo árvore &mdash; *árvore de sintaxe* &mdash; que mostra a estrutura gramatical da sequência de tokens.

### Analisador Semântico e Gerador de Código

Componente responsável pelas etapas de *análise semântica* e *geração de código* do compilador. O analisador semântico utiliza a árvore de sintaxe e as informações na tabela de símbolos para verificar a consistência semântica do programa fonte com a definição da linguagem. Ele também reune informações sobre os tipos  e as salva na árvore de sintaxe ou na tabela de símbolos, para uso subsequente durante a geração de código intermediário. Uma parte importante da análise semântica é a *verificação de tipo*, em que o compilador verifica se cada operador possui operandos compatíveis. O gerador de código tem por objetivo gerar um representação intermediária explícita a partir da árvore de sintaxe e que posteriormente será traduzida para a linguagem de máquina alvo.

Sob a [licença GPLv2](../LICENSE).
