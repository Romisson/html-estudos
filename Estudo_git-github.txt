Git e GitHub

Para inicializar um repositório local
	-> Abra a pasta do projeto, botão direito + "Git Bash here".

Dentro do cmd do git, digite:
	-> "git init" -> Isso fará a criação de um repositório git do seu projeto.



Para visualizar se um git foi criado na sua pasta, clique no menu "Visualizar", "Mostrar", "Itens escondidos". -> Assim, você verá uma pasta ".git" indicando que um versionamento de git foi criada na sua pasta "master"

"git status" 
	Usando este comando, você verá o status da sua pasta, se houve ou não alteração nos arquivos que você deseja versionar. Geralmente aparece de vermelho os arquivos que não foi adicionados ao versionamento.

"git add <nome do arquivo"
	-> Com este comando você poderá adicionar o arquivo em questão para que ele faça parte do seu versionamento do git. 

"git add ."
	-> Com este comando você poderá adicionar todos os arquivos que você tem. Não precisa necessariamente indicar qual arquivo deseja. Com este comando fará com que todos os que não foram adicionados sejam incluídos no seu projeto.

	
Quando ele indicar no "git status" que "No commits yet" significa que nenhum commit foi criado. Quando você acessar aquele arquivo no git status e que ele está na cor verde, significa que ele foi adicionado porém ainda não foi feito commit com ele. Para isso, você precisa gerar um commit para que ele incluía no seu projeto.

"git commit -m "<nome da versão>"
	-> "git commit" é o comando para gerar um commit para que seja adicionado ao seu projetp.
	-> "-m" é o comando para que configurar uma mensagem ao seu commit. Use isso para como boa prática, 	até para conseguir compreender o que foi feito no momento da criação do seu commit.

"git commit -a -m "<nome da versão>"
	-> Desta forma fazemos uma adição dos arquivos sem precisar fazer "git add .". Assim, você adiciona todos as mudanças e faz o commit com o nome da versão que você especificar.



git config --global --list
	-> Serve para listar os usuários globais cadastrados.

git config --global user.name "<nome do usuário"
	-> Serve para cadastrar o nome do usuário global

git config --global user.email "<seu email aqui">
	-> Serve para cadastrar o email do usuário global

git config user.name "<nome>" & git config user.email "<email>"
	-> Serve para cadastrar o nome e email do usuário local.

* Subir o repositório local para o remoto
git push
	-> Ao inicializar a primeira vez, o git bash vai pedir para configurar o repositório remoto (GitHub):

$ git push
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

Para isso, vá em GitHub e abra sua conta lá. Senão tiver um repositório já criado, crie um: clicando em + e create new repositor.

Após criar, basta copiar o url e ir em git bash digitar:
	"git remote add origin <url>"

Agora que foi definido o repositório local do projeto, use o comando "git push"
Óbvio que ele não irá executar corretamente. Afinal, não definimos uma branch para onde nosso projeto será carregado. Vamos fazer isso agora. Mas antes, veja a mensagem que ele exibiu ao digitar o comando git push:
	$ git push
	fatal: The current branch master has no upstream branch.
	To push the current branch and set the remote as upstream, use

	    git push --set-upstream origin master

	To have this happen automatically for branches without a tracking
	upstream, see 'push.autoSetupRemote' in 'git help config'.

Agora, se você quer que a branch onde será enviada seja a branch master, basta digitar o código que o erro acima sugeriu: 
	git push --set-upstream origin master






