
# Comandos Git

Aqui irei listar vários comandos GIT.

Conecte-se no LinkedIn:
[!LinkedIn](https://img.shields.io/badge/LinkedIn-000?style=for-the-badge&logoColor=0E76A8)](https://linkedin.com/in/andre-lucas-silva-freires)



## GIT CLONE:
Trazer um repositório remoto para uma pasta local,
ex:
'git clone url_do_repositorio'
'git clone https://github.com/nomeusuarioexemplo/repo/remoto.git'

desta forma acima, todas as branchs serão baixadas na sua máquina.

Porém, se você quiser baixar apenas uma branch em especifico, faça isto:
'git clone https://github.com/nomeusuarioexemplo/repo/remoto.git --branch teste --single-branch'  --> teste é o nome da branch











## GIT INIT
diz que a pasta local será um repositório,

exemplo -> navegue até a pasta que deseja, e em seguida digite o comando 'git init':
cmd:

c:\arquivos.
















## GIT ADD
o comando GIT ADD adiciona arquivos para serem commitados em determinada branch do repositório.

veja os passos:
1. dar o comando GIT INIT na pasta que se deseja fazer um repositório.
2. criar/alterar algum arquivo existente na pasta local do repositório e em seguida dar o comando GIT ADD *nome_do_arquivo*
ex: git add index.html
ou 
GIT ADD . (para adicionar todos os arquivos alterados)

## GIT RM
o comando GIT RM remove arquivos para nao serem comitados em determinado branch do repositório.
veja os passos:
1. digitar o comando GIT RM *nome_do_arquivo* ex: GIT RM INDEX.HTML
2. digitar o comando GIT RM -f *nome_do_arquivo* para remover o arquivo do repositório local.















## GIT COMMIT
o comando GIT COMMIT serve para especificar que os arquivos que foram adicionados através do GIT ADD são de fato os arquivos que serão enviados
ex: git commit -m 'mensagem informando o que foi mexido'














## GIT RESET

Neste comando você deve passar o parâmetro do hash do commit que você deseja restaurar até ele, ou seja, commits posteriores a este comando serão desfeitos, 
ficando apenas a alteração, na área de preparação.

soft:
Pega os arquivos/alterações que estavam nos commits posteriores que a gente indicou o hash e adiciona esses arquivos/alterações na área de preparação.
(retorna, como se você só tivesse digitado 'git add .', ou seja, ele desfaz o comando 'git commit')

soft -> ex:
git reset --soft 519b1f8eb8cfb6f71678b44c1a2887e84b4b638a


mixed:
Pega os arquivos/alterações que estavam nos commits posteriores que indicamos o hash, e adiciona esses arquivos/alterações, como se não tivéssemos nem 
digitado o comando 'git add .'

mixed -> ex:
git reset --mixed 519b1f8eb8cfb6f71678b44c1a2887e84b4b638a


hard:
Desfaz completamente os arquivos/alterações que estavam nos commits posteriores que indicamos o hash, como se nunca tivéssemos digitado.

hard -> ex:
git reset --mixed 519b1f8eb8cfb6f71678b44c1a2887e84b4b638a

outras forma de utilizar o 'git reset'

'git reset resumos/aula-01.md', ele irá deixar o arquivo 'aula-01.md' na área de preparação.

e 

git restore --staged resumos/aula-02.md













## GIT STATUS
se ainda o commit nao foi feito, entao basta dar um comando ex: git checkout --index.html














## GIT REMOTE 
-v: verifica se há repositório de núvem conectado ao repositório local
add origin {url} : a url é o endereco do repositório em núvem.















## GIT PULL
traz os dados do repositório do  remoto para o repositório local.

obs : Esse comando é a soma do 'git fetch' mais o 'git merge' do mesmo nome da branch remota e local















## GIT FETCH 
(caso seja modificado algum arquivo na branch master no repositório remoto, o git fetch sinaliza isso no repositório local)
o fetch informa se a branch está atualizada ou não. ele não atualiza imediatamente, ele apenas sincroniza e prepara
Agora pode-se utilizar o GIT MERGE para realmente atualizar a branch master local.
'Apenas baixa o conteúdo da branch remota, sem mesclar com a branch remota'

ex:
git fetch origin main

para vermos as diferenças:
git diff main origin/main

ex para unirmos:
git checkout main
git merge origin/main














## GIT LOG 
é um comando que permite ver o histórico de commits feitos ao longo da vida da branch.














## GIT REFLOG
log mais detalhado.














## GIT COMMIT --AMEND
git commit --amend -m "primeira interação"
Altera a última descrição de commit.














## GIT TAG
é um comando que permite criar marcações ou tags (RELEASES no GitHub)
ex: Você faz o commit e após o commit você pode adicionar o comando git tag 'versao' --substitua 'versao' por um número ex: 1.1
ex: GIT TAG 1.1 
e após isso você deve usar o comando GIT PUSH --TAGS














## GIT BRANCH
comando que cria um novo ramo para que as modificações fiquem apenas nesta nova branch, ou lista, ou deleta.
Antes de fazer as modificações, crie a branch, e depois altere o branch atual para a branch que foi criada.
1. para listar as branch's existentes, digite o comando: git branch
2. para deletar alguma branch, digite o comando: git branch -D 'nome_branch' ex: git branch -D feature/modificacao_arquivo_index22
3. para criar uma nova branch:
ex: git branch feature/modificacao_arquivo_index22  --ou seja, depois das palavras git branch, o que vem é o nome da branch.

'feature/' é como se fosse uma pasta, um diretório.
o nome completo da branch é 'feature/modificacao_arquivo_index22'

outra forma de criar uma branch é :
faça o checkout para a branch que você deseja usar como base:
1. 'git checkout master'.
2. 'git checkout -b nome_nova_branch'
agora só fazer as modificações.














## GIT CHECKOUT 
comando para receber branch's do servidor e pra atualizar branch's localmente 
digite o git checkout para alterar a branch atual para a branch que vai receber as modificações.
ex: git checkout feature/novabranch
e então você pode alterar o(s) seu(s) arquivo(s) 
e depois dar um git add .
e depois fazer o commit: git commit -m 'mensagem'
e depois git push.
assim, será salvo todas essas modificações na branch setada.














## GIT MERGE
Une duas branchs.
o ideal é alterar a branch atual para a branch master e depois fazer o comando git checkout master (ou seja, mudar para a branch master
ex: 
git checkout master
git merge 'nome_branch_feature'
pronto, já estão juntas as duas branchs, ou seja, trouxemos a branch 'nome_branch_feature' para a branch master.













## GIT STASH
Este comando guarda ou arquiva as suas alterações, para você poder usar depois.

'git stash list' você consegue lista-las.


'git stash pop' -> para trazer as alterações para a sua branch e excluir essas alterações.
ou
'git stash apply' para manter na lista essas modificações.

