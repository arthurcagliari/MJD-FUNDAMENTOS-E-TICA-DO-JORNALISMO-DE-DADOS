# MJD

***TRABALHO DO MASTER EM JORNALISMO DE DADOS****

___Tema: Candidatos de Manaus não vacinados na cidade de Manaus___

Este repositório contém o projeto final da disciplina "Fundamentos e Ética do Jornalismo de Dados", do curso Master de Jornalismo de Dados, Automação e Storytelling, do Insper. 

O grupo é formado por ([**Arthur Cagliari**](https://github.com/arthurcagliari)), **[Giseli Araujo](https://github.com/GiseliAraujo)**, **[Lais](https://github.com/laisbs0)**, Lucas Duarte e **[Vinicius de Melo](https://github.com/viniciusdmelo)**.

O grupo utilizou duas bases de dados para o trabalho. A primeira é fornecida pelo Tribunal Superior Eleitoral (TSE) e traz dados sobre os candidatos às vagas de deputado estadual, deputado federal, governador e presidente da República nas eleições de 2022. 

Esta primeira base tem dados desagregados por nome dos candidatos, cidade de origem, documento (CPF), partido e cargo postulante. O TSE fornece tais dados em documentos no formato CSV.

👨‍💻Notebook - Clique aqui para ler e baixar o arquivo.

✔CSV - Clique aqui para ler e baixar o arquivo.

A segunda base é disponibilizada pela Secretaria Municipal de Saúde do município de Manaus e apresenta dados de todas as pessoas vacinadas na cidade no período de 28 de agosto de 2021 a 21 de setembro de 2022. A secretaria fornece tais dados em documentos no formato PDF.

👨‍💻Notebook - Clique aqui para ler e baixar o arquivo.

✔CSV - Clique aqui para ler e baixar o arquivo.

O trabalho final buscava cruzar as duas bases e descobrir quais candidatos a cargos políticos em 2022, nascidos em Manaus, não tinham tomado a vacina na cidade neste período indicado pela tabela. Como o documento da Prefeitura de Manaus estava disponibilizados em formato PDF, primeiro foi preciso fazer uma conversão do arquivo para algum outro formato em que se pudesse extrair os dados.

Quando utilizadas ferramentas gratuitas de conversores de arquivo PDF, não foi possível converter o documento como se esperava, conseguindo apenas trazer caracteres especiais. Assim, o grupo decidiu fazer uma coleta manual do arquivo PDF, página por página, selecionando o material desejado, copiando e depois colando em um arquivo TXT. 

Após isso, os dados foram tratados dentro do Excel, com a disponibilização das informações em colunas. Terminado esse tratamento, o documento foi importado para o SQL Server em tabela nomeada “Vacinados_AM”. Após a seleção da tabela, várias linhas ficaram sem a informação da faixa etária da pessoa vacinada, mas o documento final apresentou todos os números de CPF e também a data de vacinação –o que  já era suficiente para o trabalho de cruzamento planejado.

✔ CSV - clique aqui para ler e baixar o arquivo.

***#CONTEXTO DO TEMA***

O grupo escolheu cruzar tais dados sobre candidatos não vacinados na cidade de Manaus, pois a capital amazonense ganhou repercussão internacional com a falta de oxigênio e o uso de medicamentos reconhecidamente ineficazes para o tratamento da covid-19 durante a pandemia. Daí o interesse em saber se atores que estavam se postulando a um cargo político não teriam deixado de tomar a vacina. A partir de tais nomes, o grupo seguiria uma investigação mais aprofundada sobre essas pessoas.

***#PERGUNTAS***

___1 - Há quantos candidatos no estado do Amazonas?___

660 (sendo eles Aptos e Inaptos)

___2 - Quantos candidatos do estado do Amazonas não se vacinaram em Manaus?___

130 Candidatos

___3 - Quais candidatos do estado do Amazonas não se vacinaram em Manaus?___

✔ Abrir o arquivo deste projeto com o nome  -- >> NãoVacinadosNascidosManaus.xls

___4 - Há candidatos do Amazonas para presidência ou governador do estado que não se vacinaram em Manaus? Quantos?___

R.Não tem candidatos a Presidencia e 2 para Governadores(AMAZONINO ARMANDO MENDES e NAIR QUEIROZ BLAIR)
    
___5 - Quantos candidatos no estado do Amazonas nasceram em Manaus?___

R. 38 candidatos.
 
___6 - Qual é o partido predominante dos candidatos nascidos em Manaus e não vacinados em Manaus?____

![image](https://user-images.githubusercontent.com/114266007/194380275-e92f6fe1-cc07-45eb-bc99-8be31a282c1e.png)


___7 - Há muitos candidatos indígenas nascidos em Manaus e não vacinados em Manaus?___

R. 1 candidata, ANA CLAUDIA MARTINS TOMAS

___8 - Qual era a cor/raça predominante dos candidatos nascidos em Manaus?___

![image](https://user-images.githubusercontent.com/114266007/194381013-61547351-51ec-4241-ab61-a9dbd77a2e63.png)


R. Em 47, PARDA teve o maior Contagem de Candidato e foi 840,00% maior do que INDÍGENA, que teve o menor Contagem de Candidato em 5. PARDA teve o maior Contagem de Candidato em 47, seguido por BRANCA, PRETA e INDÍGENA. PARDA contabilizou 54,02% de Contagem de Candidato. Em todos os 4 DS_COR_RACA, Contagem de Candidato variou de 5 para 47.


___Caminhos possíveis a serem seguido para realização de pauta, com os insights obtidos por meio da análise de dados:

1. Confirmar quais candidatos nascidos em Manaus realmente não tomaram vacina contra Covid-19 e cruzar com sua atuação durante a pandemia. Quem não tomou vacina foi considerado negacionista? Incentivou o uso de cloroquina e tratamento precoce? Preconizou contra a origem das vacinas, principalmente a Coronavac? Sua posição política é alinhada com o governo?

2. Quem são os políticos não-vacinados dos partidos com maior número de não-vacinados (Agir, PDT e Solidariedade) em Manaus? Qual o alinhamento político de cada um desses candidatos? Eles defenderam o tratamento precoce e o uso da cloroquina? Em caso de políticos que concorriam a eleição, destinaram verbas ou promoveram políticas públicas em prol de outros tratamentos que não a vacinação contra a Covid-19?

3. A candidata indígena Ana Claudia Martins Tomas não tomou a vacina em Manaus. Ela realmente não foi vacinada? Se sim, quais as alegações? Lembrar-se que houve uma rejeição à vacinação por parte da população indígena devido a influência das comunidades evangélicas.
