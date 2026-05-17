> **Language**: English · [Français](README.fr.md)
> 
> For a longer narrative reflection on what this data reveals about national memory, see [the essay](essay/essay.md) · [l'essai en français](essay/essai.fr.md)

---

# 🎬 Cinema and War

A data analysis of how six national film industries (USA, UK, France, Germany, Russia, and Japan) have portrayed armed conflicts in cinema from 1945 to today. Based on **2,343 films** classified across **26 conflicts**.

---

## 🎯 Research question

> **How do different national film industries portray armed conflicts?**

War cinema is often discussed as a global genre, but every country films its own wars, ignores certain conflicts, and turns historical violence into national memory at its own pace. This project tries to quantify that fragmentation.

The analysis focuses on three sub-questions:
- Which conflicts does each country choose to film?
- Does each country film its own wars or those of others?
- How long does a war take to become a film?

---

## 🗂️ Project at a glance

| Element | Detail |
|---------|--------|
| **Countries analyzed** | USA · UK · France · Germany · Russia · Japan |
| **Time period** | 1945–2025 |
| **Conflicts mapped** | 26 (from WWII to the Russo-Ukrainian War) |
| **Films analyzed** | 2,343 total · 1,445 classified to a specific conflict (66.1% effective rate) |
| **Data source** | The Movie Database (TMDB) API |
| **Tools** | Python, pandas, matplotlib, seaborn, plotly, Google Colab |

---

## ⚠️ Methodological limitations

- **TMDB's anglo-centric coverage** under-represents non-English cinemas. Adaptive filtering partially compensates but doesn't fully correct.
- **Keyword-based classification** has an estimated accuracy of 80–85%, validated on a stratified manual audit of 30 films.
- **WWII inclusion** : although the project nominally covers 1945+, WWII (1939–1945) is included as the foundational conflict for all six countries.
- **Out-of-scope films** (WWI, American Civil War, pre-modern conflicts, sci-fi war films) are explicitly flagged and excluded, representing 158 films total.
- **Soviet Union recovery** : an initial pipeline bug missed pre-1991 Russian cinema. V2 fix recovered 136 additional classified films.

---

## 🧭 Methodology

The pipeline runs across four notebooks, each handling one stage :

1. **`01_data_collection.ipynb`** : Querying the TMDB API for all war-genre films from 1945 onwards, across the 6 target countries (plus Soviet Union for pre-1991 Russian cinema).
2. **`02_data_cleaning.ipynb`** : Deduplication of co-productions, removal of incomplete records, and adaptive filtering to balance representation across cinema industries.
3. **`03_conflict_mapping.ipynb`** : Two-layer classification : regex-based matching on film synopses, then TMDB-curated keywords via API for unmatched films.
4. **`04_analysis_and_visualization.ipynb`** : Six analyses with visualizations.

### Two layers of classification

A first pass on film synopses matched 54% of films using a curated dictionary of conflict-related keywords, with regex word boundaries to avoid false positives (e.g., "ira" matching inside "iraqi"). A second pass queried TMDB's community-curated keywords API for the remaining films, recovering 172 additional matches. After manual corrections of all temporal inconsistencies, the final dataset reaches an effective matching rate of **66.1%** (1,445 classified films out of 2,185 in-scope films).

### A V2 fix worth mentioning

An initial version showed a striking anomaly : Russia had zero classified films before 1990. Investigation revealed that TMDB tags Soviet-era films under country code `SU` (not `RU`), so the initial collection had missed nearly half a century of one of the world's richest war cinemas. I iterated on the pipeline to include `SU` and merge it into `RU`, recovering 136 additional classified films and enabling proper comparison with Soviet golden-age cinema.

This was a useful methodological lesson : when a dataset shows a strikingly anomalous gap, the first suspect should be the data pipeline itself rather than the underlying phenomenon.

---

## 📊 Key results

### Volume by country

<img width="801" height="452" alt="image" src="https://github.com/user-attachments/assets/115a960b-4779-475e-ba8f-4f5388f6c6f6" />


The USA contributes nearly half of classified films (44.9%), followed by the UK (17.6%). Russia/USSR sits third at 14.4%, driven by both Soviet-era classics and contemporary productions. Japan trails at 4.3%, consistent with its constitutionally-limited military role since 1947.

⚠️ This absolute volume reflects both US industry size and TMDB's anglo-centric coverage. All subsequent analyses use proportions within each country.

### Temporal evolution


<img width="1080" height="422" alt="image" src="https://github.com/user-attachments/assets/b092d22b-9c90-4314-997f-79d7d7d97d4c" />

[![Temporal evolution chart](outputs/figures/02_temporal_evolution.png)](notebooks/04_analysis_and_visualization.ipynb#scrollTo=cell-8)

> 💡 **Interactive version** : click the image above to open the notebook 
> with zoom, range slider, and hover details enabled.

Five of six countries reach their historical peak in the 2010s. Russia is the only exception : it peaks in the 1960s (21.6%), during the Soviet golden age of WWII cinema, with a sharp collapse in the 1990s (5.3%) and a state-supported revival afterwards. France shows a striking U-curve : low post-war output (4.2–4.8% in the 1940s–50s), a 1960s jump (15.6%), and a steady rise to its 2010s peak (22.2%).

### Conflict signatures

<img width="1947" height="2376" alt="03_heatmap_conflict_country" src="https://github.com/user-attachments/assets/24f98d43-628b-4ded-a6e7-57c3971012a4" />


WWII dominates everywhere but unevenly : from 65.9% (USA) to 95.2% (Japan), a 30-point gap. Beyond WWII, national signatures emerge clearly :
- **France ↔ Algerian War** (5.4%, near-exclusive)
- **Russia ↔ Chechen Wars** (3.8%, exclusive)
- **Germany ↔ Cold War** (5.7%, the highest share of any country)
- **UK ↔ Falklands and Northern Ireland** (1.6% and 1.2%)
- **USA ↔ a war for every decade** (Vietnam, Afghanistan, Iraq, Korea, Gulf War)
- **Japan ↔ WWII almost exclusively** (95.2%)

### Self vs Other narration

<img width="1205" height="585" alt="image" src="https://github.com/user-attachments/assets/971621d6-9b35-49e2-b6ac-5a582ab8a947" />

All six countries devote 92–99% of their war films to conflicts they were involved in. But this is mechanically inflated by WWII. 

<img width="1197" height="581" alt="image" src="https://github.com/user-attachments/assets/c80e0eee-fd93-485f-99ed-764f8252c533" />

Once WWII is removed, three groups emerge :

- **Self-centered** (90%+ self) : USA, France
- **Mixed** : UK (75/25), Russia (67/33)
- **Outliers** : Germany (50/50, the most internationally-engaged) ; Japan (0/100, all the 3 non-WWII films treat foreign wars)

One surprising case : Russia's 7 non-WWII "other" films all treat the post-2001 War in Afghanistan, an American-led conflict in which Russia did not participate. Russian cinema probably revisits this American war as a mirror of the USSR's own Afghan experience (1979–89).

### Time lag

<img width="1301" height="582" alt="image" src="https://github.com/user-attachments/assets/8433f52a-0eac-478b-9b8f-4bf22c330e52" />

War cinema is overwhelmingly a cinema of memory : 74.5% of films are released more than 10 years after their conflict ended. Only 10.9% are filmed during the conflict itself. But each country has its own rhythm :

- **USA films "hot"** : 34% within 10 years of conflict end (most contemporary)
- **Japan films "cold"** : 95.2% long-term memory (most retrospective)
- **Russia (84.1% long-term)** echoes Japan, despite recent conflicts

<img width="1197" height="732" alt="image" src="https://github.com/user-attachments/assets/aa8b8f17-189b-44aa-99e4-d34c12e158be" />

Conflicts also follow different timelines. Hot : Afghanistan (83% during), Cold War (54%), Iraq (52%). Cold: WWII (87% long-term), Algerian War (80%), Vietnam (62%).

### Universal vs national conflicts

<img width="2592" height="1968" alt="06_universality_ranking" src="https://github.com/user-attachments/assets/3a47b08a-3784-4af5-8623-dfb678ac0457" />

Of 26 conflicts, only 5 (19%) are filmed by 5–6 countries, and even those are heavily US-dominated (Vietnam : 85% American ; Afghanistan : 63%). WWII is the only truly balanced universal subject. Four conflicts are true national signatures (90%+ from a single non-US country) : Algerian War (FR), First Chechen War (RU), Falklands War (UK), Northern Ireland Troubles (UK).

------

## 🎯 What the data ultimately tells us

When we aggregate 2,343 films across six countries and 26 conflicts, what emerges is less a global genre than a series of national conversations about memory.

WWII is the only conflict that genuinely unites all six countries cinematically, though each films it from its own angle : liberation in France, occupation in Germany, atomic trauma in Japan, the Great Patriotic War in Russia. Beyond WWII, each country largely keeps to its own wars and to its own silences.

The USA stands out for filming most of its modern conflicts in near-real time, with Hollywood acting as a constant chronicler of American military engagements. France has the opposite rhythm : decades of avoidance before slowly engaging with the Algerian War and the colonial past. Germany, paradoxically, has the most internationally-oriented gaze, splitting its non-WWII cinema evenly between its own engagements and foreign wars. Russia anchors most of its cinema in WWII memory, even as it occasionally turns to the contemporary American war in Afghanistan with a critical perspective shaped by its own Soviet experience. Japan concentrates 95% of its war cinema on WWII, in line with the constitutional pacifism of Article 9 (1947). And the UK fragments its gaze across imperial echoes (Falklands, Northern Ireland, occasionally Vietnam) while passing over some of its own colonial chapters, like the Mau Mau Uprising, almost in silence.

What this dataset shows, ultimately, is that war cinema reflects not only what happened, but what each country has chosen to remember on screen.

> 📖 For a longer narrative exploration of these findings, see [the essay](essay/essay.md).
