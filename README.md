# Docker - Rodar uma imagem como um container 

1. Baixe uma imagem com **docker pull**
```docker pull alancherosr/php56-oci```

2. Suba a imagem com **docker run**
```sudo docker run -d alancherosr/php56-oci ```

3. Para rodar o container mapeando um diretório na maquina hospedeira para um diretório no container e mapeando a porta 80 do container com a porta 8080 no host
```sudo docker run -d -p 8080:80 -v /home/elton/projects/sonepar/:/var/www/html/ alancherosr/php56-oci```

4. Para rodar o container mapeando um diretório na maquina hospedeira para um diretório no container e mapeando todas as portas do host para o container
```sudo docker run -d --network="host" -v /home/elton/projects/sonepar/:/var/www/html/ alancherosr/php56-oci```

Obs: Para funcionar o item 4 é preciso baixar o apache na máquina hospedeira
