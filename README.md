# Projeto-Beijo-de-Moca
Projeto final da disciplina de Estatística aplicada a computação


## Links uteis
- [serenata-toolbox](https://github.com/okfn-brasil/serenata-toolbox)
- [API para acessar os dados dos senadores](http://legis.senado.leg.br/dadosabertos/docs/resource_ListaSenadorService.html#resource_ListaSenadorService_cargosSenadorXml_GET)  
- [API para acessar os dados dos deputados](https://dadosabertos.camara.leg.br/swagger/api.html)


## Acessando API do governo
- É preciso capturar os dados dos senadores/deputados das APIs do Senado e do Legislativo. Para isso, vamos usar a lib
**requests** do Python.
- Por padrão elas retornam em XML, então é preciso se atentar para passar o header informando a saída desejada:
```python
senadores = requests.get('http://legis.senado.leg.br/dadosabertos/senador/lista/atual', headers={'Accept':'application/json'}).json()
```
- Na API da camara é possivel acessar até mesmo os gastos dos deputados, apartir dos seus respectivos IDs. Isso permite
usar a API, e não os dados da Serenata de Amor, que estão meio desorganizados.
