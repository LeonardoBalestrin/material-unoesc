#### Estrutura básica fundamental
a. Sensor -> b. Micro 1 -> c. Gera pacote -> d. Transmite -> e. Micro 2 -> f. interpreta -> g. age 

a. sensor presente na geladeira
b. micro 1 conectado ao sensor
c. Aquisição dos dados do sensor em questão
	e a geração do pacote que será enviado para a rede
d. Transmissão por Wi-Fi 
e. recebimento dos dados pelo micro 2
f. tratamento dos dados pelo micro 2
g. Logica do micro 2

	se recebi pacotes
		escreva em um arquivo
		de um "Oi"(qualquer alerta em uma API web) a cada 5s 
			Se a API Não receber sinal do controlador
				gera erro de "Problema de conexão"
				alerta os estudantes
	não recebi pacotes em 2 segundos 
		gera erro de "Perda de conexão"
		alerta os estudantes com o Problema
	se a temperatura alterou muito por mais de 1m
		  gera erro de "aumento de temperatura constante, amostras em risco"
		  alerta os estudantes com o problema
	se a energia cair
		este sinal vem no pacote
		gera erro de "Energia caiu"
		continua recebendo e escrevendo
		alerta os estudantes com o Problema
	passou (X tempo, necessário para proximo de lotar o armazenamento interno) 
		dispensa o arquivo para um ou mais armazenamentos confiaveis
		SE passou 5s sem conseguir dispensar o arquivo
			Gera erro de comunicação 
			alerta os estudantes
			Continua recebendo e escrevendo
				A cada recebimento apaga o registro mais antigo
				E escreve o recebido


Possibilidades de Micros e informações relevantes
ESP32

	Armazenamento?

ESP8266(apenas ponto de acesso)


PIC

	Armazenamento?

STM32

	Armazenamento?















