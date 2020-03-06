# aula_06_03_2020
CSS é o acrônimo de Cascading Style Sheets que em português seria algo como “folhas de estilo em cascata”. É uma especificação que define como os elementos que compõem uma página, um documento ou aplicação Web serão exibidos.

Quando falamos de acessibilidade, performance e manutenção, tem-se como princípio fazer separação do conteúdo, da interatividade e da apresentação de um site ou aplicação web. O CSS desempenha um grande papel na camada da apresentação.

A forma certa de publicar um documento web é seguindo uma estrutura semântica. O CSS traz toda a informação do layout, isto é, cores, posicionamento, fontes, tamanhos e imagens de fundo, enquanto o HTML deve fornecer uma “arquitetura” para o conteúdo. O suporte a CSS pelos navegadores de hoje é bem sólido, mas teve um início tímido, sendo inicialmente suportado pelo navegador Netscape.A primeira versão da especificação foi lançada em 1996 e uma segunda versão publicada em 1998 mas até 2009 nem todos os navegadores em uso suportavam plenamente seus recursos. Uma nova versão da especificação está em desenvolvimento e felizmente os navegadores mais recentes já estão testando-a.

Como o navegador Internet Explorer demorou a suportar todos os recursos do CSS, web developers e web designers utilizavam tabelas para montar a estrutura das páginas e toda a informação de estilo ficava junto do conteúdo. Com a melhoria das velocidades de internet (em tempos de conexão discada), foi possível adotar layouts mais complexos e modernos, ainda usando tabelas. Criou-se um mito de que projetos utilizando CSS eram muito simples, limpos e  “quadrados”. Este mito foi desvendado quando outros navegadores entraram em uso e o suporte às novas especificações foi implementado no Internet Explorer. Outro fator que contribuiu muito para a adoção das novas tecnologias para CSS foi o crescimento no uso de internet mobile em que as páginas precisam ser leves e o conteúdo apresentado de forma correta em diferentes dispositivos, o que não seria possível com tabelas.

Como funciona? Por que “cascata”?
A palavra “cascata” no nome se dá pela modularidade da especificação: Em um documento você pode ter vários arquivos CSS, carregando diferentes regras que se referem a múltiplos ou aos mesmos elementos.

Um conceito importante para o funcionamento do CSS é o modelo de blocos e elementos “inline”. Um elemento dentro de um documento HTML formatado em CSS é constituído por um bloco, um retângulo. Dentro deste bloco existe uma margem, uma borda e um preenchimento ao redor do conteúdo e através de algumas propriedades podemos alterar seus tamanhos, cores, imagens de fundo e estilos. Quando um elemento de bloco é colocado ao lado de outro, por padrão cada elemento utiliza toda a sua largura disponível e quebra a linha antes e depois de si próprio. Dentro dos elementos de bloco podem existir outros elementos de bloco ou elementos “inline”, aqueles que ocupam somente sua largura necessária e não criam linhas antes e depois de si (links, abreviações, um rótulo ou elemento de formulário por exemplo).

Talvez por conta deste conceito o mito de que os layous feitos com CSS sejam apenas “quadrados” tenha
persistido por tanto tempo.

Quais os benefícios?
CSS foi uma revolução para o desenvolvimento web. Seus benefícios mais concretos são:

Controle de interface em diferentes documentos em um único arquivo;
Controle de diferentes interfaces para diferentes dispositivos (responsive design);
Precisão para manter a mesma interface para diferentes navegadores;
Melhorias na acessibilidade com a possibilidade de “esconder” elementos da tela para usuários sem problemas de visão, mas manter os mesmos elementos acessíveis para leitores de tela;
Formulários com look and feel diferente do padrão do sistema operacional;
Menor consumo de banda para usuário e servidor;
Inúmeras técnicas dinâmicas que não poderiam ser utilizadas em tabelas;
# seletores
Seletor {propriedade: valor}

O seletor vincula um elemento do documento HTML a declaração CSS. Declaração CSS é formada pela propriedade e o valor.

A propriedade define uma característica visual para o elemento HTML “selecionado” pelo seletor.

Exemplo: O texto de um parágrafo, marcado com elemento HTML “p”, possui uma propriedade de cor denominada “color”.

Já o valor atribui valor a propriedade escolhida para o elemento selecionado.

Exemplo: O valor da propriedade color para o elemento HTML “p” selecionado é “red” (vermelho). Ou seja, o texto do parágrafo terá uma cor vermelha.

Veja o que foi explicado na imagem a seguir:

regras css
Com esta regra qualquer parágrafo em um documento HTML, desde que não selecionado de outra forma, receberá a cor vermelha.

Este parágrafo é vermelho.

Observações:

Uma regra pode ter mais que uma declaração.

p {

   font-size: 14px;   /* a fonte do texto tem 14 pixels de tamanho */

   color: red;    /* a cor da fonte é vermelha */

}
Uma regra pode ter mais de um seletor.

/* Os parágrafos e cabeçalhos h1, h2, h3 possuem cor da fonte vermelha */

p , h1, h2, h3 {

   color: red;

}
Todo conteúdo entre /* */ é um comentário. Comentários servem para instruir quem está lendo o código CSS.

Tipos de seletores comuns
Apresentarei alguns tipos de seletores mais usados que já te possibilitará estilizar páginas.

Seletor de tipo de elemento
O seletor “p” que usamos nos exemplos anteriores é um seletor de tipo de elemento. Esta espécie de seletor identifica e vincula um elemento HTML, basta que para isso coloque o elemento como seletor.

body {

   /* aqui vai uma declaração qualquer */

}


div {

   /* aqui vai uma declaração qualquer */

}

p, span, strong {

   /* aqui vai uma declaração qualquer */

}
E podemos usar um ou mais seletores para a mesma declaração. Para isso bastar usarmos vírgulas para separa-los (como nos mostra o exemplo anterior).

Seletor tipo ID
É um seletor individual usado para vincular somente um elemento por página web. Ele não pode ser usado em dois ou mais elementos. Para construí-lo basta que você crie um nome precedido pelo símbolo #.

#nome-do-identificador {

   background-color: green; /* cor de fundo verde */

}
Veja agora com atribuir no HTML para que o elemento receba a cor de fundo verde:

<body id="nome-do-identificador">
</body>
Seletor tipo class
Este seletor possibilita o uso em mais de um elemento da mesma página. Indicado quando você precisa atribuir algumas propriedades iguais em elementos diferentes. Para construí-lo basta que você crie um nome precedido por um ponto.

.nome-da-classe {

color: blue; /* cor de texto azul */

}
<h1 class="nome-da-classe">Título com cor azul</h1>


<p class="nome-da-classe">Parágrafo com a cor azul.</p>
Seletor de atributo
Este tipo de seletor associa a um atributo utilizado em um elemento HTML. Exemplo:

<input type="submit" value="Enviar">
Este é um botão para envio de dados de formulários. Podemos usar o atributo “type” com valor “submit” para estilizar o botão.

input[type="submit"] {

   font-weight: bold; /* texto em negrito */

}
