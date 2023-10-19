# CSS

CSS é uma sigla que significa Cascading Style Sheet, em português seria Folhas de Estilo em Cascata. É um mecanismo criado para definir os estilos de uma página HTML, ou seja, no CSS descrevemos como os elementos de uma página HTML serão exibidos.

## Sintaxe base

O CSS utiliza uma estrutura simples como sintaxe. Essa estrutura é definida através de atributo e valor separados pelo sinal de dois pontos, ou seja, "atributo: valor". Veja alguns exemplos de atributos usados no CSS para decorar o HTML.

| Atributo | Descrição |
| -- | -- |
| color | Define a cor do texto utilizado no elemento. |
| text-decoration | Define uma 'decoração' para o texto, tal como sublinhado ou riscado. |
| font-size | Define o tamanho da fonte utilizada. |
| font-style | Define um estilo de fonte, tal como itálico. |

## Formas de Estilizações

A estilização feita com CSS pode ser feita através de três diferentes formas, sendo elas utilizando o **'atributo style'**, a **'tag style'** ou com base em um **'arquivo externo'**.

### Atributo Style

A inclusão de estilos utilizando o atributo style, ocorre dentro da própria tag HTML, fazendo desta estilização algo particular daquele elemento. Segue abaixo como exemplo dois elementos 'div', o primeiro estilizado com o uso do atributo style e o segundo sem qualquer estilização:

```html
<div style="color:blue">
  Sou um elemento estilizado
</div>
<div>Sou um elemento sem estilos</div>
```

### Tag Style

A segunda maneira de utilizar CSS é utilizar a tag `<style>`. Ela é utilizada geralmente dentro da tag `<head>`, sua sintaxe é como a de um elemento qualquer do HTML. Diferentemente do atributo style, a tag `<style>` define um estilo geral para elementos da página. Sua sintaxe interna é um tanto diferente da sintaxe do atributo style, pois esta faz o uso de seletores CSS. Estes seletores nos possibilitam tanto indicar tags quanto referenciar os atributos **'id'** e **'class'** do HTML, permitindo definir tanto estilizações para diversos elementos quanto para apenas um elemento em específico.

| Seletor | Descrição |
| -- | -- |
| #identificador | Referenciamos atributos id `<h1 id="identificador">` utilizando o símbolo **#** antes do nome do identificador. |
| .classe | Referenciamos atributos class `<h1 class="classe">` utilizando o símbolo . (ponto) antes do nome da classe. |
| tag | Referenciamos uma tag simplesmente utilizando seu nome. |

Segue abaixo um exemplo onde utilizamos a tag `<style>` referenciando o elemento `<p>` para colorir de verde todos elementos `<p>` do documento. Logo em seguida, referenciamos o atributo **id** de nome **identificador** para mudar sua cor para vermelho:

```html
<html>
  <head>
    <meta charset="utf-8">
    <title>Titulo</title>
    <style>
      p {
        color: green;
      }
      #identificador {
        color: red;
      }
    </style>
  </head>
  <body>
    <p>Sou um elemento estilizado pela tag style</p>
    <p>Também sou um elemento estilizado pela tag style</p>
    <div id="identificador">
      Sou um elemento estilizado pela tag style 
      referenciando o atributo id
    </div>
  </body>
</html>
```

É importante ressaltar que as mudanças realizadas pela tag style alteraram todos elementos `<p>` presentes no documento HTML.

### Arquivo externo

A terceira forma de fazermos a estilização do conteúdo é declarar o CSS através da inclusão de um arquivo externo, esta forma geralmente é a mais utilizada dentre as três.

Este arquivo geralmente possui a extensão **.css** e deve ser incluído no documento HTML em que será utilizado. Esta inclusão é realizada com o uso da tag `<link>`, referenciando a localização do arquivo externo com o atributo `href`.
Vejamos um exemplo:

```html
<head>
    <link rel="stylesheet" href="nomedoarquivoexterno.css"/>
</head>
```

Assim como na tag `<style>`, dentro do arquivo externo utilizamos de seletores para referenciar os elementos a serem estilizados. Também como na tag `<style>`, as alterações indicando nome de tag são realizadas em todos elementos da mesma tag, assim como as alterações feitas referenciando alguma classe, impactam todos elementos que estiverem utilizando ela. Segue exemplo abaixo:

| pagina.html |
| -- |

```html
<html>
  <head>
    <meta charset="utf-8">
    <title>Titulo</title>
    <link rel="stylesheet" href="arquivoexterno.css">
  </head>
  <body>
    <h1>Cabeçalho</h1>
    <p id="primeiro-paragrafo">Descrições do primeiro parágrafo</p>
    <p class="paragrafo-comum">Descrições de um parágrafo comum</p>
    <p class="paragrafo-comum">Descrições de outro parágrafo comum</p>
  </body>
</html>
```

| arquivoexterno.css |
| -- |

```css
#primeiro-paragrafo {
  color: darkblue;
  font-size: 23px;
}
.paragrafo-comum {
   color: blue;
   font-size: 13px;
}
h1 {
   font-style: italic;
   text-decoration: underline;
}

```