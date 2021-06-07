
# Conceitos


## IoT Devices

Um componente físico de hardware com:

- Power Source
- Built-in modem
- Sensors
- Actuators
- Control Logic

## Esquema IoT Device

![alt text](/images/iotdevice.png "IoT Device")


## Funcionalidades dos dispositivos IoT

- Sensing
- Actuating
- Communicating
- Processing

## SenML

- Sensor Markup Language (SenML) é uma solução emergente para representar parâmetros e medições de dispositivos. A SenML está substituindo formatos de dados proprietários e está sendo aceita por cada vez mais fornecedores.

- As representações são definidas em JavaScript Object Notation (JSON), eXtensible Markup Language (XML) e Efficient XML Interchange (EXI), que compartilha o modelo de dados SenML comum. Um simples sensor, como um sensor de temperatura, pode usar este tipo de mídia em protocolos como HTTP ou CoAP para transportar as medições do sensor ou a ser configurado.

## TinyML 

- Uma vertente emergente dentro da inteligência artificial. Neste modelo, algoritmos de Machine Learning são implementados em sistemas de baixo consumo de energia, como sensores ou microcontroladores, para executar tarefas automatizadas

## Esquema IoT Device funcionalidades

![alt text](/images/iotdevice_func.png "IoT Device funcionalidades")

## Tags RFID (Radio Frequency IDentification)

- Associa objetos físicos com entidades virtuais
- Provê um ID Único (UID)
- UID lido com rede NFC (Near Field Communications)
- RFID ativo vs. passivo

## Microcontrolador (MCU)

- Processador Miniaturizado
- CPU, RAM, ROM, etc...
- Mini Computador ou SoC(System on Chip)

## Firmware

- Código guardado em memória não volátil
- Contém a lógica do dispositivo
- Pode ou não ser atualizado em manutenções de rotina

## Fonte de energia

- Baterias recarregáveis ou substituíveis 
- Baterias restringem o uso de recursos do dispositivo
- Dispositivos IoT podem ter fonte externa de energia
- O nível de bateria deve ser transmitido como parte de status do dispositivo

## Dados em IoT (IoT Data)

- Telemetry Data (Dados de sensores + Metadata (contexto))
- Command Data (Dispositivos IoT podem enviar, receber e reagir a comandos)

0bs.: Outros dados, como informações sobre o status do dispositivo, podem ser enviados no metadata ou em mensagens dedicadas.

## Control Logic

- Responsável por enviar comandos
	- Parar de reiniciar a coleta de dados de telemetria
	- Interagir com um hardware, como termostato ou módulo GPS
	- Mudar a frequência de transmissão dos dados de telemetria

- A lógica de controle pode estar:
	- Em um dispositivo IoT
	- Algum ambiente intermediário
	- Dentro da lógica do cliente

## Client Logic

- Recipiente final dos dados de telemetria
- A lógica do cliente pode ser:
	- Uma solução comericial automatizada que recebe os dados
	- Um sistema que usa Big Data, Machine Learning ou Inteligência Artificial para analisar os dados
	- Um  app no smartphone do cliente

Obs.: Quando a aplicação do cliente pode enviar comandos, a lógica do cliente engloba ou coexiste com a lógica de controle (Control Logic).

## Modem

- Modulador-Demodulador
- Sinal digital compatível com o meio de transmissão 
- Modem Multibanda (Opera em várias frequências)
- Modem SDR (Software-Defined Radio)

## Plataforma IoT

- Ambiente central na solução IoT
- Oferece vários recursos e funções
- Auxilia na execução e administração da solução IoT

## Sistema Publish-Subscribe

- Sistema de notificação de eventos
- Divulgador (publisher) e assinantes (subscriber)
- Podem haver várias notificações (tópicos)
- Camada Intemediária
- Geralmente parte da plataforma IoT

- Promove desacoplamento
	- Space decoupling: Sem troca de identidade (Ex.:IP).
	- Time decoupling: Descarta simultaneidade (Ex.: Buffer).
	- Device decoupling: Adicionar ou remover um dispositivo não prejudica o Subscriber.

## Gateways

- Agrega os nós da rede
- Coordena a conectividade entre dispositivos e a rede
- Pode fornecer localização, assistência remota, transição de protocolo, etc.
- Hardware Convercional e Torres de telecomunicação.

## Radio Trasport

- Provê a conectividade sem fio da rede IoT
- Largura de banda difere entre dispositivos

## Network 

- Grupo de nós interconectados
- Duas categorias primárias em IoT(LAN e WAN)
- Pode conter:
	- End devices;
	- Roteadores;
	- Pontes;
	- SW;
	- Hubs e/ou Gateways.

## Network Server

- Hospeda recursos IoT compartilhados
- Servidores podem se conectar para formar uma WAN
- BSF (Bootstrap Server Function)
	- Conecta dispositivos antes desconhecidos
	- Fornece configurações para compatibilidade


## Entendendo a Arquitetura IoT

