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

3. **Execute o Contêiner Docker**:
   - Após a construção da imagem, execute o contêiner com o comando:
     ```bash
     docker run -d -p 8080:80 meu-projeto-web
     ```

4. **Acesse seu Site**:
   - Abra seu navegador e vá para `http://localhost:8080` para ver seu site em ação.

Este `Dockerfile` simples utiliza o Nginx para servir seus arquivos HTML, CSS e JavaScript. Se precisar de mais alguma coisa ou tiver alguma dúvida, estou aqui para ajudar! 🚀

