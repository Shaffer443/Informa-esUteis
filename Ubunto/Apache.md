
##Removendo APACHE2


Para remover completamente o Apache2 do seu sistema Ubuntu, você pode seguir estes passos:

    1.Parar o serviço do Apache2 antes de remover o Apache2, pare o serviço:

	```sudo systemctl stop apache2```

   2.Remover o Apache2 e seus pacotes relacionados use o seguinte comando para remover o Apache2 e todos os pacotes relacionados:

	```sudo apt-get purge apache2 apache2-utils apache2-bin apache2.2-common```



Remover arquivos de configuração residuais:
Após remover os pacotes, remova quaisquer arquivos de configuração residuais:

bash

sudo apt-get autoremove
sudo apt-get autoclean

Verificar se há arquivos de configuração restantes:
Às vezes, alguns arquivos de configuração ainda podem estar presentes. Para garantir a remoção completa, você pode verificar manualmente e remover os diretórios relacionados ao Apache2:

bash

sudo rm -rf /etc/apache2
sudo rm -rf /var/www/html
sudo rm -rf /var/log/apache2

Verificar se o Apache2 foi completamente removido:
Finalmente, verifique se o Apache2 foi completamente removido:

bash

    apache2 -v

    Esse comando deve retornar um erro indicando que o comando não foi encontrado, confirmando que o Apache2 foi removido.

Aqui está um resumo dos comandos que você precisará executar:

bash

sudo systemctl stop apache2
sudo apt-get purge apache2 apache2-utils apache2-bin apache2.2-common
sudo apt-get autoremove
sudo apt-get autoclean
sudo rm -rf /etc/apache2
sudo rm -rf /var/www/html
sudo rm -rf /var/log/apache2
apache2 -v

Seguindo esses passos, o Apache2 deve ser completamente removido do seu sistema Ubuntu.
