Utilizado para trabalhar com sinais não periódicos

Necessita da Série de Fourier Exponencial:
$$
f(t) = \sum^\infty_{n=-\infty}D_ne^{jn*\omega0*t}
$$
e para burlar o sinal não periódico, foi criada a transformada continua de fourier


E para outros casos onde a equação é impreciso como sinal de voz criou-se a [[Transformada discreta de Fourier]] :

$$
X(\omega) = \sum^{N-1}_{n=0}x_n  e^{-{j2\pi kn}/N}
$$
onde N é o numero de amostras obtidas, k é o índice(pensando em uma matriz/vetor) das amostras armazenadas, e n é o valor da amostra em si
e para garantir o processamento computacional de acompanhar as amostras, é possivel utilizar a FFT(em [[Transformada discreta de Fourier]])