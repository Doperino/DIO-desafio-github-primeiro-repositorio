# Anotações sobre o conteúdo visto nas aulas de Git/Github :computer:



#### - Introdução ao Git/Github

Um projeto pode ter diversas versões de um mesmo código, uma vez que toda alteração deve ser armazenada e mapeada, para controle do que é adicionado ou removido. Esse fator é cumulativo. Para projetos muito extensos, ocupa muito espaço na **workspace** e pode apresentar uma **cronologia confusa** e possíveis **conflitos de formatos**.  

O Git soluciona problemas como esses, apresentando um eficiente **versionamento de código**, controlando as mudanças feitas e informando conflitos que surgem devido a sua capacidade de **compartilhamento**, com cópias do mesmo código em diferentes computadores de diferentes usuários que podem mudar uma mesma linha ao mesmo tempo.

O github é introduzido nesse tema pois é por meio dele que o código é armazenado na nuvem, no servidor. Por meio dessa conexão entre as plataformas, a segurança e integridade do código é assegurada por algoritmos de criptografia. Esse conjunto de fatores torna o time Git/Github um _**eficiente método de versionamento de código, compartilhamento, armazenamento e segurança.**_ 

Referente a segurança, vale ressaltar que cada alteração gera um novo código de criptografia do tipo SHA1, que é o identificador da alteração. Dessa forma, entende-se que nada passa batido sem que seja devidamente registrado, tendo por trás um responsável que também tem a identificação da sua Workspace identificada.

_(**Útil para encontrar responsáveis pelas mudanças e por possíveis problemas**)_



#### - Sequência de comandos 

- Gerando chave SSH:

1. ssh-keygen -t ed25519 -c (insira aqui o seu e-mail) **gerando a chave SSH**

2. No [github](https://github.com/), em **Settings - SSH and GPG keys**, após clicar em **New SSH key**, escolha o título da sua chave e insira em **key** a chave gerada no Git.
3. eval $(ssh-agent -s) **Criar um agent**
4. ssh-add id_ed25519 **Dar a chave para o agent**



**Obs:** não se esqueça de ativar o **Two-Factor Authentication** em **Password and authentication** para que seja possível realizar **commits** posteriormente. 



- Dando vida ao seu repositório pela Linha de Comandos

1. git init **(criar/iniciar o repositório)**
2. git add * **(move todos os arquivos que estão "untracked", "unmodified" ou "modified" para staged)**
3. git commit -m "(descrição aqui)" **faz o commit do seu repositório**
4. git remote add origin (inserir aqui o https do github) **aqui, você conecta remotamente o seu diretório da sua workspace com o seu repositório criado no github**
5. git push origin master **upa as mudanças no diretório associado do github**



**Obs:** caso seja a primeira vez realizando esse processo, é necessário configurar o Git com seus dados do Github:

git config --global user.email "(insira aqui o seu e-mail)"
git config --global user.name (Insira aqui o seu nome Github)



**Alerta:** esse guia apresenta as anotações que eu fiz enquanto realizava o curso, por isso, não traz integralmente tudo o que foi feito, de forma que possa ser utilizado perfeitamente por terceiros **(Por exemplo, eu não explico aqui sobre instalação do Git ou criação da conta no Github, além de outros temas como arquitetura de objetos do Git)**. Por isso, trate isso como um leve "guia" para tal. Mais informações você pode obter nos cursos da [DIO](https://www.dio.me/sign-up). 