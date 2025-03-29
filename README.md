# Actividad-2---B-squeda-y-sistemas-basados-en-reglas

Codigo Utilizado para la actividad 

import networkx as nx

# Crear un grafo dirigido
G = nx.DiGraph()

# Agregar nodos y aristas con pesos
G.add_edge('A', 'B', weight=5)  # De A a B toma 5 minutos
G.add_edge('A', 'C', weight=10) # De A a C toma 10 minutos
G.add_edge('B', 'C', weight=2)  # De B a C toma 2 minutos
G.add_edge('C', 'D', weight=1)  # De C a D toma 1 minuto
G.add_edge('B', 'D', weight=7)  # De B a D toma 7 minutos

def encontrar_mejor_ruta(grafo, inicio, fin):
    # Usar el algoritmo de Dijkstra para encontrar la ruta más corta
    ruta = nx.dijkstra_path(grafo, inicio, fin)
    tiempo_total = nx.path_weight(grafo, ruta, weight='weight')
    return ruta, tiempo_total

# Definir los puntos de inicio y fin
punto_inicio = 'A'
punto_fin = 'D'

# Encontrar la mejor ruta
ruta, tiempo = encontrar_mejor_ruta(G, punto_inicio, punto_fin)

# Resultado
ruta, tiempo

Codigo creado y utilizado por Juan Esteban Rodriguez Culma y Hernan Alexander Batancourth Torres 
