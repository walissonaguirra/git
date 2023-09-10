# Visão Geral <img src="../images/Git_icon.png" width="10%" height="10%" align="right" valign="center"/> 

Na imagem abaixo você vê quatro caixas. Um delas fica sozinho, enquanto os outros três estão agrupados no que chamarei de **Ambiente de Desenvolvimento**.

![imagem0](https://github.com/UnseenWizzard/git_training/raw/master/img/components.png)

Começaremos com caixa que está sozinha. O **Repositório Remoto** é para onde você envia suas alterações quando deseja compartilhá-las com outras pessoas e de onde você obtém as alterações. Se você já usou outros sistemas de controle de versão, não há nada de interessante nisso.

O **Ambiente de Desenvolvimento** é o que você tem em sua máquina local. As três partes são seu **Diretório de Trabalho** a **Área de Stageing** e o **Repositório Local**, Aprenderemos mais sobre elas à medida que começarmos a usar o Git.

Escolha um local onde deseja criar o seu **Ambiente de Desenvolvimento**. Basta ir até sua pasta pessoal ou onde quiser colocar seus projetos. Você não precisa criar uma nova pasta ainda.

### Obtendo um repositório remoto
Agora vamos baixa o conteúdo de um **Repositório Remoto** sua máquina local. Sugiro que usemos este repositorio https://github.com/UnseenWizzard/git_training.git.

Mas para acompanha esté post será necessário que você leve as alterações feitas em seu **Ambiente de Desenvolvimento** de volta para o **Repositorio Remoto**, e o Github não permite que alguém apenas faça isso no repositório de qualquer pessoa, então primeiro faça um fork do repositorio.

Agora que você tem uma cópia do meu **Repositório Remoto**, é hora de colocá-lo em sua máquina.

Para isso usaremos o comando:
```sh
git clone https://github.com/{YOUR USERNAME}/git_training.git
```

Como você pode ver no diagrama abaixo, isso copia o **Repositório Remoto** em dois locais, seu **Diretório de Trabalho** e o **Repositório Local**. Agora você vê como o Git é um controle de versão distribuído. O **Repositório Local** é uma cópia do Remoto e funciona exatamente como ele. A única diferença é que você não compartilha com ninguém.

O comando `git clone` deve ter criado uma pasta git_training em sua parta atual

![imagem1](https://github.com/UnseenWizzard/git_training/raw/master/img/clone.png)

