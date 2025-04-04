
## Conceitos:
#alising 
- um fenômeno no qual um sinal de frequência mais alta passa a se tornar mais baixa após a amostragem sem considerar o filtro Fs adequado
- imaginando a frequência real como Fsinal, n representa quantas vezes a Fs deve ser multiplicada para chegar até a faixa da frequência do sinal e Fs como frequência do sistema, um exemplo onde a Fsinal = 2050 e Fs = 1000, n = 2
$$
Fapresentada= Fsinal - n*Fs
$$

FFT

a transformada discreta de Fourier RÁPIDA, é feita utilizando dividindo a matriz original ao meio diversas vezes, fazendo o numero de operações matemáticas diminuir drasticamente.
está divisão é feita observando a simetria da matriz original separando as simetrias pares das impares.
