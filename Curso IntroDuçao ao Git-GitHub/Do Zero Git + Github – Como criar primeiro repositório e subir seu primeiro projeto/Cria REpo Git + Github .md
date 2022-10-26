### Sim, Git e Github são coisas diferentes, que trabalham juntas para tornar nosso código e projetos possíveis de serem versionados e compartilhados.

Pra começar, Git e Github são sim coisas diferentes. Porém, trabalham juntos no propósito de tornar nosso código e projetos possíveis de serem versionados e compartilhados.

Na minha pequena experiência de Deva Java, digo pra você que: GitHub é apenas uma das opções de “onde armazenar” as diversas versões do seu projeto/código. Outros serviços muito utilizados, especialmente nas empresas, são o Bitbucket, GitLab e Azure (Microsoft).

Já o Git, que é a ferramenta para “versionar” nosso código (que basicamente funciona como um “backup” de cada versão e que permite que você consiga voltar atrás quando fizer alguma grande besteira), é uma unanimidade: todo mundo usa!

> *É importante salientar que esse post não tem a intenção de ensinar os conceitos sobre Git, nem tampouco ser um tutorial para trabalho em equipes com o Git, utilizando de conceitos como branches, merges, rebases e etc. Aqui, só queremos garantir que alguém que nunca utilizou a ferramenta consiga publicar as alterações em seu código no GitHub, utilizando os comandos mais triviais – e que não deixam de ser, também, os mais usados no dia a dia, como git add, git commit e git push.*

 

#### Instalação do Git

Como pré requisito, precisamos ter instalado o Git na nossa máquina. Para cada sistema operacional há uma forma de instalar.

Confesso que, desde que iniciei a jornada me tornar desenvolvedora, migrei para o linux (Ubuntu) e faço muito uso da linha de comando (terminal). Parece mais difícil num primeiro momento, mas acho que facilita muito para diversas instalações e coisas que devemos utilizar como dev no dia a dia.

