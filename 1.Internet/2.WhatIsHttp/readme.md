# O que é HTTP? / What is HTTP?

**PT-BR**  
O _Hypertext Transfer Protocol_ (HTTP) é a base da World Wide Web, e é usado para carregar páginas da web usando links de hipertexto. O HTTP é um protocolo de camada de aplicação projetado para transferir informações entre dispositivos em rede e é executado em cima de outras camadas da pilha de protocolos de rede. Um fluxo típico sobre HTTP envolve uma máquina cliente fazendo uma requisição a um servidor, que então envia uma mensagem de resposta.

***

**EN-US**  
The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.

## O que tem em uma requisição HTTP? / What is in an HTTP request?

**PT-BR**  
Uma requisição HTTP é a maneira como as plataformas de comunicação da Internet, como navegadores da web, solicitam as informações de que precisam para carregar um site. Cada requisição HTTP feita pela Internet carrega consigo uma série de dados codificados que carregam diferentes tipos de informações. Uma requisição HTTP típica contém:

1. Tipo de versão HTTP.
2. Uma URL.
3. Um método HTTP.
4. Cabeçalhos de requisição HTTP.
5. Corpo HTTP opcional.

***

**EN-US**  
An HTTP request is the way Internet communications platforms such as web browsers ask for the information they need to load a website Each HTTP request made across the Internet carries with it a series of encoded data that carries different types of information. A typical HTTP request contains:

1. HTTP version type.
2. A URL.
3. An HTTP method.
4. HTTP request headers.
5. Optional HTTP body.

## O que é um método HTTP? / What is an HTTP method?

**PT-BR**  
Os métodos HTTP, também conhecidos como verbos HTTP, são maneiras padronizadas de especificar a ação desejada a ser executada em um recurso identificado por uma URL. Quando um cliente (como um navegador da web ou um aplicativo) se comunica com um servidor por meio do protocolo HTTP, ele usa esses métodos para indicar o tipo de operação que deseja executar no recurso.

Aqui estão alguns métodos HTTP comuns:

1. **GET**: O método GET é usado para solicitar dados de um recurso especificado. Não deve ter nenhum efeito colateral no servidor, o que significa que ele deve apenas recuperar dados e não modificá-los.

2. **POST**: O método POST é usado para enviar dados a serem processados para um recurso especificado. Muitas vezes resulta na criação de um novo recurso ou na atualização de um existente.

3. **PUT**: O método PUT é usado para atualizar um recurso ou criar um novo recurso se ele não existir na URL especificada. É idempotente, o que significa que várias solicitações idênticas devem ter o mesmo efeito que uma única solicitação.

4. **PATCH**: O método PATCH é usado para aplicar modificações parciais a um recurso. É frequentemente usado quando você deseja atualizar parte de um recurso sem afetar o restante.

5. **DELETE**: O método DELETE é usado para solicitar a remoção de um recurso identificado por uma URL. Indica que o cliente deseja excluir o recurso.

6. **OPTIONS**: O método OPTIONS é usado para descrever as opções de comunicação para o recurso de destino. É frequentemente usado pelos clientes para descobrir os métodos, cabeçalhos ou outras informações permitidos sobre um recurso.

7. **HEAD**: O método HEAD é semelhante ao GET, mas é usado para recuperar os cabeçalhos de um recurso sem os dados reais. É frequentemente usado para verificar o status de um recurso ou para obter metadados sobre ele.

***

**EN-US**  
HTTP methods, also known as HTTP verbs, are standardized ways of specifying the desired action to be performed on a resource identified by a URL. When a client (such as a web browser or an application) communicates with a server over the HTTP protocol, it uses these methods to indicate the type of operation it wants to perform on the resource.

Here are some common HTTP methods:

1. **GET**: The GET method is used to request data from a specified resource. It should not have any side effects on the server, meaning it should only retrieve data and not modify it.

2. **POST**: The POST method is used to submit data to be processed to a specified resource. It often results in the creation of a new resource or the update of an existing one.

3. **PUT**: The PUT method is used to update a resource or create a new resource if it does not exist at the specified URL. It is idempotent, meaning that multiple identical requests should have the same effect as a single request.

4. **PATCH**: The PATCH method is used to apply partial modifications to a resource. It is often used when you want to update part of a resource without affecting the rest of it.

5. **DELETE**: The DELETE method is used to request the removal of a resource identified by a URL. It indicates that the client wants to delete the resource.

6. **OPTIONS**: The OPTIONS method is used to describe the communication options for the target resource. It is often used by clients to discover the allowed methods, headers, or other information about a resource.

7. **HEAD**: The HEAD method is similar to GET but is used to retrieve the headers of a resource without the actual data. It is often used to check the status of a resource or to obtain metadata about it.

## O que são cabeçalhos de requisição HTTP? / What are HTTP request headers?

