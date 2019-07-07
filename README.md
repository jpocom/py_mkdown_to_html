# Tutorial: Python Markdown para Página web
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
- As páginas devem ser adicionadas como Markdown dentro do diretório ```[nome do projeto]\docs```. Observação, a homepage do seu site deve ser nomeada com ```index.md```. Copie seus arquivos Markdown para dentro do repositório.
- No arquivo ```mkdocs.yml``` você deve organizar os arquivos de acordo com qual página será. Você deve criar a linha ```nav:``` e abaixo dela a sintaxe é ```- [nome da página]: [nome do arquivo markdown]```. No seguinte exemplo, nosso site terá duas páginas, uma página Home criada a partir do arquivo index.md e uma página Info criada a partir do arquivo info.md.

```
nav:
- Home: index.md
- Info: info.md
```
### Alterando a aparência
- É possível alterar a aparência do seu site utilizando temas já criados pelo MkDocs ou por usuários. Para alterar, dentro do arquivo ```mkdocs.yml``` escreva
```
theme: readthedocs
```
Essa sintaxe altera o tema do site para o estilo readthedocs. Nesse [link](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes) você pode encontrar outros temas para serem instalados e utilizados.
### Construindo o site
Para construir o seu site, dentro do repositório [nome do projeto] execute o comando ```mkdocs build```.
