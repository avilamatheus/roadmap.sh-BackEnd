# DNS e como funciona? / DNS and how it works?

## O que é DNS? / What is DNS?
**PT-BR**  
O Sistema de Nomes de Domínio (DNS) é a lista telefônica da Internet. Os humanos acessam informações online através de nomes de domínio, como [nytimes.com](http://nytimes.com/) ou [espn.com](http://espn.com/). Os navegadores da Web interagem através de endereços de Protocolo de Internet (IP). O DNS traduz nomes de domínio para endereços IP para que os navegadores possam carregar recursos da Internet.

***

**EN-US**  
The Domain Name System (DNS) is the phonebook of the Internet. Humans access information online through domain names, like [nytimes.com](http://nytimes.com/) or [espn.com](http://espn.com/). Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources.

Each device connected to the Internet has a unique IP address which other machines use to find the device. DNS servers eliminate the need for humans to memorize IP addresses such as 192.168.1.1 (in IPv4), or more complex newer alphanumeric IP addresses such as 2400:cb00:2048:1::c629:d7a2 (in IPv6).

## Como o DNS funciona? / How does DNS work?
**PT-BR**  
O processo de resolução de DNS envolve a conversão de um nome de host (como [www.example.com](http://www.example.com/)) em um endereço IP amigável ao computador (como 192.168.1.1). Um endereço IP é fornecido a cada dispositivo na Internet, e esse endereço é necessário para encontrar o dispositivo de Internet apropriado - como um endereço de rua é usado para encontrar uma casa em particular. Quando um usuário deseja carregar uma página da web, uma tradução deve ocorrer entre o que um usuário digita em seu navegador da web ([example.com](http://example.com/)) e o endereço necessário para localizar a página da web [example.com](http://example.com/).

Para entender o processo por trás da resolução de DNS, é importante aprender sobre os diferentes componentes de hardware que uma consulta DNS deve passar. Para o navegador da web, a pesquisa de DNS ocorre "nos bastidores" e não requer nenhuma interação do computador do usuário, além da solicitação inicial.

***

**EN-US**  
The process of DNS resolution involves converting a hostname (such as [www.example.com](http://www.example.com/)) into a computer-friendly IP address (such as 192.168.1.1). An IP address is given to each device on the Internet, and that address is necessary to find the appropriate Internet device - like a street address is used to find a particular home. When a user wants to load a webpage, a translation must occur between what a user types into their web browser ([example.com](http://example.com/)) and the machine-friendly address necessary to locate the [example.com](http://example.com/) webpage.

In order to understand the process behind the DNS resolution, it’s important to learn about the different hardware components a DNS query must pass between. For the web browser, the DNS lookup occurs "behind the scenes" and requires no interaction from the user’s computer apart from the initial request.

## Servidores DNS envolvidos no carregamento de uma página da web / DNS servers involved in loading a webpage

**PT-BR**  
Existem 4 servidores DNS envolvidos no carregamento de uma página da web:

- **Recursor DNS** - O recursor pode ser considerado como um bibliotecário que é solicitado a encontrar um determinado livro em algum lugar de uma biblioteca. O recursor DNS é um servidor projetado para receber consultas de máquinas clientes por meio de aplicativos como navegadores da web. Normalmente, o recursor é então responsável por fazer solicitações adicionais para atender à consulta DNS do cliente.

- **Servidor de nomes raiz** - O servidor raiz é o primeiro passo na tradução (resolução) de nomes de host legíveis por humanos em endereços IP. Pode ser considerado como um índice em uma biblioteca que aponta para diferentes estantes de livros - normalmente serve como referência a outros locais mais específicos.

- **Servidor de nomes TLD** - O servidor de domínio de nível superior (TLD) pode ser considerado como uma estante específica de livros em uma biblioteca. Este servidor de nomes é o próximo passo na busca por um endereço IP específico e hospeda a última parte de um nome de host (Usando exemplo.com, o servidor TLD é "com").

- **Servidor de nomes autoritativo** - Este último servidor de nomes pode ser considerado como um dicionário em uma estante de livros, no qual um nome específico pode ser traduzido em sua definição. O servidor de nomes autoritativo é a última parada na consulta do servidor de nomes. Se o servidor de nomes autoritativo tiver acesso ao registro solicitado, ele retornará o endereço IP para o nome de host solicitado de volta ao Recursor DNS (o bibliotecário) que fez a solicitação inicial.


***

**EN-US**  
There are 4 DNS servers involved in loading a webpage:

- **DNS recursor** - The recursor can be thought of as a librarian who is asked to go find a particular book somewhere in a library. The DNS recursor is a server designed to receive queries from client machines through applications such as web browsers. Typically the recursor is then responsible for making additional requests in order to satisfy the client’s DNS query.

- **Root nameserver** - The root server is the first step in translating (resolving) human readable host names into IP addresses. It can be thought of like an index in a library that points to different racks of books - typically it serves as a reference to other more specific locations.

- **TLD nameserver** - The top level domain server (TLD) can be thought of as a specific rack of books in a library. This nameserver is the next step in the search for a specific IP address, and it hosts the last portion of a hostname (In example.com, the TLD server is “com”).

- **Authoritative nameserver** - This final nameserver can be thought of as a dictionary on a rack of books, in which a specific name can be translated into its definition. The authoritative nameserver is the last stop in the nameserver query. If the authoritative name server has access to the requested record, it will return the IP address for the requested hostname back to the DNS Recursor (the librarian) that made the initial request.

## Servidor DNS autoritativo vs Resolvedor DNS recursivo / Authoritative DNS server vs recursive DNS resolver

**PT-BR**  
Ambos os conceitos se referem a servidores (grupos de servidores) que são integrantes da infraestrutura DNS, mas cada um desempenha um papel diferente e vive em locais diferentes dentro do pipeline de uma consulta DNS. Uma maneira de pensar na diferença é que o resolvedor recursivo está no início da consulta DNS e o servidor de nomes autoritativo está no final.

***

**EN-US**  
Both concepts refer to servers (groups of servers) that are integral to the DNS infrastructure, but each performs a different role and lives in different locations inside the pipeline of a DNS query. One way to think about the difference is the recursive resolver is at the beginning of the DNS query and the authoritative nameserver is at the end.

### Resolvedor DNS recursivo / Recursive DNS resolver

**PT-BR**  
O resolvedor recursivo é o computador que responde a uma solicitação recursiva de um cliente e leva o tempo para rastrear o registro DNS. Ele faz isso fazendo uma série de solicitações até chegar ao servidor de nomes DNS autoritativo para o registro solicitado (ou expirar ou retornar um erro se nenhum registro for encontrado). Felizmente, os resolvedores DNS recursivos nem sempre precisam fazer várias solicitações para rastrear os registros necessários para responder a um cliente; o cache é um processo de persistência de dados que ajuda a interromper os pedidos necessários, servindo o registro de recurso solicitado mais cedo na pesquisa DNS.

![Sequência de solicitação de registro DNS](https://cf-assets.www.cloudflare.com/slt3lc6tev37/3NOmAzkfPG8FTA8zLc7Li8/8efda230b212c0de2d3bbcb408507b1e/dns_record_request_sequence_recursive_resolver.png)

***

**EN-US**  
The recursive resolver is the computer that responds to a recursive request from a client and takes the time to track down the DNS record. It does this by making a series of requests until it reaches the authoritative DNS nameserver for the requested record (or times out or returns an error if no record is found). Luckily, recursive DNS resolvers do not always need to make multiple requests in order to track down the records needed to respond to a client; caching is a data persistence process that helps short-circuit the necessary requests by serving the requested resource record earlier in the DNS lookup.

![DNS Record Request Sequence](https://cf-assets.www.cloudflare.com/slt3lc6tev37/3NOmAzkfPG8FTA8zLc7Li8/8efda230b212c0de2d3bbcb408507b1e/dns_record_request_sequence_recursive_resolver.png)

### Servidor DNS autoritativo / Authoritative DNS server

**PT-BR**  
Simplificando, um servidor DNS autoritativo é um servidor que realmente possui e é responsável pelos registros de recursos DNS. Este é o servidor na parte inferior da cadeia de pesquisa DNS que responderá com o registro de recursos consultado, permitindo, em última análise, que o navegador da web que faz a solicitação alcance o endereço IP necessário para acessar um site ou outros recursos da web. Um servidor de nomes autoritativo pode atender a consultas de seus próprios dados sem precisar consultar outra fonte, pois é a fonte final da verdade para determinados registros DNS.

![Sequência de solicitação de registro DNS](https://cf-assets.www.cloudflare.com/slt3lc6tev37/6Cxvsc4NOvmU4pPkKbkDmP/a7588a4c8a3c187e9175a40fa1b3d548/dns_record_request_sequence_authoritative_nameserver.png)

Vale ressaltar que, nos casos em que a consulta é para um subdomínio, como foo.example.com ou blog.cloudflare.com, um servidor de nomes adicional será adicionado à sequência após o servidor de nomes autoritativo, que é responsável por armazenar o registro CNAME do subdomínio.

![Sequência de solicitação de registro DNS](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1O1o3jhs0ztWsD00k8RLIJ/f33c1793a7e21cb92678c1f35ef1b245/dns_record_request_sequence_cname_subdomain.png)


***

**EN-US**  
Put simply, an authoritative DNS server is a server that actually holds, and is responsible for, DNS resource records. This is the server at the bottom of the DNS lookup chain that will respond with the queried resource record, ultimately allowing the web browser making the request to reach the IP address needed to access a website or other web resources. An authoritative nameserver can satisfy queries from its own data without needing to query another source, as it is the final source of truth for certain DNS records.

![DNS Record Request Sequence](https://cf-assets.www.cloudflare.com/slt3lc6tev37/6Cxvsc4NOvmU4pPkKbkDmP/a7588a4c8a3c187e9175a40fa1b3d548/dns_record_request_sequence_authoritative_nameserver.png)

It’s worth mentioning that in instances where the query is for a subdomain such as foo.example.com or blog.cloudflare.com, an additional nameserver will be added to the sequence after the authoritative nameserver, which is responsible for storing the subdomain’s CNAME record.

![DNS Record Request Sequence](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1O1o3jhs0ztWsD00k8RLIJ/f33c1793a7e21cb92678c1f35ef1b245/dns_record_request_sequence_cname_subdomain.png)

## Quais são as etapas em uma pesquisa DNS? / What are the steps in a DNS lookup?

**PT-BR**  
1. Um usuário digita ‘example.com’ em um navegador da web e a consulta viaja para a Internet e é recebida por um resolvedor DNS recursivo.

2. O resolvedor, em seguida, consulta um servidor de nomes raiz DNS (.).

3. O servidor raiz responde ao resolvedor com o endereço de um servidor DNS de domínio de nível superior (TLD) (como .com ou .net), que armazena as informações de seus domínios. Ao pesquisar example.com, nossa solicitação é apontada para o TLD .com.

4. O resolvedor, em seguida, faz uma solicitação ao TLD .com.

5. O servidor TLD, em seguida, responde com o endereço IP do servidor de nomes de domínio do domínio example.com.

6. Por fim, o resolvedor recursivo envia uma consulta ao servidor de nomes do domínio.

7. O endereço IP para example.com é então retornado ao resolvedor do servidor de nomes.

8. O resolvedor DNS, em seguida, responde ao navegador da web com o endereço IP do domínio solicitado inicialmente.

Uma vez que as 8 etapas da pesquisa DNS retornaram o endereço IP para example.com, o navegador pode fazer a solicitação da página da web:

9. O navegador faz uma solicitação HTTP para o endereço IP.
10. O servidor nesse IP retorna a página da web a ser renderizada no navegador (etapa 10).

![Pesquisa completa de DNS](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1NzaAqpEFGjqTZPAS02oNv/bf7b3f305d9c35bde5c5b93a519ba6d5/what_is_a_dns_server_dns_lookup.png)

***

**EN-US**  
1. A user types ‘example.com’ into a web browser and the query travels into the Internet and is received by a DNS recursive resolver.

2. The resolver then queries a DNS root nameserver (.).

3. The root server then responds to the resolver with the address of a Top Level Domain (TLD) DNS server (such as .com or .net), which stores the information for its domains. When searching for example.com, our request is pointed toward the .com TLD.

4. The resolver then makes a request to the .com TLD.

5. The TLD server then responds with the IP address of the domain’s nameserver, example.com.

6. Lastly, the recursive resolver sends a query to the domain’s nameserver.

7. The IP address for example.com is then returned to the resolver from the nameserver.

8. The DNS resolver then responds to the web browser with the IP address of the domain requested initially.

Once the 8 steps of the DNS lookup have returned the IP address for example.com, the browser is able to make the request for the web page:

9. The browser makes a HTTP request to the IP address.
10. The server at that IP returns the webpage to be rendered in the browser (step 10).

![Complete DNS Lookup](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1NzaAqpEFGjqTZPAS02oNv/bf7b3f305d9c35bde5c5b93a519ba6d5/what_is_a_dns_server_dns_lookup.png)

## O que é um resolvedor DNS? / What is a DNS resolver?

**PT-BR**  
O resolvedor DNS é a primeira parada na pesquisa DNS e é responsável por lidar com o cliente que fez a solicitação inicial. O resolvedor inicia a sequência de consultas que, em última análise, leva a um URL sendo traduzido no endereço IP necessário.

Nota: Uma pesquisa DNS típica não armazenada em cache envolverá consultas recursivas e iterativas.

É importante diferenciar entre uma consulta DNS recursiva e um resolvedor DNS recursivo. A consulta refere-se à solicitação feita a um resolvedor DNS exigindo a resolução da consulta. Um resolvedor DNS recursivo é o computador que aceita uma consulta recursiva e processa a resposta fazendo as solicitações necessárias.

***

**EN-US**  
The DNS resolver is the first stop in the DNS lookup, and it is responsible for dealing with the client that made the initial request. The resolver starts the sequence of queries that ultimately leads to a URL being translated into the necessary IP address.

Note: A typical uncached DNS lookup will involve both recursive and iterative queries.

It's important to differentiate between a recursive DNS query and a recursive DNS resolver. The query refers to the request made to a DNS resolver requiring the resolution of the query. A DNS recursive resolver is the computer that accepts a recursive query and processes the response by making the necessary requests.

![Recursive DNS Resolver](https://cf-assets.www.cloudflare.com/slt3lc6tev37/rOXBgctX2gaXNDqP5ktek/7086a97e00525159c6bd9318819c2287/dns_recursive_query.png)

## Quais são os tipos de consultas DNS? / What are the types of DNS queries?

**PT-BR**  
Em uma pesquisa DNS típica, três tipos de consultas ocorrem. Ao usar uma combinação dessas consultas, um processo otimizado para a resolução de DNS pode resultar em uma redução da distância percorrida. Em uma situação ideal, os dados do registro em cache estarão disponíveis, permitindo que um servidor de nomes DNS retorne uma consulta não recursiva.

3 tipos de consultas DNS:

1. **Consulta recursiva** - Em uma consulta recursiva, um cliente DNS exige que um servidor DNS (normalmente um resolvedor recursivo DNS) responda ao cliente com o registro de recurso solicitado ou uma mensagem de erro se o resolvedor não conseguir encontrar o registro.

2. **Consulta iterativa** - nessa situação, o cliente DNS permitirá que um servidor DNS retorne a melhor resposta possível. Se o servidor DNS consultado não tiver uma correspondência para o nome da consulta, ele retornará uma referência a um servidor DNS autoritativo para um nível inferior do namespace do domínio. O cliente DNS fará então uma consulta ao endereço de referência. Esse processo continua com servidores DNS adicionais na cadeia de consulta até que ocorra um erro ou tempo limite.

3. **Consulta não recursiva** - normalmente isso ocorrerá quando um cliente resolvedor DNS consulta um servidor DNS para um registro ao qual ele tem acesso, seja porque é autoritativo para o registro ou o registro existe dentro de seu cache. Normalmente, um servidor DNS armazenará em cache registros DNS para evitar consumo de largura de banda adicional e carga em servidores upstream.

***

**EN-US**  
In a typical DNS lookup three types of queries occur. By using a combination of these queries, an optimized process for DNS resolution can result in a reduction of distance traveled. In an ideal situation cached record data will be available, allowing a DNS name server to return a non-recursive query.

3 types of DNS queries:

1. **Recursive query** - In a recursive query, a DNS client requires that a DNS server (typically a DNS recursive resolver) will respond to the client with either the requested resource record or an error message if the resolver can't find the record.

2. **Iterative query** - in this situation the DNS client will allow a DNS server to return the best answer it can. If the queried DNS server does not have a match for the query name, it will return a referral to a DNS server authoritative for a lower level of the domain namespace. The DNS client will then make a query to the referral address. This process continues with additional DNS servers down the query chain until either an error or timeout occurs.

3. **Non-recursive query** - typically this will occur when a DNS resolver client queries a DNS server for a record that it has access to either because it's authoritative for the record or the record exists inside of its cache. Typically, a DNS server will cache DNS records to prevent additional bandwidth consumption and load on upstream servers.

## O que é cache DNS? / What is DNS caching?

**PT-BR**  
O objetivo do cache é armazenar temporariamente dados em um local que resulte em melhorias no desempenho e na confiabilidade das solicitações de dados. O cache DNS envolve o armazenamento de dados mais próximos do cliente solicitante, para que a consulta DNS possa ser resolvida mais cedo e as consultas adicionais mais abaixo na cadeia de pesquisa DNS possam ser evitadas, melhorando assim os tempos de carregamento e reduzindo o consumo de largura de banda / CPU. Os dados DNS podem ser armazenados em cache em uma variedade de locais, cada um dos quais armazenará registros DNS por um período de tempo determinado por um tempo de vida (TTL).

Os navegadores da web modernos são projetados por padrão para armazenar em cache registros DNS por um período de tempo determinado. O objetivo aqui é óbvio; quanto mais próximo o cache DNS ocorrer do navegador da web, menos etapas de processamento devem ser executadas para verificar o cache e fazer as solicitações corretas para um endereço IP. Quando uma solicitação é feita para um registro DNS, o cache do navegador é o primeiro local verificado para o registro solicitado. No Chrome, você pode ver o status do cache DNS acessando chrome://net-internals/#dns.

**EN-US**  
The purpose of caching is to temporarily stored data in a location that results in improvements in performance and reliability for data requests. DNS caching involves storing data closer to the requesting client so that the DNS query can be resolved earlier and additional queries further down the DNS lookup chain can be avoided, thereby improving load times and reducing bandwidth/CPU consumption. DNS data can be cached in a variety of locations, each of which will store DNS records for a set amount of time determined by a time-to-live (TTL).

Modern web browsers are designed by default to cache DNS records for a set amount of time. The purpose here is obvious; the closer the DNS caching occurs to the web browser, the fewer processing steps must be taken in order to check the cache and make the correct requests to an IP address. When a request is made for a DNS record, the browser cache is the first location checked for the requested record. In Chrome, you can see the status of your DNS cache by going to chrome://net-internals/#dns.

