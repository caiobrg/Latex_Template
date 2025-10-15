## TEMPLATE 
# Modelo de Documento LaTeX para Trabalhos Acadêmicos

Este é um modelo base para a criação de documentos acadêmicos (relatórios, artigos, etc.) em LaTeX. A estrutura de diretórios foi pensada para separar a configuração, o conteúdo e os recursos, facilitando a reutilização e a manutenção do projeto.

## Estrutura de Diretórios

O projeto está organizado da seguinte forma:
.
├── main.tex              # Arquivo principal, o "maestro" do documento
├── bibliography.bib      # Arquivo para as referências bibliográficas
├── README.md             # Este arquivo
├── .gitignore            # Ignora arquivos temporários do LaTeX no Git
│
├── content/              # Pasta para os arquivos de conteúdo (.tex)
│   ├── 01_introducao.tex
│   └── ...
│
├── settings/             # Pasta para as configurações do documento
│   ├── packages.tex      # Onde todos os pacotes são importados
│   ├── commands.tex      # Comandos personalizados e configurações
│   └── titlepage.tex     # Código da página de rosto customizada
│
└── figures/              # Pasta para todas as imagens e figuras
└── placeholder.png

## Como Usar

1.  **Clone ou baixe este repositório.**
2.  **Edite `main.tex`**: Altere as informações específicas do documento (título, autor, curso, etc.) no bloco de "INFORMAÇÕES ESPECÍFICAS DO DOCUMENTO".
3.  **Escreva seu texto**: Adicione ou edite os arquivos `.tex` dentro da pasta `content/`. A ordem é controlada pelos `\include` no `main.tex`.
4.  **Adicione imagens**: Coloque seus arquivos de imagem (`.png`, `.jpg`, `.pdf`) na pasta `figures/`.
5.  **Adicione referências**: Insira suas citações em formato BibTeX no arquivo `bibliography.bib`.

## Compilação

Para compilar o documento, é altamente recomendável usar o `latexmk`. Ele lida automaticamente com as múltiplas compilações necessárias para referências, sumário e citações.

No terminal, na pasta raiz do projeto, execute:

```bash
latexmk -pdf -pvc main.tex
