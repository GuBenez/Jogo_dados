
from random import randint
from time import sleep
from operator import itemgetter
#itemgetter colocar o dicionário em ordem
jogadores = {"jogador 1" : randint(1, 6),
             "jogador 2" : randint(1,6),
             "jogador 3" : randint(1,6),
             "jogador 4" : randint(1,6)}
ranking = []
print("Os valores Sorteados foram: ")
for k, v in jogadores.items():
    print(f"O {k} tirou {v}")
    sleep(1)
print("-=" * 30)
ranking = sorted(jogadores.items(), key = itemgetter(1), reverse = True)

for i, v in enumerate(ranking):
    print(f"O {i+1}º lugar ficou o {v[0]} com {v[1]}.")