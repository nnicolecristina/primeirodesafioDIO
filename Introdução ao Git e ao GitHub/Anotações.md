# Anotações sobre curso Git/GitHub :cat2:



Link para download do Git: https://git-scm.com/downloads

## Configurações iniciais:

- Armazena as informações no git config do sistema todo, do usuário e do projeto.
- Config global é do usuário.
- `git config --global user.name "Seu nome"`
- `git config --global user.email "seuemail@gmail.com"`
- `git config --global core.editor [comando do editor]`
- `git config user.name` (responde com o seu nome)
- `git config user.email` (responde com o seu nome)
- `git config --list` (mostra uma lista de informações do seu git)

## Inicializando um repositório

- `mkdir git-course`: para criar uma pasta
- `cd git-course/`: entrar na pasta
- `git init`: inicializa um repositório vazio
- `ls -la`: mostra todos os diretórios que tem no repositório
- `cd .git/`: entra no diretório
- `ls`: lista tudo que tem no diretório
- `cd ..`: volta 1

## Ciclo de vida dos status dos arquivos

- Untracked

  : arquivo acabou de ser adicionado, mas o git ainda não conhece dentro do repositório nenhuma versão    

  - *adiciona arquivo no git*

- Unmodified

  : existe no git, mas não tem modificação    

  - *modifica o arquivo*

- Modified

  : arquivo modificado    

  - *jogar o arquivo para área onde vai ser criada a versão*

- **Staged**: fica com todos os arquivos modificados para poder commitar

- `git status`: reporta como o repositório esta nesse momento

- `git add`: tira do modified e coloca no staged

- `git commit -m "mensagem"`: criar uma versão

## Desfazendo ações

- `git checkout [nome do arquivo]`: retorna o que o arquivo era até antes da edição
- quando o arquivo já está no staged    
  - `git reset HEAD [nome do arquivo]`: ele tira o arquivo do staged
- quando o arquivo já foi commitado    
  - `git reset --soft`: mata o commit, mas o arquivo fica no staged
  - `git reset --mixed`: mata o commit, volta o arquivo para modified
  - `git reset --hard`: ignora a existencia do commit e tudo que existe nele, mata tudo
