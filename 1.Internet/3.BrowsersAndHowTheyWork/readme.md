# Navegadores e como eles funcionam? Browsers and how they work?

## A funcionalidade principal do navegador / The browser's main functionality

**PT-BR**  
A função principal de um navegador é apresentar o recurso da web que você escolher, solicitando-o ao servidor e exibindo-o na janela do navegador. O recurso geralmente é um documento HTML, mas também pode ser um PDF, imagem ou outro tipo de conteúdo. A localização do recurso é especificada pelo usuário usando um URI (Uniform Resource Identifier).

A maneira como o navegador interpreta e exibe arquivos HTML é determinada nas especificações HTML e CSS. Essas especificações são mantidas pela organização W3C (World Wide Web Consortium), que é a organização de padrões para a web. Por anos, os navegadores se conformaram apenas a uma parte das especificações e desenvolveram suas próprias extensões. Isso causou sérios problemas de compatibilidade para os autores da web. Hoje, a maioria dos navegadores mais ou menos se conforma às especificações.

As interfaces do usuário do navegador têm muito em comum entre si. Entre os elementos comuns da interface do usuário estão:
1. Barra de endereço para inserir um URI
2. Botões Voltar e Avançar
3. Barra de favoritos
4. Botões Atualizar e Parar para atualizar ou interromper o carregamento de documentos atuais
5. Botão Início que leva você à sua página inicial

Curiosamente, a interface do usuário do navegador não é especificada em nenhuma especificação formal, ela vem apenas de boas práticas moldadas ao longo de anos de experiência e por navegadores se imitando. A especificação HTML5 não define os elementos da interface do usuário que um navegador deve ter, mas lista alguns elementos comuns. Entre eles estão a barra de endereço, a barra de status e a barra de ferramentas. Existem, é claro, recursos exclusivos de um navegador específico, como o gerenciador de downloads do Firefox.

***

**EN-US**  
The main function of a browser is to present the web resource you choose, by requesting it from the server and displaying it in the browser window. The resource is usually an HTML document, but may also be a PDF, image, or some other type of content. The location of the resource is specified by the user using a URI (Uniform Resource Identifier).

The way the browser interprets and displays HTML files is specified in the HTML and CSS specifications. These specifications are maintained by the W3C (World Wide Web Consortium) organization, which is the standards organization for the web. For years browsers conformed to only a part of the specifications and developed their own extensions. That caused serious compatibility issues for web authors. Today most of the browsers more or less conform to the specifications.

Browser user interfaces have a lot in common with each other. Among the common user interface elements are:

1. Address bar for inserting a URI
2. Back and forward buttons
3. Bookmarking options
4. Refresh and stop buttons for refreshing or stopping the loading of current documents
5. Home button that takes you to your home page

Strangely enough, the browser's user interface is not specified in any formal specification, it just comes from good practices shaped over years of experience and by browsers imitating each other. The HTML5 specification doesn't define UI elements a browser must have, but lists some common elements. Among those are the address bar, status bar and tool bar. There are, of course, features unique to a specific browser like Firefox's downloads manager.


## A estrutura de alto nível do navegador / The browser's high level structure


**PT-BR**  
Os principais componentes do navegador são:

1. A interface do usuário: isso inclui a barra de endereço, o botão Voltar / Avançar, o menu de favoritos, etc. Cada parte da exibição do navegador, exceto a janela onde você vê a página solicitada.
2. O mecanismo do navegador: gerencia as ações entre a interface do usuário e o mecanismo de renderização.
3. O mecanismo de renderização: responsável por exibir o conteúdo solicitado. Por exemplo, se o conteúdo solicitado for HTML, o mecanismo de renderização analisa HTML e CSS e exibe o conteúdo analisado na tela.
4. Rede: para chamadas de rede, como solicitações HTTP, usando diferentes implementações para diferentes plataformas por trás de uma interface independente de plataforma.
5. Backend da interface do usuário: usado para desenhar widgets básicos como caixas e janelas. Este backend expõe uma interface genérica que não é específica da plataforma. Por baixo, ele usa métodos de interface do usuário do sistema operacional.
6. Interpretador JavaScript. Usado para analisar e executar código JavaScript.
7. Armazenamento de dados. Esta é uma camada de persistência. O navegador pode precisar salvar todos os tipos de dados localmente, como cookies. Os navegadores também suportam mecanismos de armazenamento como localStorage, IndexedDB, WebSQL e FileSystem.

