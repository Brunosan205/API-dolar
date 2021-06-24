import requests
import json
 
api = requests.get("https://economia.awesomeapi.com.br/all/USD-BRL,EUR-BRL,BTC-BRL")

info = api.json()
data = api.json()

vdolar=float(info["USD"]["bid"])
dataD= data["USD"]["create_date"]

veuro=float(info["EUR"]["bid"])
dataEuro = data["EUR"]["create_date"]

moeda = int(input('Qual a Moeda converter: [1]Dolar [2]Euro '))

if moeda == 1:
    vreal = float(input('Digite o valor em Real: '))
    vconvertidoD = vreal/vdolar
    print('Na data de ' + dataD + ', o valor convertido é '+ str(round(vconvertidoD,2)) + ' dólares')

else:
    moeda == 2
if moeda == 2:   
    vreal = float(input('Digite o valor em Real: '))
    vconvertidoE = vreal/veuro
    print('Na data de ' + dataEuro + ', o valor convertido é '+ str(round(vconvertidoE,2)) + ' euros')
