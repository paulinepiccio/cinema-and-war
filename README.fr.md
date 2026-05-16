> 🌍 **Langue** : Français · [English](README.md) 
> 
> 📖 Pour une réflexion narrative plus approfondie sur ce que ces données révèlent de la mémoire nationale, voir [l'essai en français](essay/essai.fr.md) · [the essay in English](essay/essay.md)

---

# 🎬 Cinema and War

Une analyse de données qui interroge la façon dont six industries cinématographiques nationales (États-Unis, Royaume-Uni, France, Allemagne, Russie et Japon) ont représenté les conflits armés au cinéma de 1945 à aujourd'hui. **2 343 films** étudiés, classifiés selon **26 conflits**.

---

## 🎯 Question de recherche

> **Comment les différentes industries cinématographiques nationales représentent-elles les conflits armés ?**

Le cinéma de guerre est souvent abordé comme un genre globalisé, mais chaque pays filme ses propres guerres, en ignore d'autres, et transforme la violence historique en mémoire nationale à son propre rythme. Ce projet cherche à mesurer cette fragmentation.

L'analyse s'articule autour de trois sous-questions :
- Quels conflits chaque pays choisit-il de filmer ?
- Chaque pays filme-t-il ses propres guerres ou celles des autres ?
- Combien de temps faut-il pour qu'une guerre devienne un film ?

---

## 🗂️ Le projet en bref

| Élément | Détail |
|---------|--------|
| **Pays analysés** | États-Unis · Royaume-Uni · France · Allemagne · Russie · Japon |
| **Période** | 1945–2025 |
| **Conflits cartographiés** | 26 (de la Seconde Guerre mondiale à la guerre russo-ukrainienne) |
| **Films analysés** | 2 343 au total · 1 445 classifiés à un conflit (taux d'efficacité de 66,1 %) |
| **Source de données** | API The Movie Database (TMDB) |
| **Outils** | Python, pandas, matplotlib, seaborn, plotly, Google Colab |

---

## ⚠️ Limites méthodologiques

- **La couverture anglocentrée de TMDB** sous-représente les cinémas non anglophones, en particulier les productions russes, japonaises et allemandes plus anciennes. Le filtrage adaptatif compense partiellement, sans pouvoir corriger totalement.
- **La classification par mots-clés** atteint une précision estimée à 80-85 %, mesurée sur un audit manuel stratifié de 30 films.
- **L'inclusion de la Seconde Guerre mondiale** est un choix méthodologique : bien que le projet couvre nominalement la période 1945+, WWII (1939-1945) y est intégrée comme conflit fondateur pour les six pays.
- **Les films hors-périmètre** (WWI, guerre de Sécession, conflits pré-modernes, science-fiction) sont explicitement repérés et exclus. Ils ont représenté 158 films au total.
- **La récupération de l'Union soviétique** : un défaut initial du pipeline manquait le cinéma russe pré-1991. La V2 a corrigé ce trou en récupérant 136 films classifiés.

---

## 🧭 Méthodologie

Le pipeline se déploie sur quatre notebooks, chacun pris en charge par une étape :

1. **`01_data_collection.ipynb`** : Interrogation de l'API TMDB pour récupérer tous les films du genre « guerre » depuis 1939, dans les six pays cibles (avec ajout de l'Union soviétique pour le cinéma russe pré-1991).
2. **`02_data_cleaning.ipynb`** : Déduplication des coproductions, suppression des entrées incomplètes, et filtrage adaptatif par pays pour limiter le biais anglocentré de la base TMDB.
3. **`03_conflict_mapping.ipynb`** : Classification en deux couches : matching par expressions régulières sur les synopsis, puis interrogation des mots-clés TMDB via API pour les films non matchés.
4. **`04_analysis_and_visualization.ipynb`** : Six analyses accompagnées de visualisations.

### Pourquoi deux couches de classification ?

La première passe sur les synopsis a permis de classifier 54 % des films grâce à un dictionnaire de mots-clés liés aux conflits, en utilisant des bornes de mots (`\b` en regex) pour éviter les faux positifs comme « ira » se déclenchant à l'intérieur de « iraqi ». Une seconde passe a interrogé l'API des mots-clés communautaires de TMDB pour les films restants, ajoutant 172 classifications supplémentaires. Après correction manuelle de toutes les incohérences temporelles, le dataset final atteint un taux d'efficacité de **66,1 %** (1 445 films classifiés sur 2 185 films « in-scope »).

### Une itération V2 à mentionner

Une première version du dataset présentait une anomalie frappante : zéro film russe classifié avant 1990. Après enquête, il s'est avéré que TMDB indexe les films de l'ère soviétique sous le code pays `SU` (et non `RU`). La collecte initiale avait donc raté près d'un demi-siècle de l'une des cinématographies de guerre les plus riches au monde. Le pipeline a été itéré pour inclure `SU` puis fusionner les résultats avec `RU`, récupérant ainsi 136 films classifiés supplémentaires, et rendant possible la comparaison avec l'âge d'or du cinéma soviétique.

---

## 📊 Résultats clés

### Volume par pays

<img width="801" height="452" alt="image" src="https://github.com/user-attachments/assets/115a960b-4779-475e-ba8f-4f5388f6c6f6" />

Les États-Unis représentent près de la moitié des films classifiés (44,9 %), suivis du Royaume-Uni (17,6 %). La Russie/URSS arrive en troisième position (14,4 %), portée à la fois par les classiques soviétiques et la production contemporaine. Le Japon ferme la marche à 4,3 %, en cohérence avec son rôle militaire constitutionnellement limité depuis 1947.

⚠️ Ce volume absolu reflète à la fois la taille des industries et la couverture anglocentrée de TMDB. Pour pallier ces déséquilibres, les analyses qui suivent raisonnent toutes en proportions internes à chaque pays.

### Évolution temporelle

<img width="1080" height="422" alt="image" src="https://github.com/user-attachments/assets/b092d22b-9c90-4314-997f-79d7d7d97d4c" />

[![Temporal evolution chart](outputs/figures/02_temporal_evolution.png)](notebooks/04_analysis_and_visualization.ipynb#scrollTo=cell-8)

> 💡 **Version interactive**

Cinq des six pays atteignent leur pic historique dans les années 2010. La Russie fait exception : elle culmine dans les années 1960 (21,6 %), pendant l'âge d'or soviétique du cinéma sur la Grande Guerre patriotique, avant un effondrement dans les années 1990 (5,3 %) puis un redressement soutenu par l'État. La France dessine une courbe en U remarquable : production très faible dans l'après-guerre (4,2 à 4,8 % dans les années 1940-50), bond dans les années 1960 (15,6 %) puis montée régulière jusqu'au pic des années 2010 (22,2 %).

### Signatures cinématographiques par pays

<img width="1947" height="2376" alt="03_heatmap_conflict_country" src="https://github.com/user-attachments/assets/24f98d43-628b-4ded-a6e7-57c3971012a4" />

La Seconde Guerre mondiale domine partout, mais inégalement : de 65,9 % (États-Unis) à 95,2 % (Japon), soit un écart de 30 points. Au-delà de la Seconde Guerre, des signatures nationales claires émergent :

- **France ↔ guerre d'Algérie** (5,4 %, quasi-exclusivité française)
- **Russie ↔ guerres de Tchétchénie** (3,8 % sur la première guerre de Tchétchénie, exclusivité russe)
- **Allemagne ↔ guerre froide** (5,7 %, la part la plus élevée de tous les pays)
- **Royaume-Uni ↔ Malouines et Irlande du Nord** (1,6 % et 1,2 %)
- **États-Unis ↔ une guerre par décennie** (Vietnam, Afghanistan, Irak, Corée, Golfe)
- **Japon ↔ Seconde Guerre mondiale quasi exclusivement** (95,2 %)

### Narration de soi vs narration de l'autre

<img width="1205" height="585" alt="image" src="https://github.com/user-attachments/assets/971621d6-9b35-49e2-b6ac-5a582ab8a947" />

Les six pays consacrent 92 à 99 % de leurs films de guerre à des conflits dans lesquels ils ont été impliqués. Mais ce chiffre est mécaniquement gonflé par la Seconde Guerre mondiale.

<img width="1197" height="581" alt="image" src="https://github.com/user-attachments/assets/c80e0eee-fd93-485f-99ed-764f8252c533" />

Une fois celle-ci retirée, trois groupes se dessinent :

- **Cinémas auto-centrés** (90 % et + de « self ») : États-Unis, France
- **Cinémas mixtes** : Royaume-Uni (75/25), Russie (67/33)
- **Cas atypiques** : Allemagne (50/50, le cinéma le plus ouvert sur l'étranger) ; Japon (0/100, ses trois films non-WWII traitent uniquement de conflits étrangers)

Un cas particulièrement intéressant : les 7 films russes non-WWII de « narration de l'autre » traitent tous de la guerre d'Afghanistan post-2001, conflit américano-occidental auquel la Russie n'a pas pris part. Le cinéma russe revisite cette guerre américaine comme un miroir de sa propre expérience afghane (1979-89).

### Décalage temporel

<img width="1301" height="582" alt="image" src="https://github.com/user-attachments/assets/8433f52a-0eac-478b-9b8f-4bf22c330e52" />

Le cinéma de guerre est massivement un cinéma de mémoire : 74,5 % des films sortent plus de 10 ans après la fin du conflit. Seuls 10,9 % sont tournés pendant le conflit lui-même. Mais chaque pays a son propre rythme :

- **Les États-Unis filment « à chaud »** : 34 % de leurs films sortent dans les 10 ans suivant la fin du conflit
- **Le Japon filme « à froid »** : 95,2 % en mémoire longue
- **La Russie (84,1 % en mémoire longue)** rejoint le profil japonais, malgré ses conflits récents

Les conflits eux aussi suivent des rythmes radicalement différents. Conflits « à chaud » : Afghanistan (83 % pendant), guerre froide (54 %), guerre d'Irak (52 %). Conflits « à froid » : Seconde Guerre mondiale (87 % en mémoire longue), guerre d'Algérie (80 %), guerre du Vietnam (62 %).

### Conflits universels vs nationaux

<img width="2592" height="1968" alt="06_universality_ranking" src="https://github.com/user-attachments/assets/3a47b08a-3784-4af5-8623-dfb678ac0457" />

Sur les 26 conflits, seulement 5 (19 %) sont filmés par 5 à 6 pays. Et ces « universels » sont fortement dominés par Hollywood (Vietnam : 85 % américain ; Afghanistan : 63 %). La Seconde Guerre mondiale est le seul conflit véritablement universel et équilibré. Quatre conflits constituent de vraies signatures nationales (90 % et + venant d'un seul pays non-américain) : guerre d'Algérie (FR), première guerre de Tchétchénie (RU), guerre des Malouines (UK), conflit nord-irlandais (UK).

---

## 🎯 Ce que les données révèlent

Une fois agrégé sur six pays et 26 conflits, le cinéma de guerre apparaît moins comme un genre globalisé que comme un ensemble de conversations nationales autour de la mémoire.
La Seconde Guerre mondiale est le seul sujet véritablement universel : tous les pays la filment, chacun selon son propre angle. Au-delà, les asymétries deviennent frappantes : Hollywood filme les guerres américaines presque en temps réel, la France a mis des décennies avant de s'engager cinématographiquement sur la guerre d'Algérie et l'Allemagne répartit son regard à parts égales entre ses propres conflits et ceux des autres. La Russie ancre son cinéma dans la Grande Guerre patriotique tout en revisitant ponctuellement la guerre américaine en Afghanistan comme un miroir de sa propre expérience soviétique. Le Japon, sous le pacifisme constitutionnel de l'article 9 de sa constitution (1947), concentre 95 % de son cinéma de guerre sur un unique conflit (WWII). Le Royaume-Uni fragmente son regard à travers les échos de son empire colonial, tout en laissant certains chapitres (comme l'insurrection des Mau Mau) presque inexplorés à l'écran.

À travers ce corpus, le cinéma de guerre ne reflète pas seulement ce qui s'est passé : il révèle ce que chaque pays a choisi de garder en mémoire sur ses écrans (et ce qu'il a choisi de passer sous silence).

> 📖 Pour une exploration narrative plus approfondie de ces résultats, voir [l'essai](essay/essai.fr.md).
