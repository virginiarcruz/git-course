# Git na vida real - Willian Justen
## Anotações do Curso


[Link do template utilizado](https://html5up.net/big-picture)

* Tudo será feito com o Visual Studio Code
* Clicar no icone de iniciar o repositório e para commitar também há o botão de commit


## Criar commits atômicos

* Durante todo o processo criar pequenos commits para que se for necessário voltar a modificação não afetará muito o código.


## Boas práticas

* Sempre criar commits em inglês para que qualquer pessoa possa ver
* Usar verbos no imperativo, ou seja, add, change, remove


## Branchs

* Para criar novas branchs posso ir no botão inferior esquerdo onde há nome da branch atual, ou pressionar `ctrl + shift + p`, digitar git branch e escolher o que quer fazer.

## Subir um repositorio local par ao git.

* Adicionar o plugin - **Git Add Remote**
* `ctrl + shift + p` - e o comando git remote para adicionar o repositório.
    - origin
    - link do repositório e ele fará a sincronização com o repositório criado no git.


* Para ver as modificações realizadas adicionar o pluign - **Git History**
    - `ctrl + shift + p` - git view history para ver a árvore com as modificações em todas as branchs


## Merge e Rebase

* **Merge** - Quando faço modificações em diferentes branchs e faço um merge entre elas, é criado um commit a mais com o merge. Cria commits extrar. 
     - Se você já terminou sua feature e você quer jogar pro master, é ideal que use o merge. O commit a mais que ele cria ele documenta exatamente o momento que um bug foi ou não introduzido. Fica no log.

* **Rebase** - Se eu quero só atualizar minha branch com a master eu uso o `pull rebase`
    - O Rebase vai pegar as atualizações da minha branch com a que eu setei como upstrem. Aqui disse que quero deixar ela atualizada com a origin master. 
    - Não vai fazer nenhum commit a mais.
         
          git branch --set-upstream-to=origin/master redesign-navrebase
    
    - Vai ser útil para evitar commits sujos e a ramificação no histórico dos commits.


## Git Blame

- Avisa o autor e o commit naquela mudança de código.


## Stash

- Pra salvar as mudanças antes de um commit. Salvo as mudanças num stash e depois volto a editar aquele stash.
