# computacao-urbana

## Transporte
### Ciclovias
* Coordenadas das extremidades das ciclovias foram obtidas por meio do Google Maps
* As distâncias entre as coordenadas foram convertidas KM
* As coordendas das extremidades foram interpoladas de forma linear, gerando pontos intermediários a cada 0,1KM

### Estações-tubo
* Os nomes das estações tubo foram obtidas de https://pt.wikipedia.org/wiki/Rede_Integrada_de_Transporte
* As coordenadas das estações-tubo foram obtidas por meio da API https://nominatim.openstreetmap.org/ui/search.html
* Foram considerados apenas os terminais e estações-tubo, pois a cidade de Curitiba possui mais de 3 mil pontos de ônibus ( Fonte: https://www.urbs.curitiba.pr.gov.br/institucional/urbs-em-numeros), distribuídos aproximadamente de maneira uniforme pelo espaço geográfico, de forma que tal característica pouco contribuiria para o modelo

## Segurança
* Os registros de ocorrências policiais da Guarda Municipal de Curitiba foram obtidos da base SiGesGuarda, disponível em https://www.curitiba.pr.gov.br/dadosabertos/busca/
* Os registros foram filtrados pela natureza da ocorrência e divididos em dois grupos: (I) crimes contra a vida (ameaça, disparo de arma, estupro, homicídio e agressão); e (II) crimes contra o patrimônio (alarme, arrastão, furto, invasão, roubo e receptação)
* As coordendas das ocorrências foram obtidas por meio da APIhttps://nominatim.openstreetmap.org/ui/search.html
* Como os registros de ocorrências não contém o número do endereço, foi considerado o ponto médio de cada logradouro (valor retornado pelo próprio Open Street Maps), de forma que para ruas pequenas, a diferença entre o valor aproximado e o valor real será mínima
* Para ruas grandes, foi considerado o logradouro e também o bairro

## Zoneamento
* Os dados de alváras foram obtidos da base de alváras, disponível em https://www.curitiba.pr.gov.br/dadosabertos/busca/
* Os registros foram filtrados e divididos em dois grupos: (I) indústria -cuja atividade principal é a industrialização, fabricação, fundição ou extração-; e (II) comércio
* Foram desconsiderados os registros de alvarás de estabelecimentos que prestam serviços

## Saúde
* As localizações das unidades de saúde públicas foram obtidas em https://saude.curitiba.pr.gov.br/a-secretaria/localizacao-de-servicos-da-saude.html
* As localizações dos hospitais foram obtidas em https://turismo.curitiba.pr.gov.br/conteudos/hospitais-e-clinicas/35
* As coordenadas das unidades de saúde públicas foram obtidas por meio da API https://nominatim.openstreetmap.org/ui/search.html
* As coordenadas dos hospitais foram obtidas manualmente, por meio do Google Maps

## Educação
* As instituições de ensino das redes municipal, estadual, federal e particular foram obtidas de http://www4.pr.gov.br/escolas/frmPesquisaEscolas.jsp
* A lista de instituições foi complementada com dados de universidades contidos na base de alvarás de https://www.curitiba.pr.gov.br/dadosabertos/busca/, filtrando os registros em função da atividade principal como ensino de graduação e pós-graduação
*	As coordenadas das escolas foram obtidas por meio da API https://nominatim.openstreetmap.org/ui/search.html

## Lazer
* A lista de pontos turísticos, de lazer, cultura, esporte, entretenimento e música foi elaborada manualmente
* Constam nessa lista as localizações de parques, bosques, museus, bibliotecas, cinemas, teatros, estádios, espaços para espetáculos e clubes privados
* Como a cidade de Curitiba possui cerca de 500 praças, cuja distribuição parece ser uniforme pelo espaço geográfico, elas não foram consideradas, pois pouco contribuiriam para o modelo (Fonte: http://cbncuritiba.com/as-438-pracas-de-curitiba/)

## Valor imobiliário
* Os valores de aluguel e compra de imóveis em Curitiba foram obtidos de https://www.imovelweb.com.br/noticias/imovelweb-index/imovelweb-index-um-retrato-mercado-imobiliario-de-curitiba/
* Em razão da falta de dados, não foram considerados os preços médios de aluguel dos seguintes bairros: Abranches, Augusta, Butiatuvinha, Cascatinha, Caximba, Fanny, Ganchinho, Jardim Social, Jardim das Américas, Lamenha Pequena, Orleans, Riviera, São João, São Lourenço, São Miguel, Taboão, Umbará e Vista Alegre
