# TRADUÇÃO DOS SCRIPTS
O jogo trabalha com os roteiros de cada capítulo e personagem, como um teatro. Esses roteiros estavam disponíveis na pasta ../scripts/eng/ o quê facilitou muito bem.

A estrutura básica de um fragmento de texto do jogador é:

`[XS:jilltalk,1][C:13]Jill:[C:C] G'night.[STOPLIP:]`

Outro exemplo é um fragmento de texto de NPC:

`[XS:gilface,][XS:giltalk,1][C:19]Gillian:[C:C] Now I am. Yeah.[XS:giltalk,0][XS:client,1][XS:ph,1][E:11][STOPLIP:]`

O jogo exibe qualquer texto que não esteja entre `[ ]` (colchetes) e por isso é necessário muito cuidado a traduzir. Também não é possível deixar "comentários" no arquivo.
