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

