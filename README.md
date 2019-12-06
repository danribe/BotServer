# BotServer
Um bot em Shell Script que publica automaticamente em períodos pré-determinados tweets com o status de um servidor
mostrando a carga média da CPU, memória RAM utilizada e espaço livre em disco.

Requisitos:
- Se precisa ter uma conta de desenvolvedor do Twitter
- Criar um app
- Ter acesso à todos os tokens e keys após criar o app

Ferramentas necessárias do Script:
- curl
- jq
- nkf

Limatações:
- Máximo de 300 posts a cada 3 horas
- Status iguais a cada 3 horas não serão postados e retornarão um erro.

1o passo:
Preencher todas as variáveis do arquivo tweet.client.key (o que não é obrigatório) com suas tokens e keys, ou criar as mesmas variáveis no arquivo tweet.sh devidamente preenchidas.

2o passo:
Utilizar o comando "nohup" para executar o script em segundo plano e redirecionar a saída para um arquivo .log
nota: o script tweet.sh recebe um parâmetro de intervalo de tempo em segundos para as postagens.

Uso:
nohup ./tweet.sh [intervalo de postagens] > ./[nome do arquivo de log].log &
