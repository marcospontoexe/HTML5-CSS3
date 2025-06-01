
# Introdução ao Desenvolvimento Web

## HTML: Fundamentos

- HTML **não é uma linguagem de programação**.
- HTML é uma linguagem de marcação: *Hypertext Markup Language*.
- Estrutura hipertextos: leitura não linear, com links, imagens, vídeos, áudios etc.
- Interpretado e renderizado por navegadores.

## Estrutura de um Documento HTML

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Minha primeira página HTML</title>
</head>
<body>
    <h1>Primeiro cabeçalho da página</h1>
    <p>Primeiro parágrafo.</p>
    <p>Segundo parágrafo.</p>
</body>
</html>
```

## Headings HTML

```html
<h1>Este é o heading 1</h1>
<h2>Este é o heading 2</h2>
...
<h6>Este é o heading 6</h6>
```

## Imagens HTML

```html
<img src="figuras/cavalos.jpg" alt="Passeio a cavalo." width="289">
<img src="figuras/praia.jpg" alt="Férias na praia." width="289">
```

## Links HTML

```html
<a href="https://google.com/" target="_blank" title="Google">Site Google</a>
<a href="images.html" title="Teste de imagens">Images</a>
<a href="mailto:nome.sobrenome@site_examplo.com">Envie um e-mail</a>
```

## Listas HTML

```html
<ul>
    <li>Café</li>
    <li>Chá</li>
    <li>Leite</li>
</ul>

<ol>
    <li>Café</li>
    <li>Chá</li>
    <li>Leite</li>
</ol>

<dl>
    <dt>Café</dt>
    <dd>- Bebida quente...</dd>
</dl>
```

## Tabelas HTML

```html
<table>
  <tr>
    <th>Itens/Mês</th>
    <th>Janeiro</th>
    <th>Fevereiro</th>
  </tr>
  <tr>
    <td>Usuários</td>
    <td>80</td>
    <td>93</td>
  </tr>
</table>
```

### CSS Básico para Tabelas

```css
table, th, td {
    border: 1px solid black;
}
```

## Formatação HTML

```html
<p><b>Texto em negrito</b></p>
<p><strong>Texto importante</strong></p>
<p><i>Texto em itálico</i></p>
<p><em>Texto enfatizado</em></p>
<p><small>Texto pequeno</small></p>
<p>Texto <sub>subscrito</sub></p>
<p>Texto <sup>sobrescrito</sup></p>
```

## Formulários HTML

```html
<form>
  <label for="pname">Nome:</label><br>
  <input type="text" id="pname" name="pname" value="João"><br>
</form>
```

### Tipos de Campos de Formulário

- `text`, `radio`, `checkbox`, `submit`, `email`, `password`, `color`, `file`, `date`, `time`, `range`, etc.

## Métodos de Envio

- `GET`: visível na URL, não indicado para dados sensíveis.
- `POST`: dados enviados no corpo da mensagem HTTP.

---

## Para Praticar Mais

- [W3Schools HTML](https://www.w3schools.com/html)
- [Formulários HTML](https://www.w3schools.com/html/html_forms.asp)