Camadas da Arquitetura IoT

- A complexidade de projetos IoT faz necessário sua divisão em camadas para melhor organização.
- Telemetry Device Layer: Camada dos dispositivos de coleta de dados.
- Intermediary Gateway Layer: Camada de Gateways e Estação Base
- Intermediary Platform Layer: Camada da plataforma IoT.
	- Pode ser hospedado por um ou um conjunto de servidores de rede subjacentes.
- Client Application Layer: Camada da aplicação (O aplicativo, o Big Data, etc.)

## Exemplo Arquitetura IoT

![alt text](/images/exemploiotplataform.png "Arquitetura IoT")



## Modelagem de Ação IoT (IoT Action Modeling)

- Modelagem de ação num dispositivo. Exemplo: Ligar e desligar a luz de uma casa usando um celular.
	- Para cada modelagem de ação, "criam-se" vocabulários para caracterizar cada parte.


## Esquema Modelagem Ação IoT

![alt text](/images/modelagemAcaoIoT.png "Modelagem Ação IoT")

Obs.: A criação desses termos ajuda a organizar as ideias do seu projeto.

## Edge Computing

- A camada lógica pode ser colocada no gateway, aproximando a computação ao End Node.

- Permite que se distribua o processamento dos dados.

- Com a camada lógica no gateway, eles podem fazer previsões sobre o dispositivo usando Machine Learning.

## Esquema Edge Computing

![alt text](/images/edge1.png "Edge Computing")


## Considerações Comuns em IoT

- Scalability Requirements
	- Um projeto IoT pode crescer e isso pode afetar o sistema desenvolvido anteriomente.
		- Aumento na complexidade
		- Degradação de performance

- Identify Correct Telemetry Abstraction
	- Em todo projeto IoT, é importante saber como dados são obtidos.
	- Além disso, a acurácia do sensor deve se encaixar nos requisitos do seu projeto.

- Define Resource Constraints
	- Reconheça todas as limitações possíveis do seu projeto para saber como lidar com elas.
	- Exemplos:
		- Consumo de Energia
		- Tamando do payload
		- Capacidade do Sistema (Números de dispositivos)
		- Taxas de Transmissão
		- Limitações da Banda de Frequência

- Tailor Connectivity
	- Escolha com cautela a conectividade que irá usar no projeto
	- As características da comunicação devem estar de acordo com as llimitações e necessidades do projeto.

## IoT Messaging 


- Troca de dados depende essencialmente em protocolos de transportes. Afinal, tudo está na rede (Internet).

	- **HTTP** - significa HyperText Transfer Protocol, que é um conjunto de regras que os servidores seguem quando se comunicam na Internet.
	- Representational State Transfer **(REST)** define um conjunto de restrições serem usadas para a criação de web services (serviços Web).
	- CoAP e MQTT (protocolos voltados para aplicações M2M). 			 	

## IoT Messaging - HTTP (brief)

- Quando um usuário abre um navegador, ele já está fazendo uso de um HTTP.

- O protocolo HTTP faz a comunicação entre o cliente e o servidor através de mensagens. O cliente envia uma mensagem de requisição de um recurso e o servidor envia uma mensagem de resposta ao cliente com a solicitação.

## Esquema protocolo HTTP 

![alt text](/images/HTTPmecanismo.png "protocolo HTTP")

## Esquema Mensagem HTTP 

![alt text](/images/HTTP_Request.png "HTTP Request")

## Esquema Comandos 

![alt text](/images/Comandos+do+HTTP+Método+Descrição+GET1.jpg "Comandos do HTTP")

## Esquema HTTP Status Code

![alt text](/images/http_status_code.png "HTTP Status Code")

## IoT Messaging - REST (brief)

- "Transferência de Estado Representacional" (Representational State Transfer)

- Estilo arquitetural da Internet

- Definido em uma série de propriedade e restrições.

## Propriedade do padrão REST 

- Propriedade que se tornam objetivos
	- Performance
	- Scalability
	- Reliability
	- Modifiability
	- Simplicity
	- Visibility

## Esquema REST API Architecture

![alt text](/images/rest-api.jpg "REST API Architecture")

## REST - Performance

- Performance
	- Uso de memória cache para manter os dados perto de onde estão sendo processados.
	- Mantendo cada iteração com os serviços (GET, PUT ...) simples e enxuto (resposta request/response).
		- Melhorar throughput
		- Banda
		- Latência
		- Eficiência

- Device Shadow
	- Dispositivo de sombra
	- Trabalha como um nó intermediário. Paralelo com a cache.
			- Ajudando na regulação de tráfego entre dispositivo e controladores.
	- JSON usado para guardar e restaurar estados de um dispositivo

## Esquema Device Shadow

![alt text](/images/deviceshadowREst_perfor.png "Device Shadow - Dispositivo de sombra")

## REST - Scalability

