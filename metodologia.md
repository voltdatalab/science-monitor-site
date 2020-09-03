---
layout: pages
title: Metodologia
last_update: "17 de agosto, 2020"
description: "Como o Science Pulse funciona."
social_description: "Como o Science Pulse funciona."
main_img: '{{ site.baseurl }}/img/header_red.jpeg'
---

_Você pode acessar nosso código aberto desta aplicação [neste link](https://github.com/voltdatalab/science-pulse-public)._

_[Read the methodology in English](methodology)_

## SOBRE OS DADOS

### COLETA DE PERFIS
Todos os perfis de cientistas, especialistas, médicos, organizações e iniciativas científicas foram compilados pela equipe de desenvolvimento do Science Pulse por uma variedade de métodos. Encontramos esses perfis, principalmente, de três formas:

1. Um crowdsourcing, pelo qual convidamos as pessoas a sugerir perfis;

2. Ao identificar usuários com perfis verificados pelo Twitter e, a partir deles, encontrar novos perfirs a partir de quem seguem;

3. Consultando listas de Twitter feitas por universidades ou jornalistas.

Qualquer pessoa pode sugerir um novo perfil para ser incluído em nossa plataforma através [deste formulário](https://forms.gle/KHufKHzJxJVdsD7s8).

Caso seja um cientista ou especialista com o perfil mapeado por esta ferramenta, vou pode solicitar sua exclusão do banco de dados do Science Pulse. Envie um email para [sciencemonitor@icfj.org](mailto:sciencemonitor@icfj.org).


### COLETA DE DADOS

Novos posts em redes sociais são coletados constantemente. Por enquanto, estamos limitando o número de tweets para apenas períodos de 30 dias. Nosso banco de dados é atualizado regularmente com novos tweets e contagens, respeitando os limites da API gratuita do Twitter.

Ainda estamos trabalhando em módulos para incluir outras plataformas de redes sociais.

## SOBRE O ALGORITMO

### ABA TWITTER TRENDS

Todas as nossas tendências consideram apenas tweets publicados ou recompartilhados nas últimas 12 horas pelos perfis que seguimos.

Nossa aba principal de tendências é separada em três grupos para cada idioma:

1. **Popular within pulse**: lista tweets de autoria de perfis monitorados pelo Science Pulse que tenham o maior número de retweets de toda a população de usuários (contagem de RTs), no momento da última coleta de dados.

2. **Popular among scientists**: mostra as publicações mais retuitadas pelos perfis monitorados pelo Science Pulse. Toda vez que um perfil que monitoramos compartilha um tweet, ele conta como um (n = 1). As publicações melhor rankeadas possuem o maior número de retweets dentro dessa amostragem, assim identificando os tweets que conseguiram mais atenção entre os perfis monitorados pelo Science Pulse. Por exemplo: se 15 perfis em nosso banco de dados compartilharam este  [tweet da OMS](https://twitter.com/WHO/status/1275349898209173505), ele possui um taxa de compartilhamento de 15.

3. **Rising in popularity**: rankeia os cinco tweets com maior proporção de RTs por seguidores (RT:followers) publicados por membros da lista do Science Pulse (apenas se tiverem mais de 10 retweets). Essa lista mostra posts que tiveram engajamento significativo (com base em RTs), levando em conta o alcance (número de seguidores) do perfil que a escreveu. Se um tweet tiver 200 RTs e seu autor tiver 400 seguidores, o tweet possui uma razão de 0,5 RT:seguidores.


### ABA EXPLORE TWEETS

Essa aba serve para maior exploração do banco de dados do Science Pulse. Ela contém quatro conjuntos de informações sobre tweets publicados nas últimas 12 horas, também filtrados por idioma:

1. **Active Users**: os usuários que mais tuitaram no período;

2. **Hashtags**: as hashtags mais compartilhadas no mesmo período;

3. **Also popular within pulse**: utilizamos um algoritmo de agrupamento (k-means clustering) para classificar esses tweets em quatro grupos, de acordo com sua contagem de retweets com base na última coleta de dados (de 1 a 4, sendo 4 o grupo com mais retweets). Então, consideramos apenas tweets do "grupo 2", eliminando aquelas que provavelmente são mensagens pessoais e, assim, possuem menos retweets (grupo 1) e aquelas que atingiram o topo dos nossos trending topics (da aba Trends) ou com grande volume orgânico (grupos 3 ou 4). Dentro do grupo 2 é utilizada a mesma métrica da coluna "Popular within Pulse" na aba Trends.  

4. **Pulse radar**: este conjunto de dados representa uma amostra aleatória de cinco tweets do grupo 2 (descrito acima). Tweets podem coincidir com o conjunto anterior, mas dá a chance para o usuário encontrar conteúdo interessante que não está nos trends.

### COVID-19 TWEETS TAB

A aba COVID-19 filtra tweets nas últimas 12 horas por palavras-chave relacionadas à pandemia. As métricas utilizadas são as mesmas para usuários ativos e hashtags da aba EXPLORE - com a exclusão de hashtags mais recorrentes, como [#COVID-19](https://twitter.com/hashtag/covid19) - e da coluna Popular within Pulse, da aba TRENDS.  

Essas são as palavras-chave aplicadas como filtro: "Covid", "covid", "Coronavirus", "coronavirus",
                    "Corona", "corona", "SARS-CoV-2", "Sars-CoV-2",
                    "SRAG", "sindrome", "syndrome", "pandemic",
                    "pandemia", "WHO", "OMS", "quarantine", "social distancing",
                    "quarentena", "isolamento social", "distanciamento social",
                    "mascara", "mask", "distanciamiento social", "spread", "asymptomatic",
                    "epidemic", "outbreak", "epidemia", "vacina", "vaccine", "wuhan", "Wuhan"

### ABA POPULARITY

Essa aba permite com que o usuário do Science Pulse veja as hashtags mais usadas e os usuários mais ativos em um período de tempo selecionado, e também mostrar um gráfico com o número de posts publicados com uma palavra-chave específica.

### ABA PROFILES

Na aba PROFILES, listamos todos os perfis que compõe a curadoria do Science Pulse, entre cientistas, instituições, pesquisadores e especialistas. Para ajudar usuários a descobrir novas fontes de informação científica, a tabela Find New Experts retorna uma amostra aleatória de cinco perfis que possuam o número de usuários menor do que a mediana de seguidores dos perfis em nosso banco de dados.
