Ótima ideia\! Adicionar as fontes utilizadas é crucial para que outros usuários consigam compilar o documento exatamente como você o projetou. Isso evita erros e garante a reprodução fiel do seu template.

Abaixo está o `README.md` atualizado, com uma nova seção de **Fontes Necessárias** e uma revisão na seção de Pré-requisitos para deixar a informação mais clara.

-----

# Modelo Editorial para Livro A5 (Pocket) em LaTeX

Um template de LaTeX focado em uma tipografia limpa e com uma estética editorial profissional, ideal para a criação de livros no formato A5 (formato de bolso). Este modelo foi desenvolvido para produzir um resultado final com uma aparência quase perfeita, com ajustes finos de layout, margens e fontes.

## Exemplo de Saída

Para ver o resultado final, baixe o PDF de exemplo.
(É altamente recomendável que você adicione uma imagem ou screenshot do PDF aqui para que os usuários possam ver a qualidade da formatação.)

## Funcionalidades Principais

  * Formato de livro A5 (148mm x 210mm).
  * Estrutura de livro completa: capa, folha de rosto, prefácio, sumário, capítulos, bibliografia.
  * Tipografia cuidadosamente ajustada para leitura confortável.
  * Utiliza **LuaLaTeX** para recursos avançados de tipografia e manipulação de fontes.
  * Utiliza Biber para Referências.
  * Basta usar o Texstudio e o arquivo main.tex com lualatex + biber.
  * O Parte1.tex é onde estão os capítulos.
  * Documento totalmente editável a partir do seu gosto.
  * Os textos no livro são exemplos...

## Como Usar

### Pré-requisitos

Para compilar este modelo, você precisará ter o LaTeX instalado com a suíte `texlive` e as ferramentas `biber` e `bibtool`.

Você pode instalar os pacotes essenciais com o seguinte comando no Debian:

```bash
sudo apt-get install texlive biber bibtool cm-super cm-super-minimal fonts-adf-accanthis fonts-adf-berenis fonts-adf-gillius fonts-adf-universalis fonts-adobe-sourcesans3 fonts-cabin fonts-cantarell fonts-clear-sans fonts-comfortaa fonts-comic-neue fonts-croscore fonts-crosextra-caladea fonts-crosextra-carlito fonts-dejavu-core fonts-dejavu-extra fonts-dejavu-mono fonts-droid-fallback fonts-ebgaramond-extra fonts-font-awesome fonts-freefont-otf fonts-freefont-ttf fonts-gfs-artemisia fonts-gfs-baskerville fonts-gfs-complutum fonts-gfs-didot fonts-gfs-neohellenic fonts-gfs-olga fonts-gfs-porson fonts-gfs-solomos fonts-go fonts-hack fonts-inter fonts-lato fonts-liberation fonts-liberation-sans-narrow fonts-linuxlibertine fonts-lmodern fonts-lobster fonts-lobstertwo fonts-noto fonts-noto-cjk fonts-noto-cjk-extra fonts-noto-color-emoji fonts-noto-core fonts-noto-extra fonts-noto-mono fonts-noto-ui-core fonts-noto-ui-extra fonts-noto-unhinted fonts-oflb-asana-math fonts-open-sans fonts-opensymbol fonts-paratype fonts-quicksand fonts-roboto-slab fonts-roboto-unhinted fonts-sil-andika fonts-sil-charis fonts-sil-gentium fonts-sil-gentium-basic fonts-sil-gentiumplus fonts-sil-gentiumplus-compact fonts-stix fonts-symbola fonts-texgyre fonts-texgyre-math fonts-tuffy fonts-urw-base35 latex-make latexmk libbibtex-parser-perl liblatex-tounicode-perl libtext-bibtex-perl lmodern preview-latex-style texlive-base texlive-bibtex-extra texlive-binaries texlive-extra-utils texlive-font-utils texlive-fonts-extra texlive-fonts-extra-links texlive-fonts-recommended texlive-formats-extra texlive-humanities texlive-lang-english texlive-lang-greek texlive-lang-portuguese texlive-latex-base texlive-latex-extra texlive-latex-recommended texlive-luatex texlive-metapost texlive-pictures texlive-plain-generic texlive-publishers texlive-science texlive-xetex
```

### Fontes Necessárias

Este modelo utiliza as seguintes fontes, que devem estar instaladas em seu sistema para que a compilação funcione corretamente:

  * **Principal (`\setmainfont`):** Sabon MT Std
  * **Sans Serif (`\setsansfont`):** Urbanist-SemiBold
  * **Mono (`\setmonofont`):** Source Code Pro
  * **Matemática (`\setmathfont`):** Latin Modern Math

### Estrutura do Projeto

O projeto está organizado da seguinte forma:

```
.
├── frontmatter/                # Arquivos da parte inicial do livro (capa, prefácio, etc.)
│   ├── Capa.png
│   ├── copyrightpage.tex
│   └── titlepage.tex
├── misc/                       # Arquivos de estilo e configuração
│   └── options.sty             # Arquivo principal com as configurações de estilo
├── main.tex                    # Arquivo principal para compilação
└── referencias.bib             # Exemplo de arquivo de bibliografia
└── Parte 1.tex                 # Exemplo de arquivo de capítulo
```

### Compilação

Este modelo requer a compilação com **LuaLaTeX** e a ferramenta **biber** para a bibliografia. Siga estes passos para gerar o PDF final:

1.  **Compile o arquivo principal com LuaLaTeX:**
    ```bash
    lualatex main.tex
    ```
2.  **Gere a bibliografia com biber:**
    ```bash
    biber main
    ```
3.  **Compile novamente com LuaLaTeX para que as referências sejam incluídas:**
    ```bash
    lualatex main.tex
    ```
4.  **(Opcional) Compile uma terceira vez para garantir que o sumário, referências cruzadas, etc., estejam corretos:**
    ```bash
    lualatex main.tex
    ```

Como alternativa, você pode usar a ferramenta `latexmk` para automatizar este processo. Edite o arquivo `.latexmkrc` ou use a flag `-lualatex`:

```bash
latexmk -lualatex main.tex
```

## Como Customizar

  * **Título e Autor**: Edite o arquivo `main.tex` para alterar o título, autor e outras informações do livro.
  * **Estilo Visual**: O arquivo `misc/options.sty` contém a maioria das configurações de fontes, cores, e layout. Edite-o com cuidado para fazer alterações de estilo.
  * **Fontes**: As fontes padrão são configuradas no `options.sty`, mas você pode alterar para outras fontes que você preferir.

## Contribuição

Sinta-se à vontade para abrir uma *issue* para sugerir melhorias ou enviar um *pull request* com novas funcionalidades. Seu feedback é muito bem-vindo\!

## Licença

Este projeto está licenciado sob a **Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)**. Isso significa que você pode usar, modificar e distribuir este trabalho, desde que dê o devido crédito ao autor original.

Para mais detalhes, consulte o texto completo da licença neste link: [Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.pt_BR)
