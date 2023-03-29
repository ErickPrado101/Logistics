pip install googlemaps requests
import pandas as pd
import requests
import googlemaps
from datetime import datetime
#editar para por os endereços#
origem = ''
destino = ''
partida = datetime.now()
roteiro = gmaps.directions(origem, destino, mode="driving", departure_time=partida)

distancia = roteiro[0]['legs'][0]['distance']['value']
tempo = roteiro[0]['legs'][0]['duration']['value']

#alterar as dimensões do produto e os ceps's#
peso = x
comprimento = y
largura = z
altura =c 
cep_origem = ''
cep_destino = ''

url = f'https://ws.correios.com.br/calculador/CalcPrecoPrazo.aspx?nCdEmpresa=&sDsSenha=&sCepOrigem={cep_origem}&sCepDestino={cep_destino}&nVlPeso={peso}&nCdFormato=1&nVlComprimento={comprimento}&nVlAltura={altura}&nVlLargura={largura}&sCdMaoPropria=n&nVlValorDeclarado=0&sCdAvisoRecebimento=n&nCdServico=04510&nVlDiametro=0&StrRetorno=xml'
resposta = requests.get(url)

preco = float(resposta.content.decode().split('<Valor>')[1].split('</Valor>')[0].replace(',', '.'))
prazo = int(resposta.content.decode().split('<PrazoEntrega>')[1].split('</PrazoEntrega>')[0])

print(f'Distância total: {distancia/1000:.2f} km')
print(f'Tempo estimado de entrega: {tempo/60:.0f} minutos')
print(f'Preço do frete: R${preco:.2f}')
print(f'Prazo de entrega: {prazo} dias úteis')

#melhor trasportadora#
#
dados_transportadoras = pd.read_csv('dados_transportadoras.csv')

(ALTERAR OR EMPRESAS)

peso_preco = X
peso_tempo_entrega = Y

min_preco = dados_transportadoras['preco'].min()
max_preco = dados_transportadoras['preco'].max()
min_tempo_entrega = dados_transportadoras['tempo_entrega'].min()
max_tempo_entrega = dados_transportadoras['tempo_entrega'].max()
dados_transportadoras['preco_normalizado'] = (dados_transportadoras['preco'] - min_preco) / (max_preco - min_preco)
dados_transportadoras['tempo_entrega_normalizado'] = (dados_transportadoras['tempo_entrega'] - min_tempo_entrega) / (max_tempo_entrega - min_tempo_entrega)
dados_transportadoras['valor'] = peso_preco * dados_transportadoras['preco_normalizado'] + peso_tempo_entrega * dados_transportadoras['tempo_entrega_normalizado']
melhor_transportadora = dados_transportadoras.loc[dados_transportadoras['valor'].idxmin()]
print('Melhor transportadora:')
print('Nome:', melhor_transportadora['nome'])
print('Preço:', melhor_transportadora['preco'])
print('Tempo de entrega:', melhor_transportadora['tempo_entrega'])
print('Avaliação da qualidade do serviço:', melhor_transportadora['avaliacao'])


#melhor rota#
#
roteiro = gmaps.directions(origem, destino, mode="driving", departure_time=datetime.now())
distancia = roteiro[0]['legs'][0]['distance']['value']
tempo = roteiro[0]['legs'][0]['duration']['value']
coordenadas = []

for ponto in roteiro[0]['legs'][0]['steps']:
    coordenadas.extend(ponto['polyline']['points'])
    
print(f'Distância total: {distancia/1000:.2f} km')
print(f'Tempo estimado de viagem: {tempo/60:.0f} minutos')
print(f'Coordenadas dos pontos da rota: {coordenadas}')
#

