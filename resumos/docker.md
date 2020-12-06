# Docker

## Comandos úteis

### Criar/executar container
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

### Criar/executar container expondo uma porta <destino>:<origem>
```
docker run -p 5010:80 my-project:1.0
```

### Iniciar container e vincular terminal atual com o do container
```
docker start -a -i id-container
```

### Remover container
```
docker rm id-container
```

### Remover todos os containers parados
```
docker container prune
```

### Mostar imagens baixadas
```
docker images
```

### Remover imagens
```
docker rmi nome-imagem
```

## Links úteis
Minicurso Docker - Conteinerizando uma aplicação ASP.NET Core MVC: https://www.youtube.com/watch?v=rqBWvco0i_Y
Imagens Docker para .NET Core: https://hub.docker.com/_/microsoft-dotnet-aspnet