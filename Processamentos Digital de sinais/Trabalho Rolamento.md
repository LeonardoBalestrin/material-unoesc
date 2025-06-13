### Dowload de arquivo 
https://engineering.case.edu/bearingdatacenter/12k-drive-end-bearing-fault-data
baixa um qualquer, deste ou dos 48k
> **o arquivo contém amostras e dados coletados, apenas.**
> Estes arquivos tem variáveis indicadas, como RPM, DE(Driver and accelerometer data), FE(Fan and accelerometer data), e BA(Base and accelerometer data)

### Carregando arquivo e usando
1. load(arquivo) no matlab
2. 

```
%% FIR

clear

close

clc

load('coef.mat');%utilizando filtro especifico

Fs = 12000;

N = 2000;

n = 0:1:N-1;

f = 135;

x = sin(2*pi*f/Fs*n);

tamanho_buffer =length(bm);

buffer = zeros(1,tamanho_buffer);

buffer = [x(1) buffer(2:end)];

for i=1:N

y(i) = sum(bm.*buffer);

buffer = [x(i) buffer(1:end-1)];

end

figure(1)

stem(x)

hold on

stem(y)

%% IIR

clear

close

clc

load('coef.mat');%utilizando filtro especifico

Fs = 12000;

N = 2000;

n = 0:1:N-1;

f = 800;

x = sin(2*pi*f/Fs*n);

tamanho_buffer =length(bm);

bufferOut = zeros(1,tamanho_buffer-1);

bufferIn = zeros(1,tamanho_buffer);

bufferIn = [x(1) bufferIn(2:end)];

an = -1*an;

an = an(2:end);

for i=1:N

bufferIn = [x(i) bufferIn(1:end-1)];

w(i) = sum(bm.*bufferIn);

y(i) = w(i) + sum(an.*bufferOut);

bufferOut = [y(i) bufferOut(1:end-1)];

end

%Gerar grafico da simulação do sistema, entrada e saida depois de filtrado,

%se é esperado que atenue para a frequencia(f), valores devem ser diferentes

%se é para passar, ambos pontos devem ser iguais.

figure(1)

stem(x)

hold on

stem(y)

%20*log10(valor de pico/1)

%validando se o filtro deu certo, rode o comando acima, com o coef.mat que saiu

%do filterDesigner, altere frequencia(f, citada acima) e verifique qual

%interação é esperado que ocorra, para ela, se ela passa, saida = entrada,

%se é cortada, deve ser atenuada e esta conta citada, indica quantos DB

%foram atenuados na medida real do filtro.

%% trabalho rolamentos Criando filtro

clc

close all

clear

load("225.mat");

amostras = X225_DE_time;

RPM = X225RPM;

Fs = 12000;

tempo = length(amostras)/Fs;

%Defeito pego no site, Rolling Element = 4.7135

Defeito = 4.7135;

RPS = RPM/60;

%Frequencia Que deve ser Cortada

FQC = RPS * Defeito
```