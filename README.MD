# Esse repositório tem como finalidade concluir um desafio de código realizado durante o curso Docker Fundamentals da DIO.

1. Para reproduzir o container em seu ambiente virtualizado certifique-se de ter o docker instalado em sua máquina, feito isso execute os seguintes comandos.

```
sudo apt update
sudo apt install ca-certificates curl gnupg lsb-release
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

2. Esses comandos vão garantir que sua máquina virtual esteja atualizada para realizar a execução, após atualizar execute os seguintes comandos:

```
mkdir exercicio
cd exercicio
nano docker-compose.yml
```

3. Caso não tenha o nano instalado utilize ``` apt install nano ``` para instalar a ferramenta de edição de arquivos e crie um arquivo com o nome docker-compose.yml.

4. Feito isso cole o conteúdo do docker-compose.yml dentro do arquivo docker-compose.yml que criou.

5. Crie outro arquivo no mesmo diretório /exercicio utilizando o nano chamado index.html e cole o conteúdo do index.html dentro dele.

6. Feito isso, você pode executar o comando ```docker-compose -d up```, isso vai iniciar a aplicação e disponibilizá-la na porta 80.

7. Como a conexão ocorre via bridge, caso você acesse pela porta 80 do host que hospeda o container, será possível ver a mensagem de sucesso.

8. Para identificar o ip do host, você pode utilizar o seguinte comando  ```ip -h address``` e procurar pela tag eth0, esse será o endereço de sua máquina atual.

9. Agora abra seu navegador, insira o endereço na barra de pesquisa apontando para a porta 80 e pronto, uma mensagem deve aparecer em sua tela.