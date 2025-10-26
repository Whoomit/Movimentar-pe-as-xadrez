# Movimentar-peças-xadrez


Desafio: Movimentação de Peças de Xadrez 

🎯 O Que Vamos Fazer?

Vamos criar um programa que verifica se um movimento de xadrez é válido para a peça que está se movendo.

O foco é na lógica de movimento de cada peça. Não precisamos nos preocupar com regras complexas (como "cheque" ou "roque") – só se a peça está se movendo corretamente (ex: o Bispo só se move na diagonal).

🚀 O Desafio Principal

Você deve criar uma função principal chamada checar_movimento.

Essa função deve fazer três coisas:

Receber o estado atual do tabuleiro.

Receber a casa de onde a peça sai (ex: "e2").

Receber a casa para onde a peça vai (ex: "e4").

Retornar True se o movimento for permitido, ou False se for proibido.

Função Esperada (Exemplo em Python):

📋 Regras do Jogo

Para simplificar, vamos usar uma matriz (lista de listas) 8x8 para representar o tabuleiro.

1. Representação
   
Peças: Usaremos uma letra para cada peça.

Brancas (Maiúsculas): P (Peão), T (Torre), C (Cavalo), B (Bispo), D (Dama), R (Rei).

Pretas (Minúsculas): p, t, c, b, d, r.

Casa Vazia: Usaremos o ponto .

Coordenadas: As casas serão dadas na notação de xadrez (ex: "a1", "h8"). A primeira coisa que você precisa fazer é traduzir "a1" para as coordenadas da matriz (ex: [7][0]).

2. Tabuleiro Inicial
   
Use esta matriz para começar seus testes:

4. Regras de Validação Essenciais
   
Sua função deve verificar, em ordem:

Peça no Local: Tem alguma peça na casa_origem? (Não se pode mover o vazio).

Captura Amiga: Se a casa_destino tiver uma peça, essa peça é da mesma cor que a peça que está se movendo?

SIM: Movimento INVÁLIDO (Não se pode capturar uma peça sua).

NÃO: Movimento VÁLIDO se a lógica da peça permitir.

Lógica da Peça: O movimento de origem para destino segue a regra da peça?

💡 Dicas para Implementar

Organize o Código: Crie funções pequenas para cada tarefa!

traduzir_coordenadas(notacao_algebrica): Transforma "a1" em (7, 0).

obter_peca(tabuleiro, coordenadas): Retorna a letra da peça.

e_bloqueado(tabuleiro, origem, destino): Checa se há peças no caminho (para Torre, Bispo e Dama).

Separe a Lógica: Crie uma função para cada tipo de peça, ex: e_movimento_de_bispo_valido().

✅ Exemplos de Teste

Teste estas situações usando o tabuleiro_inicial:

🎁 Desafio Extra (Bônus)

Se terminar o desafio principal:

Gerador de Coordenadas: Faça a função que traduz as notações de xadrez (ex: "a1") em índices de matriz (ex: [7][0]).

Lista de Movimentos: Crie uma função que recebe o tabuleiro e uma casa de origem, e retorna uma lista de TODAS as casas para onde aquela peça pode se mover legalmente.
