
<h1 align="center">
<br>
  <img src="https://github.com/Caiocof/caiocof/blob/main/python.png?raw=true" alt="PYTHON" width="120">
<br>
<br>
Estudo de Regressão Linear 01
</h1>

<p align="center">Nesse projeto vamos analisar o consumo de cerveja no ano de 2015</p>


<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License MIT">
  </a>
</p>


## Iniciando o Notebook
 - Com o anaconda instalado na maquina de dois clique no arquivo "Start Jupyter.bat" ou abrir o seu Jupyter e navegue ate a pasta
 - Com o projeto aberto reset todas as células

## Objetivo
- Analisar o consumo de cerveja naquele ano e criar um modelo preditivo para o possível aumento ou redução no consumo

## Como usar o modelo criado
```python
import pickle

#faz a importação do arquivo que tem o modelo
modelo = open('modelo_consumo_cerveja','rb')
lm_new = pickle.load(modelo)
modelo.close()

#criar as variaveis para verificar o consumo de cerveja

#temperatura máxima previsca
temp_max = 30.5

#chuva prevista em (mm)
chuva = 12.2

#se sera no fim de semana ou não
#1 = True, 0 = False
fds = 0

#cria nossa entrada e passa para o modelo
entrada = [[temp_max, chuva, fds]]
print('{0:.2f} litros'.format(lm_new.predict(entrada)[0]))
```

## Fonte dos dados
- https://www.kaggle.com/
