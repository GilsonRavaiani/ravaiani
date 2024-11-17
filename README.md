# ravaiani

Testando criar uma imagem pessoal no docker utilizando minha página pessoal!

#Iniciando projeto!

Utilizando Ubuntu:

git clone https://github.com/GilsonRavaiani/ravaiani.git

Entrar na pasta do repositório

No VScode criar o arquivo Docker (Configurações no código)

Utilizando o COPILOT pesquisei o passo a passo apresentando o meu código

Informei meu site pessoal com HTML. CSS e JS

Segue resposta e editei conforme minha necessidade.

![Construir Image Docker](/Readme/Copilot.jpg)

Pedi ajuda ao criar o arquivo Docker: Crie um arquivo docker para meu codigo

Claro! Aqui está um exemplo de `Dockerfile` para o seu projeto HTML, CSS e JavaScript. Este `Dockerfile` vai criar uma imagem Docker que serve seu site usando um servidor web simples, como o Nginx.

### Dockerfile
```Dockerfile
# Use uma imagem base do Nginx
FROM nginx:latest

# Copie os arquivos do seu projeto para o diretório padrão do Nginx
COPY . /usr/share/nginx/html

# Exponha a porta 80 para acesso externo
EXPOSE 80

# Comando para iniciar o servidor Nginx
CMD ["nginx", "-g", "daemon off;"]
```

### Passos para Criar e Executar a Imagem Docker

1. **Crie o Dockerfile**:
   - Salve o conteúdo acima em um arquivo chamado `Dockerfile` na raiz do seu projeto.

2. **Construa a Imagem Docker**:
   - No terminal, navegue até o diretório do seu projeto e execute o comando:
     ```bash
     docker build -t meu-projeto-web .
     ```
![Construir Image Docker](/Readme/Construir_Image_Docker.jpg)


3. **Execute o Contêiner Docker**:
   - Após a construção da imagem, execute o contêiner com o comando:
     ```bash
     docker run -d -p 8080:80 meu-projeto-web
     ```

4. **Acesse seu Site**:
   - Abra seu navegador e vá para `http://localhost:8080` para ver seu site em ação.

Este `Dockerfile` simples utiliza o Nginx para servir seus arquivos HTML, CSS e JavaScript 🚀

## Precisamos adequar a resposta a nossa necessidade

## Após a criação da imagem subi para o Docker Hub com a ajuda do Copilot:

Subir uma imagem para o Docker Hub envolve alguns passos. Aqui está um guia passo-a-passo para te ajudar:

### Passos para Subir uma Imagem para o Docker Hub

1. **Faça Login no Docker Hub**:
   - No terminal, faça login na sua conta do Docker Hub usando o comando:
     ```bash
     docker login
     ```
   - Insira seu nome de usuário e senha quando solicitado.

2. **Tagueie a Imagem**:
   - Antes de subir a imagem, você precisa tagueá-la com o seu repositório do Docker Hub. Supondo que sua imagem se chame `meu-projeto-web`, use o comando:
     ```bash
     docker tag meu-projeto-web seu-usuario/meu-projeto-web:v1.0
     ```
   - Substitua `seu-usuario` pelo seu nome de usuário do Docker Hub e `v1.0` pela versão da sua imagem.

3. **Suba a Imagem**:
   - Use o comando `docker push` para subir a imagem para o Docker Hub:
     ```bash
     docker push seu-usuario/meu-projeto-web:v1.0
     ```

4. **Verifique no Docker Hub**:
   - Vá até o [Docker Hub](https://hub.docker.com/) e verifique se sua imagem foi subida corretamente. Você deve vê-la listada no seu repositório.

### Exemplo Completo:

```bash
# Faça login no Docker Hub
docker login

# Tagueie a imagem
docker tag meu-projeto-web seu-usuario/meu-projeto-web:v1.0

# Suba a imagem
docker push seu-usuario/meu-projeto-web:v1.0
```

## Vamos subir a imagem agora para o Azure Container Register (ACR)

Conficguração ACR

## Agora criar o Web App

