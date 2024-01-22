# Como a Internet funciona? / How does the Internet work?


## Introdução à Internet / Introduction to the Internet

**PT-BR**  
Antes de aprendermos o que é a Internet, precisamos entender o que é uma Rede. Uma rede é um grupo de computadores ou outros dispositivos que estão conectados entre si. Por exemplo, você em sua casa pode ter uma rede de computadores e dispositivos. Seu amigo que mora ao lado pode ter uma rede semelhante de dispositivos. O vizinho deles pode ter uma rede semelhante de dispositivos. Todas essas redes, quando conectadas, formam a internet.

***

**EN-US**  
Before we learn what the Internet is, we need to understand what a Network is. A network is a group of computers or other devices which are connected to eachother. For example, you at your home might have a network of computers and devices. Your friend living next door might have a similar network of devices. Their neighbor might have a similar network of devices. All these networks when connected together form the internet.


## Como a Internet funciona: Uma visão geral / How the Internet Works: An Overview

**PT-BR**  
Em alto nível, a internet funciona conectando dispositivos e sistemas de computador usando um conjunto de protocolos padronizados. Esses protocolos definem como as informações são trocadas entre dispositivos e garantem que os dados sejam transmitidos de maneira confiável e segura.

O núcleo da internet é uma rede global de roteadores interconectados, que são responsáveis ​​por direcionar o tráfego entre diferentes dispositivos e sistemas. Quando você envia dados pela internet, eles são divididos em pequenos pacotes que são enviados do seu dispositivo para um roteador. O roteador examina o pacote e o encaminha para o próximo roteador no caminho em direção ao seu destino. Esse processo continua até que o pacote chegue ao seu destino final.

Para assegurar que os pacotes são enviados e recebidos corretamente, a internet usa uma variedade de protocolos, incluindo o _Internet Protocol_ (IP) e o _Transmission Control Protocol_ (TCP). O IP é responsável por rotear os pacotes para seu destino correto, enquanto o TCP garante que os pacotes sejam transmitidos de maneira confiável e na ordem correta.

Além desses protocolos principais, existem uma ampla gama de outras tecnologias e protocolos que são usados ​​para permitir a comunicação e a troca de dados pela internet, incluindo o _Domain Name System_ (DNS), o _Hypertext Transfer Protocol_ (HTTP) e o _Secure Sockets Layer_ / _Transport Layer Security_ (SSL / TLS).

***

**EN-US**  
At a high level, the internet works by connecting devices and computer systems together using a set of standardized protocols. These protocols define how information is exchanged between devices and ensure that data is transmitted reliably and securely.

The core of the internet is a global network of interconnected routers, which are responsible for directing traffic between different devices and systems. When you send data over the internet, it is broken up into small packets that are sent from your device to a router. The router examines the packet and forwards it to the next router in the path towards its destination. This process continues until the packet reaches its final destination.

To ensure that packets are sent and received correctly, the internet uses a variety of protocols, including the Internet Protocol (IP) and the Transmission Control Protocol (TCP). IP is responsible for routing packets to their correct destination, while TCP ensures that packets are transmitted reliably and in the correct order.

In addition to these core protocols, there are a wide range of other technologies and protocols that are used to enable communication and data exchange over the internet, including the Domain Name System (DNS), the Hypertext Transfer Protocol (HTTP), and the Secure Sockets Layer/Transport Layer Security (SSL/TLS) protocol.


## Conceitos básicos e terminologia / Basic Concepts and Terminology

**PT-BR**  
Para entender a internet, é importante estar familiarizado com alguns conceitos e terminologia básicos. Aqui estão alguns termos e conceitos-chave para se ter em mente:
- **Pacote**: Uma pequena unidade de dados que é transmitida pela internet.
    - Um pacote é a unidade básica de informação transmitida pela internet. Dividir as informações em pequenas partes permite que a capacidade da rede seja usada de maneira mais eficiente.
    - Um pacote tem duas partes. O cabeçalho contém informações que ajudam o pacote a chegar ao seu destino, incluindo o comprimento do pacote, sua origem e destino e um valor _checksum_ que ajuda o destinatário a detectar se um pacote foi danificado durante a transmissão. Após o cabeçalho, vem os dados reais. Um pacote pode conter até 64 kilobytes de dados, o que equivale a aproximadamente 20 páginas de texto simples.
    - Se os roteadores da Internet experimentarem congestionamento ou outros problemas técnicos, eles podem lidar com isso simplesmente descartando pacotes. É responsabilidade do computador de envio detectar que um pacote não chegou ao seu destino e enviar outra cópia. Essa abordagem pode parecer contra-intuitiva, mas simplifica a infraestrutura básica da Internet, levando a um desempenho mais alto a um custo menor.
