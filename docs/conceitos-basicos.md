# Git em palavras simples
 <img src="../images/Git_icon.png" width="10%" height="10%" align="right" valign="center"/> 

### Arquivo OU Blob
Todo o conteúdo de um arquivo é armazenado em uma coisa chamada blob. Quando um arquivo é alterado, um novo blob armazenará o arquivo completo com todas as novas alterações. Blob é uma das unidades básicas de armazenamento do Git. Outros tipos de unidades/objetos são Commit e Tree.

![Um blob armazena o conteúdo do arquivo](https://xosh.org/blog/img_git/blob.png)
<p aling="center">Um blob armazena o conteúdo do arquivo</p>
<br/>

### HASH
de9f2c7fd25e1b3afad3e85a0bd17d9b100db4b3. Você vê uma string estranha semelhante ou sua forma abreviada com (primeiros caracteres) em todo o git. Isto é hash( SHA1 ). Um hash pode apontar para um blob, um commit ou uma árvore. São 40 caracteres, mas apenas alguns são suficientes para identificar um commit. Por exemplo, o GitHub mostra os primeiros 10 caracteres.

![Um Hash para cada unidade básica](https://xosh.org/blog/img_git/hash.png)
<p aling="center">Um Hash para cada unidade básica</p>

### Tree

Os arquivos são sempre armazenados em algum diretório ou pasta. As pastas também podem conter mais diretórios. Da mesma forma, um `tree` em git representa diretórios para blobs e mais tree's.

Sempre há uma tree na raiz, apontando para a tree que contém coisas.

![Uma árvore armazena de blob's e tree's](https://xosh.org/blog/img_git/hash.png)
<p aling="center">Uma árvore armazena de blob's e tree's</p>

### Commit
Agora digamos que você tenha dois arquivos. Você deseja salvá-los de uma forma que possa voltar a eles exatamente no mesmo estado a qualquer momento mais tarde. Quando você salva um bloco de alterações dele com o git, um commit criado apontando para a árvore com dois blobs (vamos chamá-los de blob1 e blob2). Cada commit tem seu próprio hash e também salva sua mensagem, timestamp de data/hora e suas informações.

![Um commit aponta para a árvore](https://xosh.org/blog/img_git/commit1.png)
<p aling="center">Um commit aponta para a árvore</p>

Quando você altera um arquivo (blob1) e faz um commit, o git armazenará o arquivo completo novamente em um novo blob (blob1c). Uma nova árvore é criada com um novo hash apontando para blob2 e o novo blob1c. Agora seu repositório git possui as duas versões de um arquivo.

![Para cada mudança há um novo blob e uma nova tree](https://xosh.org/blog/img_git/commit2.png)
<p aling="center">Para cada mudança há um novo blob e uma nova tree</p>

_Check in = Faça um commit_<br/>
Check-in é simplesmente outro nome para fazer um commit no repositório.

_Check out = Carregar um commit_<br/>
Check out é o processo de carregar um commit do repositório

### Diretório de trabalho
Este é o diretório git no qual você está trabalhando. Quando você faz check-out de um commit, todo o seu diretório com todos os arquivos é alterado/substituído para corresponder a esse commit (exceto arquivos ignorados) .

### Estágio OU Índice
O Índice é o próximo commit proposto. É um buffer antes do commit real. É basicamente uma plataforma de carregamento onde você determina quais alterações serão enviadas. Como o diretório de trabalho e o que é salvo pelo Git são essencialmente dissociados, isso permite ao desenvolvedor construir seus commits da maneira que desejar. Você pode até preparar uma única linha individual de suas muitas alterações e apenas confirmá-la.

