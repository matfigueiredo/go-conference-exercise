# Aplicação de Reserva de Ingressos para a Go Conference

Este é um programa em Go que permite que os usuários reservem ingressos para a "Conferência Go". Ele oferece uma interface de linha de comando simples para inserir os detalhes do usuário e reservar ingressos. O programa também envia um email de confirmação do ingresso para o usuário após a reserva bem-sucedida.

Construí esse projeto seguindo o passo a passo do canal TechWorldWithNana -> https://www.youtube.com/@TechWorldwithNana

## Pré-requisitos
Para executar este programa, certifique-se de ter o Go instalado em seu sistema. Você pode baixar e instalar o Go no site oficial do Go: https://golang.org

## Começando
1 - Clone o repositório ou faça o download do código-fonte.
2 - Abra um terminal ou prompt de comando e navegue até o diretório do projeto.
3 - Compile o programa usando o seguinte comando:

```
go build
```
4 - Execute o executável:

Em sistemas Unix/Linux:

```
./main
```

Em sistemas Windows:

```
main.exe
```
## Uso
1 - Ao executar o programa, você receberá uma mensagem de boas-vindas com informações sobre a conferência e o número de ingressos disponíveis.

2 - Insira seus detalhes conforme solicitado:

- Primeiro nome
- Sobrenome
- Endereço de email
- Quantidade de ingressos

3 - O programa validará sua entrada quanto ao tamanho do nome, formato do email e disponibilidade de ingressos.

- Se sua entrada for válida e houver ingressos disponíveis, o programa reservará os ingressos para você e iniciará o envio do email de confirmação em segundo plano.

- Se sua entrada for inválida ou não houver ingressos disponíveis, mensagens de erro apropriadas serão exibidas.

4 - Assim que o email for enviado (após um atraso de 10 segundos), você verá os detalhes do ingresso e o endereço de email para o qual foi enviado.

5 - Você pode repetir o processo para reservar ingressos para outros usuários ou sair do programa.

## Estrutura do Código
O código está estruturado em várias funções:

- **greetUsers**: Exibe uma mensagem de boas-vindas e informações sobre a conferência e os ingressos disponíveis.
- **getFirstNames**: Retorna uma lista de primeiros nomes das reservas atuais.
- **getUserInput**: Solicita ao usuário que insira seus detalhes (primeiro nome, sobrenome, email e quantidade de ingressos) e os retorna.
- **bookTicket**: Reserva os ingressos para o usuário, atualiza a contagem de ingressos restantes e armazena as informações da reserva.
- **sendTicket**: Envia o email de confirmação do ingresso após um atraso de 10 segundos.
- **main**: O ponto de entrada do programa. Ele chama as funções necessárias para cumprimentar os usuários, obter a entrada do usuário, validar a entrada, reservar ingressos, enviar o email e aguardar todas as goroutines serem concluídas.

## Contribua
Contribuições para este projeto são bem-vindas. Você pode contribuir enviando relatórios de bugs, solicitações de recursos ou pull requests por meio do repositório do projeto no GitHub.
