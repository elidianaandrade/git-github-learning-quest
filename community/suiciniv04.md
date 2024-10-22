
# Dio resumos GIT

# Autor: SUICINIV04    

# Contribuição feita para o curso de Git e Github da DIO


## Documentação 
- 😎
- 
<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1>

## Visão Geral do Curso e Ferramentas

### Sistemas de Controle de Versão
Os Sistemas de Controle de Versão (Version Control System - VCS), são softwares que controlam as versões de um arquivo ao longo do tempo. 
<table>
  <thead>
    <tr align="left">
      <th>Sistemas</th>
      <th>Descrição</th>
      <th>Exemplos</th>
    </tr>
  </thead>
  <tbody align="left">
    <tr>
      <td>Centralizado (CVCS)</td>
      <td>Um único servidor dispõe dos arquivos de controle de versão.</td>
      <td align="center">
          <img align="center" alt="CVS" src="https://img.shields.io/badge/CVS-000?style=for-the-badge&logo=cvs">
          <img align="center" alt="Subversion" src="https://img.shields.io/badge/Subversion-000?style=for-the-badge&logo=subversion">
      </td>
    </tr>
    <tr>
      <td>Distribuído (DVCS)</td>
      <td>Duplica localmente o repositório completo, incluindo o histórico de versões.</td>
      <td align="center">
          <img align="center" alt="Git" src="https://img.shields.io/badge/Git-000?style=for-the-badge&logo=git">
          <img align="center" alt="Mercurial" src="https://img.shields.io/badge/Mercurial-000?style=for-the-badge&logo=mercurial">
      </td>    
    </tr>
  </tbody>
  <tfoot></tfoot>
</table>

### Git
Sistema de Controle de Versão Distribuído.

<div>
    <img align="center" width="100px" src="https://user-images.githubusercontent.com/97471199/230219597-961612d8-c2a4-4a76-80c8-391e54c056b6.png">
</div>

### GitHub
Plataforma de hospedagem de código para controle de versão com Git, e colaboração.

##
<div align="center">Feito com 💙 por <a href="https://github.com/elidianaandrade">Eli</a>.</div>



<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1>

## Instalação, Configuração e Autenticação	

### Instalando o Git no Windows
- Acesse < https://git-scm.com/download/win >;
- Faça o download do instalador e execute;
- Aceite a licença e clique em “Next”, e siga configurando como desejar¹ e clicando em “Next”;
- Finalize clicando em “Install”, e “Finish”.

¹Em "Select Components“, deixe as opções “Git Bash Here” e “Git GUI Here” marcadas.

##

### Instalando o Git no Linux (Ubuntu)
- Confira a doc.: < https://git-scm.com/download/linux >;
- Instale a última versão estável do Git:
    ```bash
    # add-apt-repository ppa:git-core/ppa
    ```
    ```bash
    # apt update
    ```
    ```bash
    # apt install git
    ```
##

### Instalando o Git no macOS
- Confira a doc.: < https://git-scm.com/download/mac>;
- Instale o Homebrew: < https://brew.sh/ >;
- Instale o Git:
    ```
    $ brew install git
    ```
##

### Configurando o Git
```bash
$ git config --list
```

#### Configurando seu nome de usuário e e-mail (globalmente):
```bash
$ git config --global user.name "Nome Sobrenome"
$ git config --global user.email seuemail@email.com
```
#### Configurando o nome da Branch Padrão:
```bash
$ git config --global init.defaultBranch main
```

##
<div align="center">Feito com 💙 por <a href="https://github.com/elidianaandrade">Eli</a>.</div>


<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1>

## Primeiros Passos com Git e GitHub

### Criando e Clonando Repositórios
Existem duas formas de obter um repositório Git na sua máquina:
1. Transformando um diretório local que não está sob controle de versão, num repositório Git;
2. Clonando um repositório Git existente.

#### Criando um Repositório Local
Acesse a pasta que deseja transformar em um repositório Git  pelo terminal ou clique no atalho em “Git Bash Here”:
1. Inicialize um repositório Git no diretório escolhido:
    ```bash
    $ git init
    ```
2. Conecte o repositório local com o repositório remoto:
    ```bash
    $ git remote add origin https://github.com/username/nome-do-repositorio.git
    ```
##

### Desfazendo Alterações no Repositório Local

#### Como alterar a mensagem do último commit
```bash
$ git commit --amend
```
Alterando a mensagem sem abrir o editor:  
```bash
$ git commit --amend –m"nova mensagem"
```

#### Como desfazer um commit
```bash
$ git reset
```
```bash
$ git reset --soft
```
```bash
$ git reset --mixed
```
```bash
$ git reset --hard
```

##
<div align="center">Feito com 💙 por <a href="https://github.com/elidianaandrade">Eli</a>.</div>

<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1>

## Dicas e Materiais de Apoio

### Git Aliases: Adicionando apelidos para os comandos do Git
Exemplo: Criando um alias para o comando `status`:  
```bash
$ git config --global alias.st status
```  
Agora podemos utilizar o comando  `git st` para acionar o  `git status`.
<br>
Para remover o alias que criamos, utilizamos o seguinte comando:
```bash
$ git config --global --unset alias.st
```

### Para saber mais
- Tech Talk: Linus Torvalds on git: [https://youtu.be/4XpnKHJAok8](https://youtu.be/4XpnKHJAok8)
- ProGit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
- GitFluence: [https://gitfluence.com/](https://gitfluence.com/)
- GitIgnore: [https://www.toptal.com/developers/gitignore/](https://www.toptal.com/developers/gitignore/)
- Chocolatey: [https://community.chocolatey.org/packages/git](https://community.chocolatey.org/packages/git)
- Markdown: [https://docs.github.com/pt/get-started/writing-on-github](https://docs.github.com/pt/get-started/writing-on-github)
- My Octocat: [https://myoctocat.com/](https://myoctocat.com/)
- GitHub Desktop: [https://desktop.github.com/](https://desktop.github.com/)
- GitHub Pages: [https://docs.github.com/en/pages/getting-started-with-github-pages](https://docs.github.com/en/pages/getting-started-with-github-pages)

##
<div align="center">Feito com 💙 por <a href="https://github.com/suiciniv04">Eli</a>.</div>