**PT-BR**  
Os cabeçalhos HTTP contêm informações de texto armazenadas em pares de chave-valor, e eles estão incluídos em cada requisição HTTP (e também na resposta HTTP, que será abordado depois). Esses cabeçalhos comunicam informações básicas, como qual navegador o cliente está usando e quais dados estão sendo solicitados.

Exemplo de cabeçalhos de requisição HTTP da guia de rede do Google Chrome:

![cabeçalhos de requisição da guia de rede do Google Chrome](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-request-headers.png)

***

**EN-US**  
HTTP headers contain text information stored in key-value pairs, and they are included in every HTTP request (and also in the HTTP response, which will be covered later). These headers communicate basic information, such as what browser the client is using and what data is being requested.

Example of HTTP request headers from Google Chrome's network tab:

![request headers from Google Chrome's network tab](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-request-headers.png)

## O que tem em um corpo de requisição HTTP? / What is in an HTTP request body?

**PT-BR**  
O corpo de uma requisição é a parte que contém o ‘corpo’ de informações que a requisição está transferindo. O corpo de uma requisição HTTP contém qualquer informação sendo enviada para o servidor web, como um nome de usuário e senha, ou qualquer outro dado inserido em um formulário.

***

**EN-US**  
The body of a request is the part that contains the ‘body’ of information the request is transferring. The body of an HTTP request contains any information being submitted to the web server, such as a username and password, or any other data entered into a form.

## O que tem em uma resposta HTTP? / What is in an HTTP response?

**PT-BR**  
Uma resposta HTTP é o que os clientes da web (geralmente navegadores) recebem de um servidor da Internet em resposta a uma requisição HTTP. Essas respostas comunicam informações valiosas com base no que foi solicitado na requisição HTTP. Uma resposta HTTP típica contém:

1. Um código de status HTTP.
2. Cabeçalhos de resposta HTTP.
3. Um corpo HTTP opcional.

***

**EN-US**  
An HTTP response is what web clients (often browsers) receive from an Internet server in answer to an HTTP request. These responses communicate valuable information based on what was asked for in the HTTP request. A typical HTTP response contains:

1. An HTTP status code.
2. HTTP response headers.
3. An optional HTTP body.

## O que é um código de status HTTP? / What is an HTTP status code?

**PT-BR**  
Os códigos de status HTTP são códigos de 3 dígitos usados para indicar se uma requisição HTTP foi concluída com sucesso. Os códigos de status são divididos nos seguintes 5 blocos:

1. 1xx Informativo
2. 2xx Sucesso
3. 3xx Redirecionamento
4. 4xx Erro do cliente
5. 5xx Erro do servidor

O “xx” se refere a números diferentes entre 00 e 99.

Códigos de status que começam com o número ‘2’ indicam um sucesso. Por exemplo, após um cliente solicitar uma página da web, as respostas mais comumente vistas têm um código de status ‘200 OK’, indicando que a requisição foi concluída corretamente.

Se a resposta começar com um ‘4’ ou um ‘5’ isso significa que houve um erro e a página da web não será exibida. Um código de status que começa com um ‘4’ indica um erro do lado do cliente (é muito comum encontrar um código de status ‘404 NOT FOUND’ ao digitar errado uma URL). Um código de status que começa com ‘5’ significa que algo deu errado no lado do servidor. Os códigos de status também podem começar com um ‘1’ ou um ‘3’, que indicam uma resposta informativa e um redirecionamento, respectivamente.

***

**EN-US**  
HTTP status codes are 3-digit codes used to indicate whether an HTTP request has been successfully completed. Status codes are broken into the following 5 blocks:

1. 1xx Informational
2. 2xx Success
3. 3xx Redirection
4. 4xx Client Error
5. 5xx Server Error

The “xx” refers to different numbers between 00 and 99.

Status codes starting with the number ‘2’ indicate a success. For example, after a client requests a webpage, the most commonly seen responses have a status code of ‘200 OK’, indicating that the request was properly completed.

If the response starts with a ‘4’ or a ‘5’ that means there was an error and the webpage will not be displayed. A status code that begins with a ‘4’ indicates a client-side error (it is very common to encounter a ‘404 NOT FOUND’ status code when making a typo in a URL). A status code beginning in ‘5’ means something went wrong on the server side. Status codes can also begin with a ‘1’ or a ‘3’, which indicate an informational response and a redirect, respectively.

## O que são cabeçalhos de resposta HTTP? / What are HTTP response headers?

**PT-BR**  
Assim como uma requisição HTTP, uma resposta HTTP vem com cabeçalhos que transmitem informações importantes, como o idioma e o formato dos dados sendo enviados no corpo da resposta.

Exemplo de cabeçalhos de resposta HTTP da guia de rede do Google Chrome:

![cabeçalhos de resposta da guia de rede do Google Chrome](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-response-headers.png)

***

**EN-US**  
Much like an HTTP request, an HTTP response comes with headers that convey important information such as the language and format of the data being sent in the response body.

Example of HTTP response headers from Google Chrome's network tab:

![response headers from Google Chrome's network tab](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-response-headers.png)

## O que tem em um corpo de resposta HTTP? / What is in an HTTP response body?

**PT-BR**  
O corpo da resposta HTTP contém os dados que são enviados do servidor para o cliente em resposta a uma requisição HTTP. O conteúdo do corpo da resposta depende da natureza da requisição e do tipo do recurso sendo acessado. Aqui estão alguns tipos comuns de dados que podem ser encontrados no corpo de uma resposta HTTP:

1. **Conteúdo HTML**: Em resposta a uma requisição de uma página da web, o servidor normalmente envia de volta o conteúdo HTML da página no corpo da resposta. O navegador da web do cliente então renderiza esse HTML para exibir a página da web.

2. **Dados JSON ou XML**: Muitos aplicativos da web modernos usam JSON (JavaScript Object Notation) ou XML (Extensible Markup Language) para trocar dados entre o cliente e o servidor. O corpo da resposta pode conter dados estruturados nesses formatos, que o código do lado do cliente pode analisar e usar.

3. **Dados binários**: Algumas requisições podem resultar na transferência de dados binários, como imagens, vídeos ou outro conteúdo multimídia. Os dados binários são incluídos no corpo da resposta.

4. **Dados de texto**: O conteúdo de texto simples também pode ser enviado no corpo da resposta. Este pode ser o caso de informações textuais simples ou mensagens de erro.

5. **Downloads de arquivos**: Em alguns casos, o servidor pode responder com um download de arquivo. O corpo da resposta então contém os dados binários do arquivo, e o cliente pode solicitar ao usuário que faça o download e salve o arquivo localmente.

6. **Formatos de dados personalizados**: Dependendo do aplicativo, formatos de dados personalizados podem ser usados no corpo da resposta. Estes podem ser formatos proprietários ou específicos para os requisitos do aplicativo.

O tipo de dados no corpo da resposta é indicado pelo cabeçalho "Content-Type" na resposta HTTP. Este cabeçalho especifica o tipo de mídia do recurso enviado ao cliente. Por exemplo, "Content-Type: text/html" indica que o corpo da resposta contém conteúdo HTML. O cliente usa essas informações para processar a resposta adequadamente.

***

**EN-US**  

The HTTP response body contains the data that is sent from the server to the client in response to an HTTP request. The content of the response body depends on the nature of the request and the type of the resource being accessed. Here are some common types of data that can be found in an HTTP response body:

1. **HTML Content**: In response to a request for a web page, the server typically sends back the HTML content of the page in the response body. The client's web browser then renders this HTML to display the webpage.

2. **JSON or XML Data**: Many modern web applications use JSON (JavaScript Object Notation) or XML (eXtensible Markup Language) for exchanging data between the client and server. The response body may contain structured data in these formats, which the client-side code can parse and use.

3. **Binary Data**: Some requests may result in the transfer of binary data, such as images, videos, or other multimedia content. The binary data is included in the response body.

4. **Text Data**: Plain text content can also be sent in the response body. This might be the case for simple textual information or error messages.

5. **File Downloads**: In some cases, the server may respond with a file download. The response body then contains the binary data of the file, and the client may prompt the user to download and save the file locally.

6. **Custom Data Formats**: Depending on the application, custom data formats may be used in the response body. These could be proprietary formats or specific to the requirements of the application.

The type of data in the response body is indicated by the "Content-Type" header in the HTTP response. This header specifies the media type of the resource sent to the client. For example, "Content-Type: text/html" indicates that the response body contains HTML content. The client uses this information to process the response appropriately.

## HTTP é sem estado, mas não sem sessão / HTTP is stateless, but not sessionless

**PT-BR**  
O HTTP é sem estado: não há link entre duas requisições sendo sucessivamente realizadas na mesma conexão. Isso imediatamente tem a perspectiva de ser problemático para usuários que tentam interagir com determinadas páginas de forma coerente, por exemplo, usando carrinhos de compras em e-commerce.

Mas, embora o núcleo do HTTP em si seja sem estado, os cookies HTTP permitem o uso de sessões com estado. Usando a extensibilidade do cabeçalho, os cookies HTTP são adicionados ao fluxo de trabalho, permitindo a criação de sessões em cada requisição HTTP para compartilhar o mesmo contexto, ou o mesmo estado.


***

**EN-US**  
HTTP is stateless: there is no link between two requests being successively carried out on the same connection. This immediately has the prospect of being problematic for users attempting to interact with certain pages coherently, for example, using e-commerce shopping baskets.

But while the core of HTTP itself is stateless, HTTP cookies allow the use of stateful sessions. Using header extensibility, HTTP Cookies are added to the workflow, allowing session creation on each HTTP request to share the same context, or the same state.