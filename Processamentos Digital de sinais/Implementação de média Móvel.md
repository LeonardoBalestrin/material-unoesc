#### Codigo matlab
```
%implementacao media movel

clear

close

clc

x = [1 2 3 4 5 6 7 8 9 1 2 3 4 5 6];

n_total = length(x);

janela = 3;

y = zeros(1,n_total);

%for n = janela:(n_total-janela-1)

%y(n) = sum(x((n - janela + 1):n)) / janela;

%y(n) = mean (x(n-janela+1:n));

%objetivo é fazer os valores iniciais não zerarem, tentar resolver

%end

for n = 1:n_total

if n<janela

y(n) = sum(x(1:n))/janela;

else

y(n) = mean (x(n-janela+1:n));

end

end

```
