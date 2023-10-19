# HTML

Para codificar em HTML precisamos apenas de um editor de texto e de um navegador ( Google Chrome, Mozilla Firefox, etc...).

Para exibir um parágrafo em uma página, crie um novo arquivo com a extensão `.html` , insira o conteúdo a seguir e depois abra esse arquivo no navegador.

```html
<h1>Isto é um cabeçalho nível 1</h1>
```

## Tags

A linguagem HTML possui várias maneiras para representar os conteúdos que queremos apresentar nas páginas. Para isso, devemos criar os nossos **elementos** através da marcação de ***tags***. Existem diversas tags disponíveis, utilizaremos algumas delas ao longo deste material.
Para utilizar uma tag, devemos escrever a **tag de abertura**, o **conteúdo** e a **tag de fechamento**. Vejamos um exemplo:

```html
<p>Meu arquivo HTML</p>
```

`<p>` é a tag de abertura de um **parágrafo**, `"Meu arquivo HTML"` é o conteúdo e `</p>` é a tag de **fechamento** (note que o fechamento é denotado pelo caractere "barra"). Com isso escrito, temos um **elemento HTML** .

No [site da MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element) podemos ver a lista de todas as tags existentes.

## Atributos

As **tags HTML**  podem ter, opcionalmente, alguns atributos. Esses atributos são utilizados para agregar algum comportamento à **tag** em questão.

Por exemplo, quando queremos incluir um link para alguma outra página, utilizamos a tag `<a>`. Para especificarmos para onde (uma outra página ou um outro site, por exemplo) queremos que o usuário navegue quando clicarem nesse link, devemos especificar o atributo href. A seguir, um exemplo de um link que, ao ser clicado, faz com que o usuário navegue até o site da ThoughtWorks:

```html
<a href="https://thoughtworks.com/pt-br">
Clique aqui para acessar o site da ThoughtWorks</a>
```

Perceba que desse jeito quando clicamos no link saímos da página atual e somos levados para o site da TW. Caso você queira mudar esse comportamento do link, simplesmente adicione o atributo `target` e o valor `"_blank"`.

Existem, por exemplo, alguns atributos que servem para auxiliar na estilização dos elementos. São os atributos **id** e **class**. Embora eles sirvam para o mesmo propósito quando falamos de estilização, eles têm semânticas diferentes.

O atributo **id** é um identificador **único** na página. Podendo ser utilizado **somente uma vez**. O atributo **class** por sua vez, pode representar um **conjunto** de elementos. Veremos mais sobre estes atributos quando falarmos sobre **CSS**.


https://www.alura.com.br/artigos/css-guia-do-flexbox

## Tags de ênfase: `<em>` e `<strong>`
	
As tags `<em>` e `<strong>` servem para dar ênfase em algum pedaço do conteúdo. São bastante úteis quando precisamos destacar alguns pontos para o leitor da página.

```html
<p>Meu texto com <em>ênfase</em> em alguma palavra</p>
<p>Meu texto com <strong>strong</strong> em alguma palavra</p>
<p>Meu texto com <strong><em>strong e ênfase</em></strong> em alguma palavra</p>

```

## Comentários no arquivo HTML

```html
<p>
  Este texto aparece na página.
  <!-- Este aqui não aparecerá pois está comentado -->

  <!--
     Este aqui também não.
     E este comentário tem mais de uma linha.
  -->
</p>

```

## Estrutura básica de um arquivo HTML

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
</head>
<body>
  <!-- Aqui vai o conteúdo -->
</body>
</html>
```

## Título e ícone da página

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Título da minha página!</title>
  <link href="http://endereco-do-icone" rel="shortcut icon" />
</head>
<body>
  <h1>Minha página!</h1>
  <p>Agora com título e ícone</p>
</body>
</html>
```

A tag title permite que especifiquemos o título que queremos exibir na aba do navegador.

A tag link nos permite incluir um elemento externo (nesse caso, o ícone da ThoughtWorks, apontado pelo atributo href) e dizer que esse elemento representará o ícone da página (atributo rel com o valor "shortcut icon").
Embora tenhamos usado um ícone de um site externo, também podemos utilizar um ícone que baixamos. Por exemplo, digamos que baixamos o ícone na mesma pasta onde está o código HTML. Nesse caso, podemos incluir o ícone da seguinte forma:

```html
<link href="favicon.ico" rel="shortcut icon" />
```