![Componentes do navegador](https://web.dev/static/articles/howbrowserswork/image/browser-components-9cd8ff834cc9c_856.png)

É importante observar que navegadores como o Chrome executam várias instâncias do mecanismo de renderização: uma para cada guia. Cada guia é executada em um processo separado.

***

**EN-US**  
The browser's main components are:

1. The user interface: this includes the address bar, back/forward button, bookmarking menu, etc. Every part of the browser display except the window where you see the requested page.
2. The browser engine: marshals actions between the UI and the rendering engine.
3. The rendering engine: responsible for displaying requested content. For example if the requested content is HTML, the rendering engine parses HTML and CSS, and displays the parsed content on the screen.
4. Networking: for network calls such as HTTP requests, using different implementations for different platform behind a platform-independent interface.
5. UI backend: used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods.
6. JavaScript interpreter. Used to parse and execute JavaScript code.
7. Data storage. This is a persistence layer. The browser may need to save all sorts of data locally, such as cookies. Browsers also support storage mechanisms such as localStorage, IndexedDB, WebSQL and FileSystem.

![Browser components](https://web.dev/static/articles/howbrowserswork/image/browser-components-9cd8ff834cc9c_856.png)


It is important to note that browsers such as Chrome run multiple instances of the rendering engine: one for each tab. Each tab runs in a separate process.

## O mecanismo de renderização / The rendering engine

**PT-BR**  
A responsabilidade do mecanismo de renderização é renderizar a exibição do conteúdo solicitado na tela do navegador. Por padrão, o mecanismo de renderização pode exibir documentos HTML, XML e imagens. Ele pode exibir outros tipos de dados por meio de plug-ins ou extensões; por exemplo, exibindo documentos PDF usando um plug-in de visualizador de PDF.

Navegadores diferentes usam mecanismos de renderização diferentes: o Internet Explorer usa o Trident, o Firefox usa o Gecko, o Safari usa o WebKit. Chrome e Opera (a partir da versão 15) usam o Blink, um fork do WebKit. O WebKit é um mecanismo de renderização de código aberto que começou como um mecanismo para a plataforma Linux e foi modificado pela Apple para suportar Mac e Windows. Veja [webkit.org](webkit.org) para mais detalhes.

***

**EN-US**  
The responsibility of the rendering engine is to render the display of the requested contents on the browser screen. By default the rendering engine can display HTML and XML documents and images. It can display other types of data via plug-ins or extension; for example, displaying PDF documents using a PDF viewer plug-in. 

Different browsers use different rendering engines: Internet Explorer uses Trident, Firefox uses Gecko, Safari uses WebKit. Chrome and Opera (from version 15) use Blink, a fork of WebKit. WebKit is an open source rendering engine which started as an engine for the Linux platform and was modified by Apple to support Mac and Windows. See [webkit.org](webkit.org) for more details.

	
## O fluxo principal / The main flow

**PT-BR**  
O mecanismo de renderização começará a obter o conteúdo do documento solicitado da camada de rede. Isso geralmente será feito em blocos de 8 kB. Depois disso, este é o fluxo básico do mecanismo de renderização:

![Fluxo básico do mecanismo de renderização](https://web.dev/static/articles/howbrowserswork/image/rendering-engine-basic-fl-2fba02b24e871_856.png)

O mecanismo de renderização começará a analisar o documento HTML e converterá os elementos em nós DOM em uma árvore chamada "árvore de conteúdo". O mecanismo analisará os dados de estilo, tanto em arquivos CSS externos quanto em elementos de estilo. As informações de estilo, juntamente com as instruções visuais no HTML, serão usadas para criar outra árvore: a árvore de renderização.

A árvore de renderização contém retângulos com atributos visuais como cor e dimensões. Os retângulos estão na ordem certa para serem exibidos na tela.

Após a construção da árvore de renderização, ela passa por um processo de "layout". Isso significa dar a cada nó as coordenadas exatas onde ele deve aparecer na tela. A próxima etapa é a pintura - a árvore de renderização será percorrida e cada nó será pintado usando a camada de backend da interface do usuário.

É importante entender que este é um processo gradual. Para uma melhor experiência do usuário, o mecanismo de renderização tentará exibir o conteúdo na tela o mais rápido possível. Ele não esperará até que todo o HTML seja analisado antes de começar a construir e organizar a árvore de renderização. Partes do conteúdo serão analisadas e exibidas, enquanto o processo continua com o restante do conteúdo que continua vindo da rede.

***

**EN-US**  

The rendering engine will start getting the contents of the requested document from the networking layer. This will usually be done in 8kB chunks. After that, this is the basic flow of the rendering engine:

![Rendering engine basic flow](https://web.dev/static/articles/howbrowserswork/image/rendering-engine-basic-fl-2fba02b24e871_856.png)

The rendering engine will start parsing the HTML document and convert elements to DOM nodes in a tree called the "content tree". The engine will parse the style data, both in external CSS files and in style elements. Styling information together with visual instructions in the HTML will be used to create another tree: the render tree.

The render tree contains rectangles with visual attributes like color and dimensions. The rectangles are in the right order to be displayed on the screen.

After the construction of the render tree it goes through a "layout" process. This means giving each node the exact coordinates where it should appear on the screen. The next stage is painting - the render tree will be traversed and each node will be painted using the UI backend layer.

It's important to understand that this is a gradual process. For better user experience, the rendering engine will try to display contents on the screen as soon as possible. It will not wait until all HTML is parsed before starting to build and layout the render tree. Parts of the content will be parsed and displayed, while the process continues with the rest of the contents that keeps coming from the network.

## Exemplos de fluxo principal / Main flow examples

**PT-BR**  
Fluxo principal do WebKit:

![Fluxo principal do WebKit](https://web.dev/static/articles/howbrowserswork/image/webkit-main-flow-b779d50c0cf28_856.png)

Fluxo principal do mecanismo de renderização Gecko da Mozilla:

![Fluxo principal do mecanismo de renderização Gecko da Mozilla](https://web.dev/static/articles/howbrowserswork/image/mozillas-gecko-rendering-b18e445544965_856.jpg)

Você pode ver que, embora o WebKit e o Gecko usem terminologia ligeiramente diferente, o fluxo é basicamente o mesmo. O Gecko chama a árvore de elementos visualmente formatados de "árvore de quadros". Cada elemento é um quadro. O WebKit usa o termo "Render Tree" e consiste em "Render Objects". O WebKit usa o termo "layout" para a colocação de elementos, enquanto o Gecko chama de "Reflow". "Attachment" é o termo do WebKit para conectar nós DOM e informações visuais para criar a árvore de renderização. Uma pequena diferença não semântica é que o Gecko tem uma camada extra entre o HTML e a árvore DOM. É chamado de "content sink" e é uma fábrica para fazer elementos DOM.

***

**EN-US**  

WebKit main flow:

![WebKit main flow](https://web.dev/static/articles/howbrowserswork/image/webkit-main-flow-b779d50c0cf28_856.png)

Mozilla's Gecko rendering engine main flow:

![Mozilla's Gecko rendering engine main flow](https://web.dev/static/articles/howbrowserswork/image/mozillas-gecko-rendering-b18e445544965_856.jpg)

You can see that although WebKit and Gecko use slightly different terminology, the flow is basically the same. Gecko calls the tree of visually formatted elements a "Frame tree". Each element is a frame. WebKit uses the term "Render Tree" and it consists of "Render Objects". WebKit uses the term "layout" for the placing of elements, while Gecko calls it "Reflow". "Attachment" is WebKit's term for connecting DOM nodes and visual information to create the render tree. A minor non-semantic difference is that Gecko has an extra layer between the HTML and the DOM tree. It is called the "content sink" and is a factory for making DOM elements.