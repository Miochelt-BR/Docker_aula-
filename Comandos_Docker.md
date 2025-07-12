para 
**docker pull nginx:1.29.0-alpine**



**comandos basicos
# Verificar imagens locais
docker images

# Baixar imagem do Docker Hub
docker pull <imagem>:<tag>

# Rodar um container
docker run <opções> <imagem>:<tag>

# Rodar container com porta exposta
docker run -d -p 8080:80 nginx:1.29.0-alpine

# Ver containers em execução
docker ps

# Ver todos os containers (executando ou não)
docker ps -a

# Parar um container
docker stop <container_id_ou_nome>

# Remover um container
docker rm <container_id_ou_nome>

# Remover uma imagem
docker rmi <imagem>:<tag>

# Inspecionar detalhes de uma imagem
docker image inspect <imagem>:<tag>

# Ver logs de um container
docker logs <container_id_ou_nome>

# Acessar terminal do container
docker exec -it <container_id_ou_nome> /bin/sh

# Ver versão do Docker
docker --version

# Ver ajuda de qualquer comando
docker <comando> --help




**COMANDOS EXTRAS**
📘 Exemplo prático
bash
Copiar
Editar
curl -I https://www.google.com
🔽 Saída típica:

http
Copiar
Editar
HTTP/2 200 
date: Sat, 13 Jul 2025 02:14:39 GMT
expires: -1
cache-control: private, max-age=0
content-type: text/html; charset=ISO-8859-1
x-frame-options: SAMEORIGIN
server: gws


