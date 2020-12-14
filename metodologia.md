---
layout: pages
title: Metodologia
last_update: "14 de dezembro, 2020"
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

1. **Popular no Pulse**: lista tweets de autoria de perfis monitorados pelo Science Pulse que tenham o maior número de retweets de toda a população de usuários (contagem de RTs), no momento da última coleta de dados. Usuários podem escolher duas opções para visualização: *Enhance Discovery* mostra tweets de usuários que estejam abaixo da mediana do número de seguidores dentre os perfis listados no Science Pulse, e *Focus on Popularity* mostra tweets de todos os perfis da base de dados.

2. **Popularidade em alta**: ranqueia os cinco tweets com maior proporção de RTs por seguidores (RT:followers) publicados por membros da lista do Science Pulse (apenas se tiverem mais de 10 retweets). Essa lista mostra posts que tiveram engajamento significativo (com base em RTs), levando em conta o alcance (número de seguidores) do perfil que a escreveu. Se um tweet tiver 200 RTs e seu autor tiver 400 seguidores, o tweet possui uma razão de 0,5 RT:seguidores.

3. **Descubra mais**: mostra uma lista de 5 tweets aleatórios que tiveram mais que um RT (por usuários de toda a rede social) e são de autoria de perfis listados no Science Pulse. Ao clicar no ícone "Mostrar novos tweets" o usuário sorteia uma nova lista com 5 tweets aleatórios.

### ABA FACEBOOK

Essa seção é composta por posts do Facebook feitas nas últimas 24 horas. Ela apresenta duas colunas com posts em destaque nas páginas seguidas pelo Science Pulse, a partir de dados do [Crowd Tangle](https://www.crowdtangle.com/), além de uma coluna com a possibilidade do usuário explorar outros posts nas páginas monitoradas pela nossa ferramenta. 

Os três grupos de postagem são:

1. **Desempenho em alta**: posts com os maiores escores na medida de desempenho em alta (*overperforming*), desenvolvida pelo Crowd Tangle. Essa métrica mostra publicações que estão se saindo melhor em engajamento em relação ao que seria esperado pelas características da página em que ela foi publicada.  

2. **Populares**: postagens com o maior número de compartilhamentos na lista de páginas selecionadas pelo Science Pulse. Essa métrica serve para identificar o que tem sido compartilhado em massa.

3. **Descubra mais**: amostra aleatória de 5 posts das páginas monitoradas pelo Science Pulse. Ao clicar no ícone "Mostrar novos posts" o usuário sorteia uma nova lista com 5 posts.

### ABA EXPLORE 

Essa aba serve para maior exploração do banco de dados de tweets do Science Pulse. Ela contém quatro conjuntos de informações sobre tweets publicados nas últimas 12 horas, também filtrados por idioma:

1. **Usuários ativos**: os usuários que mais tuitaram no período;

2. **Hashtags**: as hashtags mais compartilhadas no mesmo período;

3. **Também populares no pulse**: utilizamos um algoritmo de agrupamento (k-means clustering) para classificar esses tweets em quatro grupos, de acordo com sua contagem de retweets com base na última coleta de dados (de 1 a 4, sendo 4 o grupo com mais retweets). Então, consideramos apenas tweets do "grupo 2", eliminando aquelas que provavelmente são mensagens pessoais e, assim, possuem menos retweets (grupo 1) e aquelas que atingiram o topo dos nossos trending topics (da aba Trends) ou com grande volume orgânico (grupos 3 ou 4). Dentro do grupo 2 é utilizada a mesma métrica da coluna "Popular within Pulse" na aba Trends.  

4. **Radar Pulse**: este conjunto de dados representa uma amostra aleatória de cinco tweets do grupo 2 (descrito acima). Os tweets apresentados nesta coluna podem coincidir com aqueles do conjunto anterior, mas ela proporciona ao usuário maiores chances de encontrar conteúdo científico interessante e que não alcançou os trends.

5. **Popular entre cientistas**: mostra as publicações mais retuitadas pelos perfis monitorados pelo Science Pulse. Toda vez que um perfil que monitoramos compartilha um tweet, ele conta como um (n = 1). As publicações melhor ranqueadas possuem o maior número de retweets dentro dessa amostragem, assim identificando os tweets que conseguiram mais atenção entre os perfis monitorados pelo Science Pulse. Por exemplo: se 15 perfis em nosso banco de dados compartilharam este  [tweet da OMS](https://twitter.com/WHO/status/1275349898209173505), ele possui um taxa de compartilhamento de 15.


### ABA COVID-19

O **ESPECIAL COVID-19** apresenta tweets em destaque nas últimas 12 horas em posts filtrados por palavras-chave relacionadas à pandemia. As métricas utilizadas são as mesmas para usuários ativos e hashtags da aba EXPLORE - com a exclusão de hashtags mais recorrentes, como [#COVID-19](https://twitter.com/hashtag/covid19) - e das colunas da aba TRENDS.  

Essas são as palavras-chave aplicadas como filtro: "Covid", "covid", "Coronavirus", "coronavirus",
                    "Corona", "corona", "SARS-CoV-2", "Sars-CoV-2",
                    "SRAG", "sindrome", "syndrome", "pandemic",
                    "pandemia", "WHO", "OMS", "quarantine", "social distancing",
                    "quarentena", "isolamento social", "distanciamento social",
                    "mascara", "mask", "distanciamiento social", "spread", "asymptomatic",
                    "epidemic", "outbreak", "epidemia", "vacina", "vaccine", "wuhan", "Wuhan",
                    "herd immunity", "imunidade de rebanho", "imunidade coletiva".

### ABA SEARCH

Na aba **SEARCH**, usuários podem pesquisar tweets dos últimos 30 dias de acordo com diferentes filtros, como algumas palavras-chave, intervalo de datas, perfis verificados, retweets ou replies. 

### ABA PROFILES

Na aba **PROFILES**, listamos todos os perfis que compõe a curadoria do Science Pulse, entre cientistas, instituições, pesquisadores e especialistas. Para ajudar usuários a descobrir novas fontes de informação científica, a tabela *Encontre novos especialistas* retorna uma amostra aleatória de cinco perfis que possuam o número de seguidores menor do que a mediana dessa medida dentre todos os perfis em nosso banco de dados.

### ABA PÁGINAS (FB)

Nesta aba, listamos todas as páginas públicas do Facebook que no momento são monitoradas pelo Science Pulse. Esta lista é formada por páginas de universidades, organizações científicas e iniciativas de divulgação de pesquisas brasileiras e internacionais. A coluna *Encontre novas páginas* mostra uma amostra aleatória de cinco páginas que possuam um número de seguidores menor do que a mediana de todas as páginas em nosso banco de dados.
