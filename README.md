# Aula-sass

Sass (Syntactically Awesome Style Sheets) é uma extensão CSS que facilita o desenvolvimento de folhas de estilo. Ele adiciona recursos como variáveis, aninhamento, mixins e funções, permitindo que os desenvolvedores escrevam código CSS mais organizado e reutilizável. Com Sass, é possível criar estilos de forma mais eficiente, além de promover uma melhor manutenção do código. Ele compila arquivos Sass em CSS padrão, que pode ser entendido por todos os navegadores. Essa ferramenta é amplamente utilizada em projetos web para melhorar a produtividade e a estrutura do código.

# Node JS

Para utilizar o Sass, especialmente em sua versão mais moderna (Sass indented syntax ou SCSS), é necessário ter o Node.js instalado. Veja algumas razões para isso:

- Compilação: O Sass precisa ser compilado em CSS antes de ser utilizado em um projeto web. O Node.js fornece um ambiente para executar essa compilação de forma eficiente.
- Ferramentas de Desenvolvimento: Muitas ferramentas modernas de desenvolvimento front-end, como Gulp, Webpack e Parcel, utilizam Node.js para automatizar tarefas. Essas ferramentas podem integrar o Sass facilmente, permitindo a compilação automática sempre que um arquivo Sass é modificado.
- Gerenciamento de Pacotes: O Node.js vem com o npm (Node Package Manager), que permite instalar pacotes e bibliotecas, incluindo o Sass. Isso facilita a instalação e a atualização da ferramenta conforme necessário.
- Ambiente de Execução: O Node.js fornece um ambiente consistente e leve para executar o Sass, permitindo que desenvolvedores trabalhem em diferentes sistemas operacionais sem problemas de compatibilidade.

# Node para Windows
- winget install OpenJS.NodeJS

# Node para Linux (Ubuntu)
- sudo apt update
- sudo apt install nodejs npm

# Verificar a instalação
- node -v
- npm -v

# Diferença entre a sintaxe do SASS e do SCSS

# Sintaxe

SASS: 
- Utiliza uma sintaxe mais limpa e sem chaves ou ponto e vírgula.
- O Aninhamento é feito através de recuos (indentação).
- Não é compatível com CSS puro, precisa de sintaxe específica do SASS.

SCSS:
- É uma sintaxe semelhante ao CSS padrão, utiliza chaves "{}" e ponto e vírgula ";".
- Permte que qualquer código CSS válido seja um um SCSS válido.
- Compatível com CSS, é possível copiar e colar código CSS sem precisar modificá-lo.

Ambos suportam variáveis, mixins, funções e outras fncionalidades do SASS. No entanto, a forma de escrever varia de acordo com a sintaxe escolhida.

# Mixins

No SASS, mixins e @include são ferramentas que ajudam a reutilizar estilos e a manter o código organizado. Mixins são blocos de código que depois de definidos são possíveis de reutilização em diferentes partes do código. É possível incluir propriedades CSS, além de argumentos para personalização.

- Exemplo de uso do mixins:
  
  @mixin botão($cor, $tamanho) {
  background-color: $cor;
  color: white;
  padding: $tamanho;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.botão-primário {
  @include botão(#007bff, 10px);
}

.botão-secundário {
  @include botão(#6c757d, 8px);
}
