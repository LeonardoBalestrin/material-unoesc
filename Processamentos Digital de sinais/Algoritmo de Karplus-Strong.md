### 1º Simplificação do diagrama
[[Karplus-Strong.excalidraw|Esquema visivel]] 

#### construindo equação
$$
y[n] = x[n]+\alpha y[n-M] 
$$
#### codigo matlab exemplo
```
clear
close
clc

Fs = 48e3; %Frequencia de amostragem
f= 440 ;% frequencia desejada em Hz
M = round(Fs/f); % amostras
tempo = 2; %Tempo duracao nota
n_total = tempo*Fs;
n = 1:1:M;
x= cos(2*pi*100*n/Fs); % no x eu posso manipular o timbre para uma nota
x = sawtooth(n)
alpha = 0.9; %determina a atenuação da nota

for i = 1:n_total
	if i<=M
		y(i) = x(i);
	else
		y(i) = alpha*y(i-M);
	end
end

stem(y)
soundsc(y,Fs)
```
