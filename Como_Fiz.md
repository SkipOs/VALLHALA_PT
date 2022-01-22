# TRADUÇÃO DOS SCRIPTS
O jogo trabalha com os roteiros de cada capítulo e personagem, como um teatro. Esses roteiros estavam disponíveis na pasta `../scripts/eng/` o quê facilitou muito na hora de editar e descobrir cada um dos comandos inseridos.

A estrutura básica de um fragmento de texto do jogador é:

`[XS:jilltalk,1][C:13]Jill:[C:C] G'night.[STOPLIP:]`

Outro exemplo é um fragmento de texto de NPC:

`[XS:gilface,][XS:giltalk,1][C:19]Gillian:[C:C] Now I am. Yeah.[XS:giltalk,0][XS:client,1][XS:ph,1][E:11][STOPLIP:]`

O jogo exibe qualquer texto que não esteja entre `[ ]` (colchetes) e por isso é necessário muito cuidado a traduzir. Também não é possível deixar "comentários" no arquivo script.
Cada um dos colchetes se refere a um elemento do jogo.

Segue uma lista das Sintaxes descobertas e seus significados:
Sintaxe | Resultado no jogo
------------ | -------------
`#` | Utilizado pra representar quebra de linha. O jogo não executa automaticamente, e não inserir um `#` no texto pode resultar na fala saindo da caixa de texto.
`[E:<valor>]`| Indica uma seção. Sempre deve estar em ordem numérica. Somente o conteúdo entre o numero ímpar até o próximo par será exibido/interpretado.
`[STOPLIP:]` | Aparece em todo final de linha. Indica o fim da exibição do texto na caixa, e prepara a próxima.
`[XS: ]` | Nunca aparece sozinho, Esse comando invoca uma subrotina.
`[C:<valor>]` | `C:` é a declaração de Cor, o `<valor>` inserido vai resultar na cor co  seu respectivo Id.
`[XS:mix,<valor>]` | Inicia a subrotina do processo de fazer as bebidas, e o `<valor>` aparece tanto como 1 ou 0 por motivos desconhecidos.
`[XS:ph,<valor>]` | Aparece sempre após um `[XS:mix,]` com o `<valor>` correspondente à bebida a ser feita. Sempre vem seguido de um `[E:<valor>]`.
`[XS:<nome>face,<valor/reação>]` | Exibe a imagem do personagem de nome `<nome>` com o `<valor/expressão>`. 1 representa a posiçãod e "descanso" do personagem.
`[XS:<nome>talk,<valor>]` | Faz com que o personagem `<nome>` com o `<valor/expressão>` ative a subrotina de fala (animação da boca).