- **Roteador**: Um dispositivo que direciona pacotes de dados entre diferentes redes.
- **Endereço IP**: Um identificador único atribuído a cada dispositivo em uma rede, usado para rotear dados para o destino correto.
- **Nome de domínio**: Um nome legível por humanos que é usado para identificar um site, como google.com.
- **DNS**: O _Domain Name System_ é responsável por traduzir nomes de domínio em endereços IP.
- **HTTP**: O _Hypertext Transfer Protocol_ é usado para transferir dados entre um cliente (como um navegador da web) e um servidor (como um site).
- **HTTPS**: Uma versão criptografada do HTTP que é usada para fornecer comunicação segura entre um cliente e um servidor.
- **SSL/TLS**: Os protocolos _Secure Sockets Layer_ e _Transport Layer Security_ são usados ​​para fornecer comunicação segura pela Internet.

***

**EN-US**  
To understand the internet, it’s important to be familiar with some basic concepts and terminology. Here are some key terms and concepts to be aware of:

- **Packet**: A small unit of data that is transmitted over the internet.
    - A packet is the basic unit of information transmitted over the internet. Splitting information up into small pieces allows the network’s capacity to be used more efficiently.
    - A packet has two parts. The header contains information that helps the packet get to its destination, including the length of the packet, its source and destination, and a checksum value that helps the recipient detect if a packet was damaged in transit. After the header comes the actual data. A packet can contain up to 64 kilobytes of data, which is roughly 20 pages of plain text.
    - If internet routers experience congestion or other technical problems, they are allowed to deal with it by simply discarding packets. It’s the sending computer’s responsibility to detect that a packet didn’t reach its destination and send another copy. This approach might seem counterintuitive, but it simplifies the internet’s core infrastructure, leading to higher performance at lower cost.
- **Router**: A device that directs packets of data between different networks.
- **IP Address**: A unique identifier assigned to each device on a network, used to route data to the correct destination.
- **Domain Name**: A human-readable name that is used to identify a website, such as google.com.
- **DNS**: The Domain Name System is responsible for translating domain names into IP addresses.
- **HTTP**: The Hypertext Transfer Protocol is used to transfer data between a client (such as a web browser) and a server (such as a website).
- **HTTPS**: An encrypted version of HTTP that is used to provide secure communication between a client and server.
- **SSL/TLS**: The Secure Sockets Layer and Transport Layer Security protocols are used to provide secure communication over the internet.

## O papel dos protocolos na Internet / The Role of Protocols in Internet

**PT-BR**  
Um protocolo é um conjunto de regras e padrões que definem como as informações são trocadas entre dispositivos e sistemas.

Existem muitos protocolos diferentes usados ​​na comunicação pela Internet, incluindo o _Internet Protocol_ (IP), o _Transmission Control Protocol_ (TCP), o _User Datagram Protocol_ (UDP), o _Domain Name System_ (DNS) e muitos outros. O IP é responsável por rotear pacotes de dados para seu destino correto, enquanto o TCP e o UDP garantem que os pacotes sejam transmitidos de maneira confiável e eficiente. O DNS é usado para traduzir nomes de domínio em endereços IP e o HTTP é usado para transferir dados entre clientes e servidores.

