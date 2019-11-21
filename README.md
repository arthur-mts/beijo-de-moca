# Projeto-Beijo-de-Moca
**Projeto final da disciplina de Estatística aplicada a computação** \
Tem o objetivo de gerar interpreções sobre os gastos públicos suspeitos feitos por deputados e senadores com \
dados disponibilizados pelo Jarbas, um site onde é possível navegar pelos gastos e descobrir mais sobre cada suspeita,
de maneira simples e descomplicada.


## Links uteis
- [serenata-toolbox](https://github.com/okfn-brasil/serenata-toolbox)  

- [API para acessar os dados dos senadores](http://legis.senado.leg.br/dadosabertos/docs/resource_ListaSenadorService.html#resource_ListaSenadorService_cargosSenadorXml_GET)  
- [API para acessar os dados do Portal da Transparência](http://www.transparencia.gov.br/swagger-ui.html)
 [API para acessar os dados dos deputados](https://dadosabertos.camara.leg.br/swagger/api.html)  

- [O que é a CEAP? (Cota para o exercício da atividade parlamentar
)](https://www2.camara.leg.br/transparencia/acesso-a-informacao/copy_of_perguntas-frequentes/cota-para-o-exercicio-da-atividade-parlamentar) 

## Acessando API do governo
- É preciso capturar os dados dos senadores/deputados das APIs do Senado e do Legislativo. Para isso, vamos usar a lib
**requests** do Python.
- Por padrão elas retornam em XML, então é preciso se atentar para passar o header informando a saída desejada:
```python
senadores = requests.get('http://legis.senado.leg.br/dadosabertos/senador/lista/atual', headers={'Accept':'application/json'}).json()
```
- Na API da camara é possivel acessar até mesmo os gastos dos deputados, apartir dos seus respectivos IDs. Isso permite
usar a API, e não os dados da Serenata de Amor, que estão meio desorganizados.  

## Built With
- [requests](https://2.python-requests.org/en/master/) para as requisições HTTP e APIs.
- [serenata-toolbox](https://github.com/okfn-brasil/serenata-toolbox) para a base de dados do projeto Serenata de Amor.
- [pandas](https://pandas.pydata.org/) para analise de dados e gráficos (com matplotlib).
---
