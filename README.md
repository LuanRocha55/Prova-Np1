O sistema inicia criando uma estrutura de dados fundamental: a matriz reserva.
Essa matriz bidimensional representa a planta do avião, onde cada posição corresponde a um assento.
Inicialmente, todos os assentos são marcados como livres, indicando que estão disponíveis para reserva.
Além disso, são definidas constantes para determinar o número de linhas e colunas da matriz, que representam o tamanho da aeronave.

A função exibirPlanta tem como objetivo apresentar ao usuário a disposição atual dos assentos.
Ela percorre a matriz reserva, linha por linha e coluna por coluna, e exibe na tela um diagrama simplificado do avião.
Cada posição da matriz é representada por um caractere: um espaço em branco indica um assento livre, enquanto a letra 'x' indica um assento ocupado.

A função reservarAssento permite que o usuário escolha um assento específico.
Ao receber a escolha do usuário, a função verifica se o assento selecionado está disponível, ou seja, se ele ainda não foi reservado.
Caso esteja livre, o assento é marcado como ocupado na matriz.
Além disso, a função implementa uma lógica básica para verificar a compatibilidade do assento com o tipo de passagem escolhido pelo usuário (econômica ou executiva).

O loop principal do programa permite que o usuário realize múltiplas reservas de forma consecutiva.
A cada iteração do loop, a função exibirPlanta é chamada para mostrar a planta atualizada do avião, e a função reservarAssento é chamada para permitir que o usuário escolha um novo assento.
O loop continua até que o usuário decida encerrar o programa.