Então, seu computador está conectado à Internet e tem um endereço único. Como ele 'conversa' com outros computadores conectados à Internet? Um exemplo: Digamos que seu endereço IP seja 1.2.3.4 e você deseja enviar uma mensagem para o computador 5.6.7.8. A mensagem que você deseja enviar é "Olá computador 5.6.7.8!". A mensagem deve ser traduzida de texto alfabético em sinais eletrônicos, transmitida pela Internet e depois traduzida de volta em texto alfabético. Como isso é realizado? Através do uso de uma pilha de protocolos. Todo computador precisa desta pilha para se comunicar na Internet, que geralmente está embutida no sistema operacional do computador (ou seja, Windows, Unix, etc.). A pilha de protocolos usada na Internet é referida como pilha de protocolos TCP/IP por causa dos dois principais protocolos de comunicação usados. A pilha TCP/IP se parece com isso:
- **Application Protocols Layer**: Protocolos específicos para aplicativos como WWW, e-mail, FTP, etc.
- **Transmission Control Protocol Layer (TCP)**: Direciona pacotes para um aplicativo específico em um computador usando um número de porta.
- **Internet Protocol Layer (IP)**: Direciona pacotes para um computador específico usando um endereço IP.
- **Hardware Layer**: Converte dados de pacotes binários em sinais de rede e vice-versa (por exemplo, placa de rede ethernet, modem para linhas telefônicas, etc.).

1. A mensagem começaria no topo da pilha de protocolos em seu computador e seguiria seu caminho para baixo.
2. Se a mensagem a ser enviada for longa, cada camada da pilha que a mensagem passar poderá dividi-la em pedaços menores de dados (Pacotes, conforme descrito anteriormente).
3. Os pacotes passariam pela _Application Protocols Layer_ e continuariam para a camada TCP. Cada pacote recebe um número de porta. Precisamos saber qual programa no computador de destino precisa receber a mensagem porque ele estará ouvindo em uma porta específica.
4. Depois de passar pela camada TCP, os pacotes seguem para a camada IP. É aqui que cada pacote recebe seu endereço de destino, neste caso, 5.6.7.8.
5. Agora que nossos pacotes de mensagem têm um número de porta e um endereço IP, eles estão prontos para serem enviados pela Internet. A camada de hardware cuida de transformar nossos pacotes contendo o texto alfabético de nossa mensagem em sinal eletrônico.
6. O roteador do ISP (Provedor de Serviços de Internet) examina o endereço de destino em cada pacote e determina para onde enviá-lo. Muitas vezes, a próxima parada do pacote é outro roteador.
7. Eventualmente, os pacotes chegam ao computador 5.6.7.8. Aqui, os pacotes começam na parte inferior da pilha TCP/IP do computador de destino e vão subindo.
8. À medida que os pacotes sobem pela pilha, todos os dados de roteamento que a pilha do computador de envio adicionou (como endereço IP e número de porta) são removidos dos pacotes.
9. Quando os dados atingem o topo da pilha, os pacotes foram reagrupados em sua forma original, "Olá computador 5.6.7.8!".

***

**EN-US**  
A protocol is a set of rules and standards that define how information is exchanged between devices and systems. 

There are many different protocols used in internet communication, including the Internet Protocol (IP), the Transmission Control Protocol (TCP), the User Datagram Protocol (UDP), the Domain Name System (DNS), and many others. IP is responsible for routing packets of data to their correct destination, while TCP and UDP ensure that packets are transmitted reliably and efficiently. DNS is used to translate domain names into IP addresses, and HTTP is used to transfer data between clients and servers.

So your computer is connected to the Internet and has a unique address. How does it 'talk' to other computers connected to the Internet? An example: Let's say your IP address is 1.2.3.4 and you want to send a message to the computer 5.6.7.8. The message you want to send is "Hello computer 5.6.7.8!". The message must be translated from alphabetic text into electronic signals, transmitted over the Internet, then translated back into alphabetic text. How is this accomplished? Through the use of a protocol stack. Every computer needs one to communicate on the Internet and it is usually built into the computer's operating system (i.e. Windows, Unix, etc.). The protocol stack used on the Internet is refered to as the TCP/IP protocol stack because of the two major communication protocols used. The TCP/IP stack looks like this:

- **Application Protocols Layer**: Protocols specific to applications such as WWW, e-mail, FTP, etc.
- **Transmission Control Protocol Layer (TCP)**: Directs packets to a specific application on a computer using a port number.
- **Internet Protocol Layer (IP)**: Directs packets to a specific computer using an IP address.
- **Hardware Layer**: Converts binary packet data to network signals and back.
(E.g. ethernet network card, modem for phone lines, etc.)

