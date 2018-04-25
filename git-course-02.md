# Git na vida real - Willian Justen
## Anotações do Curso


## Comandos do cotidiano

* Subi algo errado, como reverto?

    1. git revert - reverte um commit, é como se fizesse um ctrl + z
        - `git log` - para ver o commit que quero reverter
        - `git reverse` e a hash
        - se tiver tudo certo: `:wq` pra criar o commit revertendo.
        - `git push origin master` para enviar
    
    2. uma forma que não é uma boa prática porque muda todo o histórico, pra você e para o time. Ele retorna ao hash tiver marcado. Serve pra evitar que tenha commits sujos.
        - `git reset` - posso passar 2 parametros
            - `--hard` - reseta tudo, volta pro commit que quero, apagando tudo o que foi feito.
            - `--soft` - não reseta tudo, volta para o anterior
        
        - é bom para branchs separados e o revert serve para a master.

* Como editar o último commit

    - `git commit --amend` - edito o que eu quero e `:wq` pra salvar
    - só vai ser útil se não tiver enviado pro repositório remoto com o push.


* Como pegar um commit específico de um branch e colocar no meu
    - faço checkout na branch que quero pegar
    - git log e copio a hash do commit que quero copiar
    - vou pra minha branch
    - `git cherry-pick` + o hash

