Passos para utilização do GITHUB com o VSCode

1. O Git já tem que estar instalado no computador (https://git-scm.com/)
2. Verificar se o caminho (path), está configurado nas 'Variáveis de ambiente do windows' -> 'variáveis do sistema' -> 'path' -> tem que ter: C:\Program Files\Git\cmd
3. Criar o repositório no Github
4. No VSCode, na pasta do projeto, abrir o terminal e rodar o comando: 
    > git init
5. Para 'empacotar' um arquivo a ser enviado para o repositorio do Github: 
    > git add NOME_DO_ARQUIVO
5a. Para 'empacotar' todos os arquivos do projeto de uma só vez para serem enviados para o repositório: 
    > git add .
6. Para vincular a conta Github ao VSCode via Git: 
    > git config --global user.email "rigueira@gmail.com"
6a. Para vincular a conta Github ao VSCode via Git: 
    > git config --global user.name "Andre Rigueira"
7. Para 'preparar' o pacote no Github fazendo o versionamento: 
    > git commit -m "Projeto inicial. primeiro commit"
8. Para criar a ramificação do projeto (branch): 
    > git branch -M main
9. Para vincular o diretório local com o repositório de destino dos arquivos no Github, criando essa caminho com um 'apelido' (no caso 'origin') é mais seguro usar o SSH: 
    > git remote add origin git@github.com:AndreRigueira/aula_github.git
10. Para configurar a segurança pro uso do SSH, é preciso ir no Github --> settings --> SSH and GPG keys --> e criar uma nova
Para saber como criar a chave SSH: https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
11. Comando para criar a chave SSH: 
    > ssh-keygen -t ed25519 -C "rigueira@gmail.com"
Essa Chave Pública fica armazenada em c:\usuarios\Rigueira\.ssh\id_ed25519.pub
12. Para efetivamente enviar (sincronizar) os arquivos, conforme as orientações anteriores: 
    > git push -u origin main

Sequência:
> git init
> git add .
> git commit -m "projeto inicial"
> git remote add origin git@github.com:SEU_USUARIO/SEU_REPOSITORIO
> git push -u origin main


Para clonar um repositório (pegar o projeto de outra pessoa):

1. Ir no Github, na pasta de repositório que se deseja clonar (puxar para o computador, para trabalhar localmente), e clicar no botão verde 'Code'
2. Na opção Clone, copiar o caminho (url) desse repositório.
3. No diretório onde se deseja clonar o repositório, clicar com o botão direito, e abrir o Terminal do windows
4. Executar o comando: 
    > git clone URL_DO_REPOSITORIO_QUE_SERA_CLONADO
Obs. o comando 'clone', já cria a conexão do repositório remoto com a pasta local, e portanto não precisa fazer o 'git remote add origin'

Para verificar como está o status do commit (se já foi feito a sincronização, ou não com o repositório do Github)
    > git status

Para verificar quais foram os commits feitos no projeto:
    > git log

Para verificar quais são os repositorios remotos que tem adicionado ao projeto:
    > git remote


BOAS PRÁTOCAS PARA AS MENSAGENS DE COMMIT

As mensagens dos commits devem ser simples e objetivas. A seguir, listamos algumas orientações para isso:

1. Mantenha a mensagem curta e concisa: A primeira linha da mensagem deve conter, no máximo, 72 caracteres. 
Caso seja necessário uma descrição adicional, você deve pular uma linha e adicionar os detalhes, como o contexto, da mudança realizada.

2. Uso de verbo no infinitivo: É comum que a mensagem do commit inicie com um verbo no infinitivo que descreva a alteração feita, 
como “adicionar”, “corrigir” ou “atualizar”. Em sequência, são adicionados detalhes concisos da mudança. Por exemplo: “Atualizar texto do título da página”.

3. Evite detalhes técnicos: Não inclua detalhes técnicos complexos na mensagem de commit. 
Esses detalhes podem ser adicionados nos comentários de código ou na documentação.

4. Um commit deve ser realizado sempre que você finalizar uma tarefa específica ou resolver algum bug. 
Isso mantém o histórico de commits claro e rastreável, de modo que seja possível entender o que foi feito em cada commit.

5. NUNCA realizar um commit de um código que você sabe que contém bugs. O ideal é que o commit contenha somente código funcional.