- Scalability

	- Suportar desde um número baixo até um alto número de instâncias ou interações.
	- Scaling Up: Aumenta a capacidade de serviços e outros componentes da rede.
	- Scaling Out: Distribui a carga para outras fontes.
	- Smoothing Out: Elimina interações em períodos de pico ou fora do pico.
	- Decoupling: Separa o consumo de recursos finitos (ex: memória) de consumidores simultâneos.
	- O dispositivo sozinho não garante escalabilidade.
	- A infraestrutura de redes que tem essa responsabilidade.

## REST - Modifiability

- Modifiability
	- Facilidade em modificar a arquitetura. Variações:
		- Evolvability: Mudar uma implementação sem prejudicar outras.
		- Extensibility: Adicionar funcionalidade enquanto os serviços estão acontecendo.
		- Customizability: Capacidade de mudar, temporariamente, alguns serviços.
		- Configurability: Capacidade de mudar os serviços permanentemente.
		- Reusability: Adicionar novas soluções que reusam a arquitetura em questão, sem modificações.
	- Dispositivo IoT podem suportar essas variações de modificabilidade. Dependendo de como a lógica está distribuída e como o hardware funciona.

## REST - Reability/Confiabilidade

- Reability/Confiabilidade
	- Habilidade de continuar funcionando, mesmo que ocorram falhas.
	- Persistências de estados. Cookies e cache.
	- Device Shadow permite que tudo continue operando mesmo que o dispositivo não esteja conectado.
		- Continua enviando o último estado entregue pelo dispositivo.


## REST - Simplicity/Simplicidade e Visibility/Visibilidade

- Simplicity/Simplicidade:
	- Maior contribuição para uma interface uniforme.
- Visibility/Visibilidade:
	- Forma como os dados serão mostrados. Muitos dados a serem mostrados de forma sucinta.
	- Aliás, quais dados podem ser mostrados e para quem.

## IoT Messaging - REST - Constraints

- Constraints: Restrições aplicadas para uma solução REST:
	- Client Server - Cliente-Servidor.
	- Layered System (Sistema em camadas).
	- Stateless + Cache (Sem estado + cache).
	- Code-On-Demand.
	- Uniform Interface.

## REST - Constraints Client Server

- Client Server
	- Separação de cliente e servidor ajuda na independência de ambos.
	- Arquitetura distribuída.
	- Aplicação requisita um dado, dispositivo responde.

![alt text](/images/rest_constrains1.png "REST - Constraints Client Server")

## REST - Constraints Layered Sytem 

- Layered Sytem (Sistema em Camadas)
	- Divisão em camadas ajuda a organizar e manter a independência entre elas.
	- Em IoT, nem sempre essa independência é atingida.

## REST - Constraints Stateless + Cache
- Stateless + Cache
	- Stateless:
		- Cada pedido de um serviço tem que conter todos os dados requisitados da sessão. 
		- Um serviço não deve salvar o estado da sessão.

	- Cache:
		- Guarda dados de estados anteriores permitindo que mensagens guardadas possam ser usadas por outras camadas.

![alt text](/images/stateless_cache.png "REST - Constraints Stateless + Cache")

## REST - Constraints Code-On-Demand

- Code-On-Demand
	- A restrição do Code-On-Demand destina-se principalmente a permirtir que a lógica entre os computadores do serviço seja atualizada pelo serviço.
	- Não é usado muito em IoT.

## REST - Constraints Uniform Interface

- Uniform Interface
	- Estabelece uma padronização entre os serviços de iterações.
	- Implementação de uma interface uniforme para uso.

## Constrained Application Protocol (CoAp)

- Utilizado como um dos principais protocolos de transferência **(para M2M)** juntamente com o MQTT.
- Protocolo da camada de aplicação que não necessariamente mantém canais seguros para transmissão.
- CoAp mapeia o HTTP e estabelece um servidor autossuficiente em cada **device**. Ideal para nós e redes restritas.
- Eficiente protocolo RESTful.
- Usando um CoAp, o dispositivo pode receber um HTTP GET da rede e responder com um HTTP POST.
- Usado especificamente para IoT/M2M.
- CoAp usa UDP ao invés de TCP. Isso alivia o dispositivo de ficar administrando conexões (não necessita estabelecer conexão prévia).
- Estabelece três níveis de QoS (confirmável, não confirmável).
- Usa formatos binários para transportar a mensagem (GET, PUT e POST).

## HTTP com CoAp

- CoAp e MQTT são HTTP-based.
	- Mas são modificados.
- Não usam HTTP puro, uma vez que não usam texto puro.
- Uso de representações binárias.
- Fatos importantes e necessários para comunicação.
	- Resource Identifies: Padronização de sintaxe (de mensagem) para identificação da fonte.
	- Media Types: Tipo de mensagem a ser transmitida. O CoAp reduz tudo a números para reduzir os bytes.
	- HTTP:
		- Métodos: Tipo de comunicação GET/POST/PUT/DELETE.
		- Código de Resposta.
		- Cabeçalho: Usado para definir metadados.







	


	







