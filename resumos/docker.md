# Docker

## Versões no Windows

### Docker CE
Necessita do Windows Pro 64 bit e virtualização ativa

### Docker Toolbox:
Recomendado para casos em que os requisitos do Docker CE não foram atendidos, mais pesado que o primeiro

## Comandos úteis

### Criar/executar container ("docker pull + docker start")
```
docker run hello-word
```

### "Olá mundo"
```
docker run ubuntu echo "Olá mundo"
```

### Criar/executar container e vincular terminal atual com o do container 
```
winpty docker run -it ubuntu
```
Obs: winpty é necessário quando se está no Windows e o prompt não é o PowerShell (vide: https://stackoverflow.com/questions/48623005/docker-error-the-input-device-is-not-a-tty-if-you-are-using-mintty-try-prefi)

### Criar/executar container sem travar o terminal
```
docker run -d my-project:1.0
```

### Criar/executar container deixando a seleção de portas automática
```
docker run -d -P dockersamples/static-site
```

### Criar/executar container expondo uma porta <destino>:<origem>
```
docker run -p 5010:80 my-project:1.0
```

### Iniciar container e vincular terminal atual com o do container
```
docker start -a -i id-container
```

### Obter detalhes do container
```
docker inspect id-container
```

### Iniciar container e criar volume
```
 docker run -it -v "C:\Users\teste-docker:/var/www" ubuntu
```

### Iniciar container, criar volume e definir um comando inicial
```
docker run -d -v "C:\Users\teste-docker:/var/www" -w "/var/www" node npm start
```

### Remover container
```
docker rm id-container
```

### Remover todos os containers parados
```
docker container prune
```

### Remover container pelo id da imagem
```
docker rm $(docker ps -aq -f ancestor=id-imagem)
```

### Mostrar todos os cantainers (mesmo inativos)
```
docker ps -a
```

### Mostar imagens baixadas
```
docker images
```

### Remover imagens
```
docker rmi id-imagem
```

### Criar imagem
```
docker build -t my-project:1.0 .
```

## Links úteis
Minicurso Docker - Conteinerizando uma aplicação ASP.NET Core MVC: https://www.youtube.com/watch?v=rqBWvco0i_Y  
Imagens Docker para .NET Core: https://hub.docker.com/_/microsoft-dotnet-aspnet  
docker run with --interactive and --tty flag: https://stackoverflow.com/questions/59965032/docker-run-with-interactive-and-tty-flag  
What does it mean to attach a tty/std-in-out to dockers or lxc?: https://stackoverflow.com/questions/22272401/what-does-it-mean-to-attach-a-tty-std-in-out-to-dockers-or-lxc  
Configurações do Firewall do Windows para permitir que o Docker for Windows compartilhe a unidade: https://qastack.com.br/programming/42203488/settings-to-windows-firewall-to-allow-docker-for-windows-to-share-drive  
Absolute paths change with git bash on windows: https://github.com/moby/moby/issues/24029  