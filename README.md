# Linux :computer:

- **Manipulação de usuários**

  **Esses comandos alteram arquivos principalmente no diretório /etc**

  - **Criando um novo usuário**

    $ adduser nome_do_user

    $ adduser -ingroup nome_do_grupo nome_do_user

    ​	_a flag **-ingroup** cria um usuário e já adiciona ele há um grupo específico_

  - **Adicionando ou alterando senha de usuário**

    $ passwd nome_do_user

  - **Deletando usuário**

    $ userdel nome_do_user

    $ userdel -r nome_do_user

    ​	_a flag **-r** remove o usuário e a pasta dele no sistema_

  - **Criando grupos para usuários**

    $ addgroup nome_do_grupo

  - **Listando os grupos que o usuário faz parte**

    $ groups nome_do_user

  - **Modificando o grupo do usuário**

    $ usermod -G nome_do_grupo nome_do_user

  - **Adicionando usuário em um grupo**

    $ addgroup nome_do_user nome_do_grupo

  - **Removendo o usuário de um grupo**

    $ gpasswd -d nome_do_user nome_do_grupo

  - **Apagando um grupo**

    $ groupdel nome_do_grupo

- **Permissões de arquivos e diretórios**

  - **Alterando permissão do proprietário**

    $ chmod u=rwx nome_do_arquivo

  - **Alterando permissão do grupo**

    $ chmod g=rwx nome_do_grupo

  - **Alterando permissão para outros usuários**

    $ chmod o=rwx nome_do_arquivo

  - **Alterando todas as permissões para todos os usuários**

    $ chmod a=rwx nome_do_arquivo

  - **Alterando o proprietário do arquivo**

    $ chown nome_do_user nome_do_arquivo

  - **Alterando o grupo do arquivo**

    $ chgrp nome_do_grupo nome_do_arquivo

    **OBS:**

    **rwx** representam as permissões, caso não queira uma ou nenhuma das permissões, basta não adicioná-las.

    o linux trata arquivos e diretórios como iguais, o que muda é que um diretório terá um **d** antes das permissões, e um arquivo terá um **-**.

    o sinal de **=** pode ser trocado pelo **+, para adicionar uma permissão** ou pelo **-, para remover uma permissão.** Isso se torna útil já que o sinal de **=** obriga o usuário a passar todas as permissões desejadas, mesmo as que o ele já tem.

- **Manipulando arquivos e diretórios**

  - **Criando uma pasta no sistema**

    $ mkdir nome_da_pasta

  - **Apagando diretórios vazios e arquivos**

    $ rmdir nome_da_pasta

  - **Criando arquivo**

    $ touch nome_do_arquivo.txt

  - **Ler o conteúdo de um arquivo**

    $ cat nome_do_arquivo

  - **Alterando o nome do arquivo**

    $ mv nome_do_arquivo novo_nome

  - **Copiando um arquivo para um diretório**

    $ cp nome_do_arquivo /caminho_do_diretorio

    ​	**ex:** cp teste.txt /home/user/diretorio/

  - **Movendo arquivos de diretórios**

    $ mv nome_do_arquivo /caminho_do_diretorio

  - **Mostrar diretório atual**

    $ pwd

    ​	_retorna o caminho em que o usuário está_

  - **Excluindo diretórios não vazios**

    $ rm -rf nome_do_diretorio

    ​	na flag **-rf** o **r** é de recursivo, isso significa que primeiro será excluído tudo 	de dentro do diretório e depois o diretório em si. 

    ​	o **f** é de **force**, significa que é para forçar a execução do comando, nesse 	caso, a remoção do diretório.