##
## DESAFIO 
1 -Objetivo: 
É a prática de comandos Linux e Markdown 
2 – Entregáveis: 
Todos os arquivos de “dados_de_vendas.csv” gerados (pode-se renomea-los para 
“commitar”) 
Todos os arquivos de scripts gerados 
Arquivo de evidências de execução contendo imagens/prints das execuções. 
Arquivo escrito no formato markdown contendo todos os passos para a reexecução do 
desafio 
3 – Preparação: 
Faça o download do arquivo “dados_de_vendas.csv” 
No Linux cria um diretório chamado “ecommerce” e nele insira o arquivo chamado 
“dados_de_venda.csv” 
Esse arquivo chamado “dados_de_venda.csv”, que contém informações sobre as 
vendas de uma loja online. O arquivo tem que ter o seguinte formato: 
 “id, produto, quantidade, preço, data” 
Cada linha representa uma venda realizada com: “id da venda, o nome do produto, a 
quantidade vendida, o preço unitário e a data da venda”. Por exemplo: 
1, camiseta, 2, 29.90, 1/01/2023 
Significa que a venda de id 1 foi de 2 camisetas, cada uma custando 29.90 reais, na 
data 1/01/2023 
4 – Desafio: 
O seu objetivo é processar e gerar relatório de vendas para isso será necessário: 
4.1 – Criar arquivo executável: 
criar um arquivo executável chamado “processamento_de_vendas.sh” que realiza as 
seguintes tarefas usando os comandos do Linux. 
Cria um diretório chamado vendas e copie o arquivo “dados_de_vendas.csv” para 
dentro dele. 
Dentro do diretório chamado vendas, cria um subdiretório chamado “backup” e faça 
uma cópia do arquivo “dados_de_venda.csv” para dentro dele com a data de 
execução como parte do nome do arquivo no padrão “yyyymmdd” precedido de hífen. 
Por exemplo: “dados-20230831.csv” 
Dentro do diretório backup, renomeie o arquivo “dados-yyymmdd.csv” para “backupdados-yyymmdd.csv” 
Seguindo os mesmos padrões acima. Por exemplo: “backup-dados-20230831.csv” 
Dentro do diretório backup cria um arquivo chamado “relatório.txt” que contenha as 
seguintes informações: 
- data do sistema operacional informado YYY/MM/DD HH:MI 
- data do primeiro registro de venda contido no arquivo 
- data do último registro de venda contido no arquivo 
- a quantidade total de itens diferentes vendidos 
- dentro do diretório backup, mostra as primeiras 10 linhas do arquivo “backupdados-yyyymmdd.csv” e os inclua no arquivo “relatório.txt 
- para a redução de espaço em disco comprima o arquivo “backup-dadosyyyymmdd.csv” para arquivo “backup-dados-yyyymmdd.zip” 
- apague o arquivo “backup-dados-yyyymmdd.csv” do diretório backup e o arquivo 
“dados_de_vendas.csv do diretório vendas 
 4.2 – Agendar a execução do processamento 
- então cria um agendamento de execução de comandos Linux para executar esse 
script “processamento_de_vendas.sh”, todos os dias de segunda a quinta às 15:27. 
Não se esqueça de conceder permissões para a execução do script 
4.3 - Criar novo relatório 
- depois de tudo isso pronto, vamos mudar os dados para criar um novo relatório. 
- 1 por dia modifique manual e completamente os dados do arquivo vendas 
“dados_de_vendas.csv” que estão no diretório ecommerce 
- certifique-se que o arquivo “processamento_de_venda.sh esteja corretamente 
agendado 
- crie um script chamado “consolidador_de_processamento_de_vendas.sh” que une 
todos os relatórios gerados e gere outro arquivo chamado “relatório_final.txt” 
- após diversos execuções do script “processamento_de_vendas.sh” execute 
manualmente o script “consolidador_de_processamento_de_vendas.sh

##
## Minha Solução

