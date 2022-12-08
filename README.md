# Desafio Cientista de Dados



Nesse projeto, exploramos um conjunto de informações de bairros para identificar melhores localizações de São Paulo para novas filias de um empreendimento alimentício que atua no Rio de Janeiro.  Além disso, realizamos a tarefa de predição potencial, também realizamos a previsão do faturamento esperado por bairro .

## ![zap](https://github.githubassets.com/images/icons/emoji/unicode/26a1.png) **Tecnologias**

- Pandas
- Seaborn
- Matplotlib
- Scikit-learn
- dentre outras...

## ![hammer_and_wrench](https://github.githubassets.com/images/icons/emoji/unicode/1f6e0.png)Como executar o projeto

A pasta *dataset* contém a seguinte estrutura, contendo além do dataset do desafio o [Limite_de_Bairros.zip](https://www.data.rio/datasets/PCRJ::limite-de-bairros/) e [idh_rio.xls](https://www.data.rio/documents/58186e41a2ad410f9099af99e46366fd).

```
.
├── DadosDesafioCientista.csv
├── DadosDesafioCientista.xlsx
└── rio-de-janeiro
    ├── idh_rio.xls
    ├── Limite_de_Bairros.zip
    ├── rio_geo.csv
    └── wiki_rj.json
```

Para melhor reprodução do experimento, criamos um Dockerfile.


```bash
docker build -t app-geo .
docker run -d --name app-geo -p 8889:8888 -v "$(pwd)"/dataset:/content/Dados -v "$(pwd)"/src:/content/src app-geo
```