Aqui tem o [site oficial](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) com as formas de instalar em cada SO. Para quem usa Windows, uma opção é utilizar o client do GitHub para desktop -> [GitHub Desktop](https://desktop.github.com/). Outra opção, também, é utilizar uma IDE (Integrated Development Environment – que basicamente é um softfware que vai te facilitar a desenvolver softwares :D). Como exemplos podemos citar o IntelliJ, que já vem com o Git instalado por padrão, ou o Eclipse, no qual podemos adicionar o plugin Egit.

Se você está, como eu, utilizando Linux, o processo é bem simples. Basta um comando no terminal e tcharamm…

*sudo apt install git-all*

Para conferir se a instalação foi sucesso, digite:

*git –version*

Se aparecer algo semelhante ao abaixo é porque está tudo certo e já podemos começar.

*git version 2.25.1*

 

#### Criar conta e repositório no GitHub

O GitHub é um serviço que vai armazenar nossos projetos e nos auxiliar a gerenciá-los. É uma excelente vitrine para expor nossos trabalhos e estudos.

A primeira etapa é criar uma conta no GitHub, que é um cadastro básico como em qualquer site ou serviço. Na página inicial você deve preencher seus dados, escolhendo um username (que será sua identificação no site), colocando seu e-mail e escolhendo uma senha.

Depois disso, vamos criar nosso primeiro repositório: o local para expor nossa arte!

Agora, é preciso preencher o nome do novo repositório e colocar uma breve descrição (não é obrigatório, mas dá um tom de organização, né?!). O restante das opções eu geralmente deixo o padrão que está: public e desmarcado para criação do README e do learning lab.

Quando você clicar em “Create repository”, vem a chave para nosso primeiro teste: todos os comandos que precisamos executar em nosso PC para conseguir “subir” nosso primeiro arquivo! Segura esses comandos aí que, já já, vamos precisar deles.

![.](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-1.gif)

#### Criar projeto básico Spring Initializr

Uma forma de criar um projetinho mais próximo da vida real para subir em nosso repositório, é utilizar o [Spring Initializr](https://start.spring.io/), que pode gerar um pacote já com toda a estrutura de um projeto Java.
Mas, para enviar ao GitHub utilizando o Git, podemos usar qualquer projeto ou conjunto de arquivos. Vamos criar o projeto com as seguintes definições:

- Em “Project”: “Maven Project”; Em “Language”: “Java”; Em “Spring Boot”: A versão que já vier marcada;
- Em “Project Metadata”: Eu preencho assim: “Group”: “com.isagiongo”; “Artifact”: “basic-git”; “Name”: “basic-git”; “Description”: “Testing Git”; “Package name”: “com.isagiongo.basic-git”;
- Em “Packaging”: “Jar”; Em “Java”: “8”; (não precisa selecionar nenhuma dependência no momento). Agora basta clicar em Generate que o site vai baixar nossa base de projeto em um arquivo compactado.
- 
- ![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-2.gif)

Descompacte esse arquivo em seu diretório(pasta) de projetos-java, por exemplo. Acesse a pasta que você acabou de descompactar. Você deve conseguir ver pelo menos o seguinte lá dentro:

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-3.png)

#### Comandos para inicializar nosso repositório e subir nosso projeto para o GitHub

Agora vem a hora de utilizar aqueles comandos que o GitHub nos passou assim que criamos nosso repositório (para uma lista mais completa de comandos do Git, dá uma olhada [aqui](https://woliveiras.com.br/posts/comandos-mais-utilizados-no-git/).

Uma coisa importante para entender o que os comandos abaixo estão fazendo, é dar uma olhada nas “áreas” que o Git gerencia pra gente, e o fluxo que nossas alterações percorrem até chegar lá no nosso repositório no GitHub. A imagem abaixo ilustra isso.

Quando utilizamos “git add”, enviamos o arquivo para o “staging area” (área de preparo), que significa que ele está sendo preparado para entrar na próxima revisão do repositório. São as coisas que vão entrar no próximo commit.

Ao executar “git commit”, vamos pegar tudo que foi enviado com git add ao staging área e “tirar uma foto” do estado atual do projeto e registrar isso no nosso repositório local.

E, por fim, o comando “git push”, vai enviar essas alterações commitadas para o repositório remoto.

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-4.png)

Estando dentro da pasta do seu projeto, vamos digitar os seguintes comandos:

- o comando echo está “enviando” (>>) o conteúdo que está entre aspas duplas para o arquivo README.md (para saber mais sobre a função do README e como montar um bem legal olha esse artigo.

*echo “# Project Basic Git” >> README.md*

- o comando git init está criando um novo repositório do git

*git init*

- como já tínhamos arquivos dentro da nossa pasta, fizemos um pouco diferente do indicado nos comandos do GitHub. O comando git add . adiciona todo o conteúdo do atual diretório à área de index do Git ([para saber mais](https://rogerdudler.github.io/git-guide/index.pt_BR.html))

*git add .*

- o comando seguinte, vai confirmar que queremos adicionar essas mudanças, e sempre vamos colocar dentro de aspas duplas uma mensagem que explique o que esse commit está fazendo, o que ele está adicionando. É importante que a mensagem de commit realmente seja explicativa em relação às alterações que foram feitas.

*git commit -m “Enviando primeiro projeto ao GitHub”*

- Depois disso, vamos nos conectar ao nosso servidor remoto, ao nosso repositório do GitHub

*git remote add origin https://github.com/isagiongo-tutorial/basic-git.git*

- E, por fim, enviar essas alterações lá para o nosso repositório do GitHub

*git push -u origin master*

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-5.gif)

**Pronto! Nosso projeto já está na nossa página do GitHub!**

Só para fazer um teste, vamos editar nosso arquivo de README, acrescentando algumas informações para comprovar que o Git está mesmo “monitorando” nossas alterações. E, claro, vamos novamente enviar o que alteramos em nosso projeto para nosso repositório remoto.

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-6.gif)

Se nenhum arquivo de nosso projeto tiver sido alterado, ao executar o comando git status, temos como resultado:

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-7.png)

Isso nos informa que estamos trabalhando na branch master (assunto para próximos posts) e que estamos atualizados em relação ao que está no nosso repositório remoto (no GitHub). E nos informa também que, não temos nada a commitar, pois não acrescentamos nenhuma alteração.

Agora vamos alterar e salvar o arquivo README, acrescentando qualquer informação. Após isso, vamos testar o comando git status novamente.

Agora sim, temos a informação de que um arquivo foi modificado e que temos o que commitar.

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-8.png)

E assim faremos! Vamos adicionar o arquivo com git add README.md, commitar informando uma mensagem do que alteramos com git commit -m “mensagem” e enviar ao repositório remoto no GitHub com o comando git push.

![](C:\Users\Kevin Guasti\Documents\Desafios de Projeto DIO\Desafio Git-GitHUb\dio-desafio-github-primeiro-repositorio\Curso IntroDuçao ao Git-GitHub\Do Zero Git + Github – Como criar primeiro repositório e subir seu primeiro projeto\IMAGEM-9.gif)

E essa é a rotina básica de uso do Git! Toda vez que fizermos algum acréscimo ou alteração em nosso projeto, podemos adicionar e submeter essas alterações ao nosso repositório!

Abaixo, alguns links interessantes e úteis para você aprender mais:

- [Curso grátis na Udemy sobre Git e GitHub básico](https://www.udemy.com/course/git-e-github-para-iniciantes/) – em português.
- [Para aprender mais sobre branches no git interativamente](https://learngitbranching.js.org/?locale=pt_BR) – em português.
- [App desktop para aprender na prática sobre Git](https://github.com/jlord/git-it-electron#what-to-install) – em inglês.
- [Acha que fez m*&¨% e não sabe como resolver? Aqui tem a resposta! 😀](https://ohshitgit.com/pt_BR) – em português.
