# Tutorial: Python Markdown para Página web
Tutorial para a criação de uma página html a partir de arquivos Markdown que utilizam Python. Utilizaremos a ferramenta [MkDocs](https://www.mkdocs.org). Para configurações mais avançadas, acesse ao site.

## Instruções
- Com Python 3.X e pip instalados em seu sistema, execute
`pip install mkdocs`.
- Clone este repositório, como você pode ver, existe uma pasta `notebooks` onde ficarão os notebooks que você utilizou no seu trabalho.
<!-- - Crie um repositório no Github e clone em seu computador. -->
<!-- - Nas configurações do seu repositório, desça até o campo ```GitHub Pages```, em ```Source``` selecione ```master branch```. Sua página agora está hospedada em [nome do seu usuário].github.io/[nome do repositório]. -->
- No terminal, caminhe até dentro do seu repositório e use o comando `mkdocs new ./`. O MkDocs irá criar os arquivos da construção do site dentro dela.

Dentro dessa pasta temos o arquivo `mkdocs.yml`, este é um arquivo YAML que contém as configurações do seu site. Dentro dessa pasta também haverá outra pasta, `docs`, que conterá os arquivos Markdown para o site.
- Para construir uma visualização do seu site, utilize o comando `mkdocs serve`, o site estará hospedado em `http://127.0.0.1:8000/`.

### Adicionando páginas
- Use o seguinte comando para converter seus notebooks em markdowns.

```bash
jupyter nbconvert --output-dir ./docs/ --to markdown notebooks/olives-eda.ipynb
jupyter nbconvert --output-dir ./docs/ --to markdown notebooks/olives-model.ipynb
```
- Páginas adicionais devem ser adicionadas como Markdown dentro do diretório `docs`. 
- No arquivo ```mkdocs.yml``` você deve organizar os arquivos de acordo com qual página será. Você deve criar a linha ```nav:``` e abaixo dela a sintaxe é ```- [nome da página]: [nome do arquivo markdown]```. No seguinte exemplo, nosso site terá duas páginas, uma página Home criada a partir do arquivo index.md e uma página Info criada a partir do arquivo info.md.

```
nav:
- Home: index.md
- EDA: olives-eda.md
- MODEL: olives-model.md
```
### Alterando a aparência
- É possível alterar a aparência do seu site utilizando temas já criados pelo MkDocs ou por usuários. Para alterar, dentro do arquivo ```mkdocs.yml``` escreva
```
theme: readthedocs
```

Essa sintaxe altera o tema do site para o estilo readthedocs. Nesse [link](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes) você pode encontrar outros temas para serem instalados e utilizados.

### Construindo o site
- Para construir e implantar seu site, você precisa executar `mkdocs gh-deploy`
- Após ter carregado os arquivos, seu site estará hospedado em ```[nome do usuário].github.io\py_mkdown_to_html```.

### Configuração extra: omitir código

Para criar menus que podem exibir/esconder campos de códigos, você deve manualmente abrir o seu arquivo markdown (antes de ter construído o site) e nos blocos que você deseja omitir deve inserir as tags ```<summary>``` e ```<details>```, da seguinte forma:

```
<details>
<summary>Code</summary>

\```python
print("hello world!")
\```

</details>
```
(Obs: a barra \ não deve estar presente no código).
Observe como é apresentado o resultado:

<details>
<summary>Code</summary>

```python
print("hello world!")
```

</details>


