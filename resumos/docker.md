# Docker

## Comandos úteis

### Cria container
```
docker run hello-word
```

### "Olá mundo"
```
docker run ubuntu echo "Olá mundo"
```

### Criar container e vincular terminal atual com o do container 
```
winpty docker run -it ubuntu
```
Obs: winpty é necessário quando se está no Windows e o prompt não é o PowerShell (vide: https://stackoverflow.com/questions/48623005/docker-error-the-input-device-is-not-a-tty-if-you-are-using-mintty-try-prefi)

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