Passos para utilização do GITHUB com o VSCode

1. O Git já tem que estar instalado no computador (https://git-scm.com/)
2. Verificar se o caminho (path), está configurado nas 'Variáveis de ambiente do windows' -> 'variáveis do sistema' -> 'path' -> tem que ter: C:\Program Files\Git\cmd
3. Criar o repositório no Github
4. No VSCode, na pasta do projeto, abrir o terminal e rodar o comando: git init
5. Para 'empacotar' um arquivo a ser enviado para o repositorio do Github: git add NOME_DO_ARQUIVO
5a. Para 'empacotar' todos os arquivos do projeto de uma só vez para serem enviados para o repositório: git add .
6. Para vincular a conta Github ao VSCode via Git: git config --global user.email "rigueira@gmail.com"
6a. Para vincular a conta Github ao VSCode via Git: git config --global user.name "Andre Rigueira"
7. Para 'preparar' o pacote no Github fazendo o versionamento: git commit -m "Projeto inicial. primeiro commit"
8. Para criar a ramificação do projeto (branch): git branch -M main
9. Para vincular o diretório local com o repositório de destino dos arquivos no Github, é mais seguro usar o SSH: git remote add origin git@github.com:AndreRigueira/aula_github.git
10. Para configurar a segurança pro uso do SSH, é preciso ir no Github --> settings --> SSH and GPG keys --> e criar uma nova
Para saber como criar a chave SSH: https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
11. comando para criar a chave SSH: ssh-keygen -t ed25519 -C "rigueira@gmail.com"
Essa Chave Pública fica armazenada em c:\usuarios\Rigueira\.ssh\id_ed25519.pub
12. Para efetivamente enviar (sincronizar) os arquivos, conforme as orientações anteriores: git push -u origin main



Sequência:
> git init
> git add .
> git commit -m "projeto inicial"
> git remote add origin git@github.com:SEU_USUARIO/SEU_REPOSITORIO
> git push -u origin main
