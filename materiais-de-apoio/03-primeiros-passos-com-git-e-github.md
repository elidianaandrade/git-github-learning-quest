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
O Git oferece várias maneiras de desfazer um commit, dependendo de como você quer manipular o histórico.

- Reseta o último commit mantendo as mudanças na área de preparação:
 
```bash
$ git reset --soft
```

- Reseta o último commit e move as mudanças para a área de trabalho:

```bash
$ git reset --mixed
```

- Remove completamente o commit e as mudanças associadas:

```bash
$ git reset --hard
```

##
<div align="center">Feito com 💙 por <a href="https://github.com/elidianaandrade">Eli</a>.</div>