1. The message would start at the top of the protocol stack on your computer and work it's way downward.
2. If the message to be sent is long, each stack layer that the message passes through may break the message up into smaller chunks of data (Packets, as described previously).
3. The packets would go through the Application Layer and continue to the TCP layer. Each packet is assigned a port number. We need to know which program on the destination computer needs to receive the message because it will be listening on a specific port.
4. After going through the TCP layer, the packets proceed to the IP layer. This is where each packet receives it's destination address, in this case, 5.6.7.8.
5. Now that our message packets have a port number and an IP address, they are ready to be sent over the Internet. The hardware layer takes care of turning our packets containing the alphabetic text of our message into electronic signal.
6. The ISPs router examines the destination address in each packet and determines where to send it. Often, the packet's next stop is another router.
7. Eventually, the packets reach computer 5.6.7.8. Here, the packets start at the bottom of the destination computer's TCP/IP stack and work upwards.
8. As the packets go upwards through the stack, all routing data that the sending computer's stack added (such as IP address and port number) is stripped from the packets.
9. When the data reaches the top of the stack, the packets have been re-assembled into their original form, "Hello computer 5.6.7.8!".

## Entendendo IPs e nomes de domínio / Understanding IPs and Domain names

**PT-BR**  
Um endereço IP é um identificador único, sendo mais conhecido na versão IPv4, que usa um endereço de 32 bits. Um endereço IPv4 tem formato **n.n.n.n** onde n deve ser um número de 0 a 255, atribuído a cada dispositivo em uma rede.

O IP é usado para rotear dados para o destino correto, garantindo que as informações sejam enviadas ao destinatário pretendido. Ao contrário do TCP, o IP é um protocolo não confiável e sem conexão. O IP não se importa se um pacote chega ou não ao seu destino e não sabe sobre conexões e números de porta. O trabalho do IP é enviar e rotear pacotes para outros computadores. Os pacotes IP são entidades independentes e podem chegar fora de ordem ou não chegar. É o trabalho do TCP garantir que os pacotes cheguem e estejam na ordem correta. A única coisa que o IP tem em comum com o TCP é a maneira como ele recebe dados e adiciona suas próprias informações de cabeçalho IP aos dados do TCP.

Se você se conecta à Internet por meio de um Provedor de Serviços de Internet (ISP), geralmente recebe um endereço IP temporário durante a sessão. Se você se conecta à Internet de uma rede local (LAN), seu computador pode ter um endereço IP permanente ou pode obter um temporário de um servidor DHCP (Dynamic Host Configuration Protocol). Em qualquer caso, se você estiver conectado à Internet, seu computador terá um endereço IP exclusivo.

Os nomes de domínio, por outro lado, são nomes legíveis por humanos usados ​​para identificar sites e outros recursos da Internet. Eles geralmente são compostos por duas ou mais partes, separadas por pontos finais. Por exemplo, "[google.com](http://google.com/)" é um nome de domínio. Os nomes de domínio são traduzidos em endereços IP usando o _Domain Name System_ (DNS). Quando você insere um nome de domínio em seu navegador da web, seu computador envia uma consulta DNS para um servidor DNS, que retorna o endereço IP correspondente. Seu computador usa esse endereço IP para se conectar ao site ou outro recurso que você solicitou.

***

**EN-US**  
An IP address is a unique identifier, most commonly known in the IPv4 version, which uses a 32-bit address. An IPv4 address has the format **n.n.n.n** where n must be a number from 0 to 255, assigned to each device on a network.

IP is used to route data to the correct destination, ensuring that information is sent to the intended recipient. Unlike TCP, IP is an unreliable, connectionless protocol. IP doesn’t care if a packet makes it to its destination or not, and it doesn’t know about connections and port numbers. IP’s job is to send and route packets to other computers. IP packets are independent entities and can arrive out of order or not arrive at all. It’s TCP’s job to ensure that packets arrive and are in the correct order. The only thing IP has in common with TCP is the way it receives data and adds its own IP header information to the TCP data.

If you connect to the Internet through an Internet Service Provider (ISP), you are usually assigned a temporary IP address for the duration of your session. If you connect to the Internet from a local area network (LAN) your computer might have a permanent IP address or it might obtain a temporary one from a DHCP (Dynamic Host Configuration Protocol) server. In any case, if you are connected to the Internet, your computer has a unique IP address.

