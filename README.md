# Micromania
Analyse des jeux vidéos vendus dans les magasins Micromania en Amérique du Nord en Europe et au Japon.

![micromania logo](https://github.com/Aurelie9/Micromania/assets/161243335/55b3c028-1615-4f59-8b96-57643f5784b9)

![micromania_vidéo](https://github.com/Aurelie9/Micromania/assets/161243335/74f0f1c0-b11f-40dc-9107-0b94e00b00d1)


## Analyse n°1
> Analyse des ventes des jeux vidéos au Japon

```python
import pandas as pd
import matplotlib.pyplot as plt

# Supposons que vous ayez déjà chargé vos données dans le DataFrame ventes_par_genre

# Calculer les ventes totales par genre au Japon
ventes_totales_par_genre = df.groupby('Genre')['JP_Sales'].sum().sort_values(ascending=False)

# Afficher un graphique barplot des ventes par genre au Japon
plt.figure(figsize=(10, 6))
ventes_totales_par_genre.plot(kind='bar', color='skyblue')
plt.title('Ventes par genre de jeux vidéo au Japon')
plt.xlabel('Genre')
plt.ylabel('Ventes au Japon (en millions)')
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()
```
![Vente de jeux vidéos au Japon](https://github.com/Aurelie9/Micromania/assets/161243335/11532ae5-6d7e-4eb7-ba0d-a23b74834f94)

## Analyse n°2 
> Analyse des ventes des jeux vidéos entre l'Europe et l'Amérique du Nord
```python
# Calcul de la corrélation entre les ventes en Amérique du Nord et en Europe
correlation = df['NA_Sales'].corr(df['EU_Sales'])

print(f"La corrélation entre les ventes en Amérique du Nord et en Europe est : {correlation}")
# Calculer la matrice de corrélation
correlation_matrix = df.corr()

# Afficher le graphique de la matrice de corrélation
plt.figure(figsize=(12, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f")
plt.title("Matrice de Corrélation des Ventes de Jeux Vidéo par Région")
plt.show()
```

![Analyse 3 micromania](https://github.com/Aurelie9/Micromania/assets/161243335/ba597b54-1db5-4056-84da-65fdd9925911)
> La corrélation entre les ventes en Amérique du Nord et en Europe est : 0.7677666590359654. Dans le contexte des ventes de jeux vidéo par région, une corrélation positive élevée entre les ventes en Amérique du Nord et les ventes en Europe, pourrait indiquer que les jeux qui se vendent bien en Amérique du Nord ont tendance à se vendre également bien en Amérique du Sud.

## Analyse n°3
> Quelle est la région contribuant le plus aux ventes mondiales
```python
import matplotlib.pyplot as plt

# Données de vente par région (Amérique du Nord, Europe, Japon, Autres régions, Ventes mondiales)
ventes_par_region = {
    'Amérique du Nord': 500,
    'Europe': 300,
    'Japon': 200,
    'Autres régions': 150,
    'Ventes mondiales': 1150
}

# Création des données pour le graphique
regions = list(ventes_par_region.keys())
ventes = list(ventes_par_region.values())

# Création du diagramme à barres
plt.figure(figsize=(10, 6))
plt.bar(regions, ventes, color='blue')

# Ajout de titres et d'étiquettes
plt.title('Ventes de jeux vidéo par région')
plt.xlabel('Région')
plt.ylabel('Ventes (en millions)')
plt.xticks(rotation=45)

# Affichage du graphique
plt.tight_layout()
plt.show()
```


![analyse 4](https://github.com/Aurelie9/Micromania/assets/161243335/3095d4e2-2b6b-497b-b176-b2bf249d53b5)

