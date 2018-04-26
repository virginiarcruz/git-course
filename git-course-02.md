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


## Para atualização de conteúdo

- Para separar os conteúdos de um commit
    - `git add -p`
    - ele vai abrir para mim o menu para que eu possa decidir se eu quero ou não adicionar tais pedaços e ele mostra da mudanças realizadas então você tem as opções:
        - Y - adicionar
        - N - não add
        - Q - não adicione e saia imediatamente desse menu.
        - A - adiciona esse e todos os outros que vierem 
        - D - funciona igual ao Q não adiciono esse e nem os outros mas não sai
        - J - passar o hank e definir o próximo
        - G - passa esse e ver o anteior
        - S - divide em partes menores
        - E - para editar manualmente

## Juntando commits com Squash

- Quando criamos uma feature e criamos vários commits, e então queremos juntar os commits criando um commit só com a aquela feature

    1. vou para o commit que eu quero. No caso o Head-2 é porque eu quero ir para o segundo commit abaixo do HEAD que ele está.
            
            `git rebase -i HEAD~2`

    - squash é o que utilizo para juntar com o comando anterior.
    - aperto i para editar no VIM, deixo o primeiro como pick e o segundo como squash que é pra juntar
    `esc:wq` - para salvar e digito a mensagem e salvo.
## Juntando commits com fixup e autosquash