Domain names, on the other hand, are human-readable names used to identify websites and other internet resources. They’re typically composed of two or more parts, separated by periods. For example, “[google.com](http://google.com/)” is a domain name. Domain names are translated into IP addresses using the Domain Name System (DNS). When you enter a domain name into your web browser, your computer sends a DNS query to a DNS server, which returns the corresponding IP address. Your computer uses this IP address to connect to the website or other resource you requested.

## Construindo aplicações com TCP/IP / Building Applications with TCP/IP

**PT-BR**  
Abaixo da camada de aplicação na pilha de protocolos está a camada TCP. Quando os aplicativos abrem uma conexão com outro computador na Internet, as mensagens que enviam (usando um protocolo de camada de aplicativo específico) são passadas pela pilha para a camada TCP. O TCP é responsável por rotear protocolos de aplicativos para o aplicativo correto no computador de destino.

Para isso, são usados ​​números de porta. As portas podem ser consideradas canais separados em cada computador. Por exemplo, você pode navegar na web enquanto lê e-mails. Isso ocorre porque esses dois aplicativos (o navegador da web e o cliente de e-mail) usaram números de porta diferentes. Quando um pacote chega a um computador e sobe pela pilha de protocolos, a camada TCP decide qual aplicativo recebe o pacote com base em um número de porta.

O TCP funciona assim:
- Quando a camada TCP recebe os dados do protocolo da camada de aplicativo acima, ele os segmenta em 'pedaços' gerenciáveis ​​e, em seguida, adiciona um cabeçalho TCP com informações TCP específicas a cada 'pedaço'. As informações contidas no cabeçalho TCP incluem o número da porta do aplicativo para o qual os dados precisam ser enviados.
- Quando a camada TCP recebe um pacote da camada IP abaixo dela, a camada TCP retira os dados do cabeçalho TCP do pacote, faz alguma reconstrução de dados, se necessário, e, em seguida, envia os dados para o aplicativo correto usando o número da porta retirado do cabeçalho TCP.

É assim que o TCP roteia os dados que passam pela pilha de protocolos para o aplicativo correto.

Além disso, o TCP não é um protocolo textual. O TCP é um serviço de fluxo de bytes confiável e orientado à conexão. Orientado à conexão significa que dois aplicativos usando TCP devem primeiro estabelecer uma conexão antes de trocar dados. O TCP é confiável porque, para cada pacote recebido, um reconhecimento é enviado ao remetente para confirmar a entrega. O TCP também inclui um checksum em seu cabeçalho para verificar erros nos dados recebidos.

Ao criar aplicativos com TCP/IP, existem alguns conceitos-chave a serem entendidos:
- **Portas**: Usadas para identificar o aplicativo ou serviço em execução em um dispositivo. Cada aplicativo ou serviço recebe um número de porta exclusivo, permitindo que os dados sejam enviados para o destino correto.
- **Sockets**: Combinação de um endereço IP e um número de porta, representando um ponto de extremidade específico para comunicação. Os soquetes são usados ​​para estabelecer conexões entre dispositivos e transferir dados entre aplicativos.
- **Conexões**: Estabelecidas entre dois soquetes quando dois dispositivos desejam se comunicar entre si. Durante o processo de estabelecimento de conexão, os dispositivos negociam vários parâmetros, como o tamanho máximo do segmento e o tamanho da janela, que determinam como os dados serão transmitidos pela conexão.
- **Transferência de dados**: Uma vez estabelecida a conexão, os dados podem ser transferidos entre os aplicativos em execução em cada dispositivo. Os dados são normalmente transmitidos em segmentos, sendo que cada segmento contém um número de sequência e outros metadados para garantir a entrega confiável.

***

**EN-US**  
Under the application layer in the protocol stack is the TCP layer. When applications open a connection to another computer on the Internet, the messages they send (using a specific application layer protocol) get passed down the stack to the TCP layer. TCP is responsible for routing application protocols to the correct application on the destination computer.

To accomplish this, port numbers are used. Ports can be thought of as separate channels on each computer. For example, you can surf the web while reading e-mail. This is because these two applications (the web browser and the mail client) used different port numbers. When a packet arrives at a computer and makes its way up the protocol stack, the TCP layer decides which application receives the packet based on a port number.

TCP works like this:
- When the TCP layer receives the application layer protocol data from above, it segments it into manageable 'chunks' and then adds a TCP header with specific TCP information to each 'chunk'. The information contained in the TCP header includes the port number of the application the data needs to be sent to.
- When the TCP layer receives a packet from the IP layer below it, the TCP layer strips the TCP header data from the packet, does some data reconstruction if necessary, and then sends the data to the correct application using the port number taken from the TCP header.

This is how TCP routes the data moving through the protocol stack to the correct application. 

Also, TCP is not a textual protocol. TCP is a connection-oriented, reliable, byte stream service. Connection-oriented means that two applications using TCP must first establish a connection before exchanging data. TCP is reliable because for each packet received, an acknowledgement is sent to the sender to confirm the delivery. TCP also includes a checksum in it's header for error-checking the received data.

When building applications with TCP/IP, there are a few key concepts to understand:
- **Ports**: Used to identify the application or service running on a device. Each application or service is assigned a unique port number, allowing data to be sent to the correct destination.
- **Sockets**: Combination of an IP address and a port number, representing a specific endpoint for communication. Sockets are used to establish connections between devices and transfer data between applications.
- **Connections**: Established between two sockets when two devices want to communicate with each other. During the connection establishment process, the devices negotiate various parameters such as the maximum segment size and window size, which determine how data will be transmitted over the connection.
- **Data transfer**: Once a connection is established, data can be transferred between the applications running on each device. Data is typically transmitted in segments, with each segment containing a sequence number and other metadata to ensure reliable delivery.

## Introdução ao HTTP e HTTPS / Introduction to HTTP and HTTPS

**PT-BR**  
HTTP (Hypertext Transfer Protocol) e HTTPS (HTTP Secure) são dois dos protocolos mais usados ​​em aplicativos e serviços baseados na Internet.

O HTTP é o protocolo usado para transferir dados entre um cliente (como um navegador da web) e um servidor (como um site). Quando você visita um site, seu navegador da web envia uma solicitação HTTP ao servidor, solicitando a página da web ou outro recurso que você solicitou. O servidor, em seguida, envia uma resposta HTTP de volta ao cliente, contendo os dados solicitados.

O HTTPS é uma versão mais segura do HTTP, que criptografa os dados transmitidos entre o cliente e o servidor usando criptografia SSL / TLS (Secure Sockets Layer / Transport Layer Security). Isso fornece uma camada adicional de segurança, ajudando a proteger informações confidenciais, como credenciais de login, informações de pagamento e outros dados pessoais.

***

**EN-US**  
HTTP (Hypertext Transfer Protocol) and HTTPS (HTTP Secure) are two of the most used protocols in internet-based applications and services.

HTTP is the protocol used to transfer data between a client (such as a web browser) and a server (such as a website). When you visit a website, your web browser sends an HTTP request to the server, asking for the webpage or other resource you’ve requested. The server then sends an HTTP response back to the client, containing the requested data.

HTTPS is a more secure version of HTTP, which encrypts the data being transmitted between the client and server using SSL/TLS (Secure Sockets Layer/Transport Layer Security) encryption. This provides an additional layer of security, helping to protect sensitive information such as login credentials, payment information, and other personal data.

## Protegendo a comunicação pela Internet com SSL e TLS / Securing Internet Communication with SSL and TLS

**PT-BR**  
Como discutimos anteriormente, o SSL/TLS é um protocolo usado para criptografar dados transmitidos pela Internet. É comumente usado para fornecer conexões seguras para aplicativos como navegadores da web, clientes de e-mail e programas de transferência de arquivos.

Ao usar o SSL/TLS para proteger a comunicação pela Internet, existem alguns conceitos-chave a serem entendidos:
- **Certificados**: Certificados SSL/TLS são usados ​​para estabelecer confiança entre o cliente e o servidor. Eles contêm informações sobre a identidade do servidor e são assinados por uma terceira parte confiável (uma Autoridade Certificadora) para verificar sua autenticidade.
- **Handshake**: Durante o processo de handshake SSL/TLS, o cliente e o servidor trocam informações para negociar o algoritmo de criptografia e outros parâmetros para a conexão segura.
- **Criptografia**: Uma vez estabelecida a conexão segura, os dados são criptografados usando o algoritmo acordado e podem ser transmitidos com segurança entre o cliente e o servidor.

***

**EN-US**  
As we discussed earlier, SSL/TLS is a protocol used to encrypt data being transmitted over the internet. It is commonly used to provide secure connections for applications such as web browsers, email clients, and file transfer programs.
When using SSL/TLS to secure internet communication, there are a few key concepts to understand:
- **Certificates**: SSL/TLS certificates are used to establish trust between the client and server. They contain information about the identity of the server and are signed by a trusted third party (a Certificate Authority) to verify their authenticity.
- **Handshake**: During the SSL/TLS handshake process, the client and server exchange information to negotiate the encryption algorithm and other parameters for the secure connection.
- **Encryption**: Once the secure connection is established, data is encrypted using the agreed-upon algorithm and can be transmitted securely between the client and server.

## O que é IPv6? / What is IPv6?

**PT-BR**  
Como falado anteriormente, a versão mais conhecida do protocolo IP é a IPv4, que usa um endereço de 32 bits. Isso significa que existem 2^32 endereços IPv4 possíveis, o que equivale a aproximadamente 4 bilhões de endereços. Embora isso possa parecer muito, o crescimento da Internet significa que o IPv4 está ficando sem endereços disponíveis. 

Para resolver esse problema, o IPv6 foi desenvolvido, que usa um endereço de 128 bits. Isso significa que existem 2^128 endereços IPv6 possíveis, o que equivale a aproximadamente 340 undecilhões de endereços. O IPv6 também inclui outras melhorias em relação ao IPv4, incluindo suporte a multicast, autoconfiguração e segurança aprimorada.


Um endereço IPv6 contém tantos números quanto letras. Ele é escrito usando oito grupos de números hexadecimais de quatro dígitos separados por dois pontos. Exemplo: `2001:db8:3333:4444:CCCC:DDDD:EEEE:FFFF`

Além de ter mais endereços de IP, o IPv6 também tem um cabeçalho mais simples do que o IPv4. Um cabeçalho de IP é a meta-informação localizada no início de um pacote de IP. O cabeçalho do IPv6 vem com um novo formato projetado para minimizar o seu tamanho, fazendo com que o processamento dos pacotes seja mais eficiente.

Outra diferença entre o IPv4 e o IPv6 é que a versão mais recente elimina a necessidade do _Network Address Translation_ (NAT), restaurando a conectividade de ponta a ponta na camada do IP.

No início, a transição para o IPv6 foi lenta. O trabalho técnico no padrão foi concluído na década de 1990, mas a comunidade da Internet enfrentou um problema: enquanto a maioria das pessoas usava o IPv4, havia pouco incentivo para que alguém mudasse para o IPv6.

Mas, à medida que os endereços IPv4 se tornaram escassos, a adoção do IPv6 acelerou. A fração de usuários que se conectaram ao Google via IPv6 cresceu de 1% no início de 2013 para 6% no meio de 2015.

***

**EN-US**  
As we discussed earlier, the most widely used version of the IP protocol is IPv4, which uses a 32-bit address. This means that there are 2^32 possible IPv4 addresses, which is roughly 4 billion addresses. While this might seem like a lot, the growth of the internet means that IPv4 is running out of available addresses.

To solve this problem, IPv6 was developed, which uses a 128-bit address. This means that there are 2^128 possible IPv6 addresses, which is roughly 340 undecillion addresses. IPv6 also includes other improvements over IPv4, including support for multicast, autoconfiguration, and enhanced security.

An IPv6 address contains as many numbers as letters. It is written using eight groups of four-digit hexadecimal numbers separated by colons. Example: `2001:db8:3333:4444:CCCC:DDDD:EEEE:FFFF`

In addition to having more IP addresses, IPv6 also has a simpler header than IPv4. An IP header is the metadata located at the beginning of an IP packet. The IPv6 header comes with a new format designed to minimize its size, making packet processing more efficient.

Another difference between IPv4 and IPv6 is that the newer version eliminates the need for Network Address Translation (NAT), restoring end-to-end connectivity at the IP layer.

At first, the transition to IPv6 was slow. Technical work on the standard was completed in the 1990s, but the internet community faced a problem: as long as most people were using IPv4, there was little incentive for anyone to switch to IPv6.

But as IPv4 addresses became scarce, IPv6 adoption accelerated. The fraction of users who connected to Google via IPv6 grew from 1 percent at the beginning of 2013 to 6 percent in mid-2015.