O problema a ser resolvido? O desafio consistia em criar  scripts que processasse um arquivo dados_de_vendas.csv e gerasse relatórios com algumas informações, entre as quais a quantidade total de itens diferentes , salvando backups e organizando os dados de maneira eficiente. Além disso, havia a necessidade de consolidar todos esses relatórios diários em um relatório final após o 4º dia.
Essas ações atendem aos requisitos do desafio, conforme descrito acima. 

A forma que resolvi :Foram desenvolvidos dois scripts:
1.	processamento_de_vendas.sh: Ele processa o arquivo dados_de_vendas.csv, copiando-o para o diretório  de vendas e criando backups rotulados com a data e hora. Ele também gera um relatório contendo informações como a data de execução, data do primeiro e último registro de vendas, e a quantidade total de itens vendidos. Por fim, o script compacta o arquivo de backup e remove os arquivos de origem.
2.	consolidador_de_processamento_de_vendas.sh: Esse script consolida todos os relatórios gerados pelo primeiro script em um único arquivo chamado relatorio_final.txt. Ele varre todos os arquivos de relatório no diretório de backup e os agrupa em um arquivo final para facilitar a análise dos dados.
Dificuldades? Foram algumas, entre as quais poderia incluir o agendamento correto do cron job para garantir que o script fosse executado nos horários indicados, bem como a manipulação eficiente e as permissoes para acessar os arquivos no Linux . A geração de backups, compactar dados e garantir que os relatórios fossem gerados corretamente
Quanto ao código em execução e evidências de execução. 
Estão mostradas os prints dos códigos e os seus processamentos Os scripts fornecidos já incluem comandos e seus respectivos markdown que mostram as etapas sendo realizadas. As evidências de execução foram obtidas com os prints das saídas no terminal shell do linux após a execução de cada  scripts. Houve também os prints através do explorer do Windows.
Em resumo é isto. Muito Obrigado!

##
## Exercícios

1. Processamento de Vendas:
[Script de Processamento de Vendas](exercicios/processamento_de_vendas.sh)

2. Consolidador de Processamento de Vendas:
[Script Consolidador de Processamento de Vendas](exercicios/consolidador_de_processamento_de_vendas.sh)

##
## Evidências

Ao executar o código do Processamento de Vendas, observei que os resultados foram conforme esperado, como mostrado na imagem a seguir:


1. ![Data e Crontab](evidencias/data_e_crontab%20-_e.jpg)

2.  ![Diretório Ecommerce](evidencias/diretorio%20ecommerce.jpg)

3.  ![Dados de Vendas CSV](evidencias/dados_de_vendas_csv.jpg)

4.  ![Relatório 1](evidencias/1%20relatorio.jpg)
 
5.  ![Dia no Shell do Linux](evidencias/2%20dia%20no%20Shell%20do%20linux.jpg)

6.  ![View pelo Explorer do Windows](evidencias/view%20pelo%20explorer%20do%20windos.jpg)

7.  ![Relatório 2](evidencias/2%20relatorio.jpg)

8.  ![Dia 3](evidencias/3%20dia.jpg)

9. ![Relatório 3](evidencias/3%20relatorio.jpg)

10.![Dia 4](evidencias/4%20dia.jpg)

11.![Relatório 4](evidencias/4%20relatorio.jpg)
 
12.![Pasta Backup de Vendas](evidencias/pasta%20backup%20de%20vendas%20de%20ecommerce.jpg)

13.![Script de Processamento](evidencias/script%20de%20processamento.jpg)

14.![Script Consolidador](evidencias/script%20de%20consolidador.jpg)

15.![Relatório Final](evidencias/relatorio%20final.jpg)

16.![Upgrade no Script Consolidador](evidencias/upgrade%20no%20script%20consolidador.jpg)

17.![View no Shell](evidencias/view%20no%20Shell.jpg)

18.![View do Novo Relatório Final](evidencias/view%20do%20novo%20relatorio%20final%20.jpg)

19.![Resultado do Consolidador](evidencias/resultado%20do%20consolidador%20.jpg)

20.![Último Status do Ecommerce](evidencias/ultimo%20status%20do%20ecommerce.jpg)



##
## Certificados

Por orientaçao da Compass UOL, somente colocaremos certificados de cursos extras UDEMY, e que estejam relacionados a AWS AMAZON WEB SERVICES.


