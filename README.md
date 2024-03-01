# Micromania
Analyse des jeux vidéos vendus dans les magasins Micromania en Amérique du Nord en Europe et au Japon.

## Exemple d'une analyse
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
