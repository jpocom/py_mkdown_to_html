# py_mkdown_to_html
Tutorial para a criação de uma página html a partir de arquivos Markdown que utilizam Python. Utilizaremos a ferramenta [MkDocs](https://www.mkdocs.org).

## Instruções
- Com Python(2.7, 3.4, 3.5, 3.6, 3.7) e pip instalados em seu sistema, execute
```pip install mkdocs```.
- Crie um repistório no Github e clone em seu computador.
- Nas configurações do seu repositório, desça até o campo ```GitHub Pages```, em ```Source``` selecione ```master branch```. Sua página agora está hospedada em [nome do seu usuário].github.io/[nome do repositório].
- No terminal, caminhe até dentro do seu repositório e use o comando ```mkdocs new [nome projeto]```. O MkDocs irá criar uma pasta com o nome [nome do projeto] com os arquivos da construção do site dentro dela. Caminhe para dentro dessa pasta.
Dentro dessa pasta temos o arquivo ```mkdocs.yml```, este é um arquivo YAML que contém as configurações do seu site. Dentro dessa pasta também haverá outra pasta, ```docs```, contendo os arquivos Markdown para o site.
- Para construir uma visualização do seu site, utilize o comando ```mkdocs serve```, o site estará hospedado em ```http://127.0.0.1:8000/```.
### Adicionando páginas
- As páginas devem ser adicionadas como Markdown dentro do diretório ```[nome do projeto]\docs```.
