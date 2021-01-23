# Introdução ao Git e ao GitHub

Nesse curso foi apresentado um pouco da história do Git e como ele se tornou essencial para otimizar projetos dos desenvolvedores. Também conhecendo seus principais comandos, como funciona a plataforma e como ela pode simplificar o seu trabalho.

## Conteúdo abordado

* Introdução ao Git
* Navegação via command line interface e instalação
* Entendendo como Git funciona por baixo dos panos
* Primeiros comandos com Git
* Ciclo de vida do arquivo Git
* Resolvendo conflitos	

## Introdução ao Git

O Git é um sistema **específico open-source de controle de versão** criado por Linus Torvalds em 2005. De forma específica, o Git é um **sistema de controle de versões distribuído**, ou seja, toda a base de código e histórico fica disponível no computador de todos os desenvolvedores, o que permite um branching e merging simples. Segunda uma [investigação de desenvolvedores da Stack Overflow](https://insights.stackoverflow.com/survey/2018/#work-version-control), mais de 87% dos desenvolvedores usam o Git.

## Navegação via Command Line Interface e Instalação

### Comandos

* CD / - direciona para base
* CD - Entrar em uma pasta
* CD ..  Retornar para a pasta
* DIR -  Listando arquivos e pastas
* MOVE - Mover arquivos ou renomear pastas
* MAKDIR - cria diretórios
* DEL - deleta arquivos
* RMDIR /S /Q - deleta diretórios e arquivos
* CLS - limpar tela
* ECHO - printa no terminal um texto, cria arquivo com conteúdo

## Sobre Markdow

**Markdown Syntax** é uma sintaxe usada para padronizar e facilitar formatação de texto na web, utilizada em aplicativos como [Slack](https://slack.com/) e [GitHub](https://github.com/). Textos estilizados com **Markdown** são, na maioria dos casos, apenas texto com caracteres não-alfabéticos, como `#`, `\*` e `![]()`, usados para a configuração de títulos, listas, itálico, negrito e inserção de imagens.

## Entendendo como Git funciona por baixo dos panos

### Git sistema distribuído e seguro

O **GIT** também é um dos VCS mais **seguros** do mercado. Nele todo o conteúdo dos códigos, assim como a relação entre os diferentes arquivos, diretórios, versões e tags são criptograficamente protegidos por um algoritmo de hashing chamado SHA1. ... Além disso, tudo no **GIT** tem seu checksum calculado antes que seja armazenado.

### O que é SHA 1

A sigla SHA significa Secure Hash Algorithm (Algoritmo de Hash Seguro), é um conjunto de funções hash criptográficas projetadas pela Agência de Segurança Nacional dos EUA. Uma função hash gera um valor ou valores de uma sequência de texto usando uma função matemática, é uma maneira de ativar a segurança durante o processo de transmissão de uma mensagem para um destinatário específico.

### Openssl

**OpenSSL** é uma implementação de código aberto dos protocolos SSL e TLS. A biblioteca (escrita na linguagem C) implementa as funções básicas de criptografia e disponibiliza várias funções utilitárias. ... O OpenSSL é utilizado para gerar certificados de autenticação de serviços/protocolos em servidores (servers).

### Blobs

O blob (Binary Large Object - grande objeto binário) é um campo criado para o armazenamento de qualquer tipo de informações em formato binário, dentro de uma tabela de um banco de dados.

### Trees

Um objeto de árvore Git cria a hierarquia entre os arquivos em um repositório Git. Você pode usar o objeto de árvore Git para criar o relacionamento entre os diretórios e os arquivos que eles contêm. Esses pontos de extremidade permitem que você leia e grave objetos de árvore em seu banco de dados Git no GitHub.

### Commits

Um **commit** é o ato de enviar e guardar, ou seja, enviar dados ou códigos para armazenamento em um banco de dados ou em um sistema de controle de versão.		

## Primeiros comandos com Git

* GIT INIT - O comando **git init** cria um novo repositório do **Git**. Ele pode ser usado para converter um projeto existente e não versionado em um repositório do **Git** ou inicializar um novo repositório vazio.
* GIT ADD - Indexar (track) arquivo para commit, necessário toda vez que arquivo for alterado (antes do commit)
* GIT COMMIT - Realizar commit com comentário indicado.

## Ciclo de vida do arquivo Git

Os arquivos no Git sempre se encontram em algum estado: **untracked**, **unmodified**, **modified** e **stage**. Entender esses estados nos ajuda a saber melhor qual o momento certo de usar cada comando.

​			

*****************ADICIONAR IMAGEM*************

* UNTRACKED - Arquivos marcados como *untracked* são arquivos não monitorados pelo Git. Os arquivos que acabaram de ser criados sempre estarão com esse estado.
* UNMODIFIELD - Quando realizamos um commit, os arquivos saem de stage para unmodified, isso significa que, na linha do tempo, seu arquivo está igual ao estado salvo no último commit.
* MODIFIELD - São os arquivos já monitorados pelo Git que sofreram alguma alteração desde o último commit.
* STAGE - Os arquivos marcados como stage são os arquivos novos ou modificados que serão salvos no próximo commit.
* GIT STATUS - Exibir o estado atual do git.
* GIT CONFIG --LIST - Verificar Configurações.
* GIT CONFIG --GLOBAL --UNSET - Reescreve o email cadastrado
* GIT CONFIG --GLOBAL --UNSET - Reescreve o usuario cadastrado
* GIT CONFIG --GLOBAL USER.EMAIL - Adiciona email.
* GIT CONFIG --GLOBAL USER.NAME - Adiciona Usuário.
* GIT REMOTE ADD ORIGIN "LINK" - Para adicionar um novo remote, use o comando 'git remote add' no terminal, no diretório em que se repositório está armazenado.
* GIT REMOTE -V - Listar remotes atuais.
* GIT PUSH - Enviar código da branch indicada para repositório online.
* GIT PULL - Baixar alterações do repositório online para repositório local na branch indicada.
* GIT CLONE - Copiar diretório git do link de origem para diretório destino

# Resolvendo conflitos

Bem, um conflito é gerado quando duas pessoas mexem em um mesmo arquivo de código, gerando incompatibilidade com o arquivo que se encontra no repositório. 

Ex:

Eu e a Maria, que estamos na equipe GitHub, queremos mexer no código do Projeto, então puxamos para nossas máquinas o projeto que consta na Branch A. 



///////////////////////////IMAGEM--------------------------------------

Então, vamos imaginar que ambos alterem o projeto, no mesmo arquivo, e então nós duas queremos mandar o projeto com nossas mudanças para o GitHub. 

///////////////////////////IMAGEM--------------------------------------

Quando o projeto que eu mandei para o GitHub é aceito e faz merge com o projeto já existente, este agora contem as alterações que eu havia feito. Porém, o arquivo que a Maria possui, era o projeto sem minhas alterações, o projeto de cor lilás. E agora que ela fez alterações nesse projeto e tenta subir, o conflito aparece. Isso ocorre pois o projeto que está no repositório contém minhas alterações e o projeto que a Maria possui, apenas contem as alterações dela.

///////////////////////////IMAGEM--------------------------------------

### **Mas e agora? Como eu resolvo isso?**

Agora que ambas já fizeram as alterações desejadas, elas vão subir para o GitHub, na Branch A. Então, a Maria sobe o projeto dela, com as alterações dela. Agora eu vou subir o meu projeto também (git add + git commit) porém, quando tento subir para a branch, olha quem encontramos aqui: **um conflito!**

#### E então, tentaremos abrir o arquivo para consertarmos.

Quando abrirmos esse arquivo, teremos que procurar pelo erro. Sempre devemos procurar pelos sinais abaixo, já que eles indicam o erro.

///////////////////////////IMAGEM--------------------------------------

Para resolver esse conflito, poderei adicionar o parâmetro que a Maria criou na função ou apagá-lo. Então, apagarei os sinais de erro, deixando apenas a função com as correções.

Para finalizar, após as correções, iremos dar um git add, um git commit e então, um git push para mandar para o repositório remoto. E assim, resolvemos o nosso conflito!





Grupo GFT
Digital Innovation One Inc.
Otavio Reis



https://medium.com/@raullesteves/github-como-fazer-um-readme-md-bonit%C3%A3o-c85c8f154f8

lincar as imagens




