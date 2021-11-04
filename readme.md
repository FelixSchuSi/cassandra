# Cassandra

## Mit DB aus pyhton verbinden
```python
from cassandra.cluster import Cluster
print("Connecting...")
cluster = Cluster(['cassandra'])
session = cluster.connect()
print("Connection Established")
dir(cluster) # Wenn hier alle Funktionen & Properties geloggt werden hat es geklappt
```

## Mögliche Datensätze
1. [Steam Daten](https://cseweb.ucsd.edu/~jmcauley/datasets.html#steam_data)

    Mögliche Aufgabenstellung könnte sein, dass regelmäßig reccomender systems trainiert werden.
    Daher muss Cassandra immer Daten dafür bereitstellen
    Z. B. Spieler die > 100 Stunden in Spiel X gespielt haben spielen auch 

2. [Andere Daten für Recomender Systems](https://cseweb.ucsd.edu/~jmcauley/datasets.html)

    Sind z. B. Amazon Reviews, Twitch Daten(Welcher User guckt welchen Streamer), fitness tracking data

3. Sonst ist [Google Dataset Search](https://datasetsearch.research.google.com/) eine gute Quelle

    
### Docker snippets

Alle Images entfernen
```
docker rmi -f $(docker images -a -q)
```

Alle Container entfernen
```
docker rm -f $(docker ps -qa)
```

Alle Networks aufzählen
```
docker network ls
# Alle networks ohne Referenz entfernen
docker network prune
# Networks manuell entfernen
docker network rm <ID>
```

Alle Volumes aufzählen
```
docker volume ls
# Alle volumes ohne Referenz entfernen
docker volume prune
# Volumes manuell entfernen
docker volume rm <ID>
```