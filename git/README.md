# Git 

#### Index
###### Clonar um repositório
###### Fazer um commit
###### Criar uma branch
###### Fazer um commit nessa nova branch
###### Após as mudanças em paralelo na mesma branch, resolver um 
conflito após um pull
###### Fazer um amend no commit anterior 
###### Alterar a mensagem de commits anteriores
###### Reverter um commit
###### Resetar um commit
###### Colocar as mudanças em stash, depois aplicar essas mudanças em 
outro branch
###### Pegar (cherry pick) um commit específico de um branch para outro
###### Fazer um merge de dois branchs
<br/>

__Clonar um repositório__
```bash
$ git clone colar url (http:// ou ssh) 
```

__Fazer um `commit`__
```bash
$ git add . && git commit -m"msg"
```

 __Criar uma `branch`__
Se tiver alterações, fazer primeiro o commit.
```bash
  $ git checkout nome_branch_atual -b nome_novo_branch
```

  __Fazer um `commit` nessa nova `branch`__
```bash
$ git add . && git commit -m"Mensagem"
```

__Após as mudanças em paralelo na mesma branch, resolver um conflito 
após um `pull`__
```txt
No vscode mostra o código atual e o novo código, eu resolvo pela ide e 
depois faço um commit.
```

__Fazer um `amend` no `commit` anterior__(emendar dois commits)
```bash
"Os arquivos que serão adicionados, modificados ou excluídos devem estar 
na stage area para ser emendado no novo commit anterior"
$ git commit -m "mensagem desejada"
$ git add "arquivos ou "." para adicionar todos"
$ git commit --amend
```
__Alterar a mensagem de  commits anteriores__
```bash
$ git rebase -i head~n 
"Alterar de pick para reword as mensagens que devem receber alterações, 
salvar, Fazer as alterações e salvar novamente. n= numero de comites que 
irão aparecer para recer as alterações, Para subir as alterações"
$ git push --force
"Se aparecer a msg (fatal: Needed a single revision) é pq só tem um 
commit, usar o comando"
$ git rebase -i --root
```
__Reverter um `commit`__
```bash
$ git  revert HEAD~n "n é igual a quantidade de commits que serão 
desfeitos, se tiver 10 commits, segue o padrão de pilha começando pelo 
0. Se n for = 3 serão desfeitos os commits 10, 9, 8, 7."
```

__Resetar um commit__ *(Esse comando deve ser usado com cuidado!)*
Ex: Se tiver 10 commits e você escolher a numeração 5 do commit, do 6° 
em diante vai ser excluído 
```bash
$ git log --oneline 
"Vai aparecer todos os commits e suas numerações."
$ git reset --head "numeração desejada."
```
__Colocar as mudanças em `stash`, depois aplicar essas mudanças em outro 
`branch`__
Na branch atual, digamos (master) 
```bash
$ git add . 
$ git stash 
$ git stash branch dev "vai passar a stage area da master para a dev"
```
__Pegar (`cherry pick`) um `commit` específico de um `branch` para 
outro__
```bash
$ git log --oneline
$ git checkout master
$ git cherry-pick "numero do commit da branch anterior"
```
__Fazer um `merge` de dois `branchs`__
Digamos que o branch atual seja o (master) e vai receber os códigos do  
branch (dev) 

```bash
$ git merge dev
``` 

