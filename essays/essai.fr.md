> 🌍 **Langue** : Français · [English](essay.md)
> 
> 🛠️ Pour la méthodologie et le code, voir le [README technique](../README.fr.md).

---

# Cinéma et guerre : ce que les nations choisissent de filmer

*Réflexion à partir de l'analyse de 2 343 films de guerre dans six cinématographies nationales (1945-2025).*

---

## Introduction

Quand un pays produit un film de guerre, il fait deux choses à la fois : il représente un conflit, et il fabrique une mémoire. *Apocalypse Now* (1979) ne dit pas le Vietnam : il dit l'Amérique vietnamienne, c'est-à-dire un récit américain sur une guerre où l'Amérique a été défaite. Entre l'événement et son film, il y a toujours un choix : choix de filmer ou de se taire, choix d'attendre ou de filmer dans l'urgence, choix de raconter une guerre qui est la sienne ou une guerre qui ne l'est pas. C'est ce choix, dans ses régularités et ses dissonances, qui intéresse ce travail.

À partir d'un corpus de 2 343 films produits entre 1945 et 2025 dans six pays (États-Unis, Royaume-Uni, France, Allemagne, Russie et Japon) et classifiés selon 26 conflits armés, il s'est agi de mesurer ce qui, dans le genre apparemment globalisé du film de guerre, relève en réalité de mémoires nationales fragmentées et asymétriques. Les chiffres, à eux seuls, ne disent pas grand-chose ; mais croisés avec le contexte géopolitique de chaque pays, ils dessinent une géographie singulière de l'amnésie et de la commémoration. 

*La méthodologie complète qui a permis de constituer ce corpus est exposée à la fin du document.*

Trois questions, prises ensemble, structurent l'analyse. Y a-t-il, d'abord, un cinéma de guerre, ou plusieurs ? Au-delà d'un référent commun (la Seconde Guerre mondiale), les volumes et les rythmes nationaux divergent profondément, au point qu'on peut douter de l'unité du genre. Mais admettre cette pluralité, c'est aussitôt se demander ce que chaque cinéma national choisit de représenter, et surtout ce qu'il choisit de taire : que filme-t-on, dès lors qu’on filme une guerre ? Reste enfin la dimension la plus discrète, et peut-être la plus instructive, celle du temps. Quand filme-t-on la guerre ? Certaines sont filmées presque en temps réel ; d'autres demandent une génération de silence avant de pouvoir devenir image. Ces trois interrogations, du général au particulier puis du particulier au temporel, dessinent un cinéma de guerre moins universel qu'il n'y paraît.

---

## I. Y a-t-il un cinéma de guerre, ou plusieurs ?

La première observation, qui pourrait passer pour une évidence, mérite d'être posée pour ce qu'elle révèle ensuite. À première vue, les six pays étudiés produisent tous des films de guerre, et tous filment massivement le même conflit fondateur : la Seconde Guerre mondiale. Vu de loin, l'unité du genre semble acquise.

<img width="801" height="452" alt="image" src="https://github.com/user-attachments/assets/115a960b-4779-475e-ba8f-4f5388f6c6f6" />

Pourtant, dès qu'on regarde de plus près les volumes produits, l'asymétrie crève les yeux. Les États-Unis représentent à eux seuls près de la moitié du corpus classifié (44,9 %), suivis de loin par le Royaume-Uni (17,6 %). La Russie (14,4 %), la France (11,6 %), l'Allemagne (7,3 %) et le Japon (4,3 %) ferment la marche dans cet ordre. Hollywood n'est pas simplement *un* cinéma de guerre parmi d'autres : c'est, statistiquement, *le* cinéma de guerre mondial. À lui seul, le déséquilibre entre les États-Unis et le Japon (plus de dix fois plus de films côté américain) suggère que ce qu'on appelle « cinéma de guerre » ne désigne pas une réalité unifiée mais une géographie de production très inégalement répartie. On notera, du reste, que ce volume reflète à la fois la taille des industries nationales et la couverture anglo-centrée de la base TMDB, qui sous-représente structurellement les cinématographies non anglophones. 

C'est en examinant la temporalité de cette production que le diagnostic se précise. Cinq des six pays atteignent leur pic historique dans les années 2010, dans ce qui apparaît comme un boom contemporain du genre, sans doute lié à la fois aux plateformes de streaming, aux commémorations d'anniversaire (Seconde Guerre mondiale, Vietnam) et aux conflits ouverts (Irak, Afghanistan, Syrie, Ukraine). Tous, sauf un : la Russie.

<img width="1080" height="422" alt="image" src="https://github.com/user-attachments/assets/b092d22b-9c90-4314-997f-79d7d7d97d4c" />

[![Temporal evolution chart](outputs/figures/02_temporal_evolution.png)](notebooks/04_analysis_and_visualization.ipynb#scrollTo=cell-8)

> 💡 **Version interactive**

La Russie est le seul pays dont le pic ne se situe pas dans les années 2010, mais dans les années 1960 (21,6 %), suivi d'un second sommet dans les années 1970 (17,3 %). Ce n'est pas un détail. Ce double pic correspond à l'âge d'or du cinéma soviétique sur la « Grande Guerre patriotique », celui de Tarkovski et de *L'Enfance d'Ivan* (1962), de Kalatozov et de *Quand passent les cigognes* (1957). C'est aussi l'époque où, sous Khrouchtchev puis Brejnev, la mémoire de 1945 devient le ciment idéologique d'un pouvoir soviétique en quête de légitimité post-stalinienne. Le profond effondrement des années 1990 (5,3 %) raconte, en miroir, la dislocation de l'industrie cinématographique russe après la chute de l'URSS, avant un redressement post-2000 largement soutenu par l'État poutinien. Ce profil temporel singulier, qu'aucun autre pays ne partage, suffit déjà à rendre caduque l'idée d'un cinéma de guerre unifié à l'échelle mondiale.

La France, à sa manière, présente un autre profil atypique : une courbe en U remarquable, avec une production très basse dans l'immédiat après-guerre (4,2 à 4,8 % dans les années 1940-50, soit la part la plus faible de tous les pays occidentaux à cette période), un bond dans les années 1960 (15,6 %), puis une montée régulière jusqu'au pic des années 2010 (22,2 %). Ce silence post-1945, étonnamment long, en dit long sur la mémoire complexe de l'Occupation et de la collaboration, que le cinéma français a longtemps préféré contourner. Cette relative discrétion ne signifie pas que la France ne filme pas du tout sa Seconde Guerre : La Bataille du rail (1946) ou Le Silence de la mer (1949) en témoignent dès l'après-guerre. Mais ce que ces films représentent majoritairement, c'est la France résistante, conformément au récit national construit par de Gaulle après 1944. Il faudra attendre Le Chagrin et la Pitié de Marcel Ophüls (1969), puis Lacombe Lucien de Louis Malle (1974), pour que le cinéma français commence véritablement à filmer la zone grise : la collaboration, l'antisémitisme d'État, les ambiguïtés de Vichy. Il y a là un cas, déjà, où le silence cinématographique est un fait historique en soi.

Si donc on peut parler d'« un » cinéma de guerre, c'est seulement au sens où plusieurs cinématographies nationales coexistent sous une étiquette commune. La réalité statistique impose plutôt l'inverse : il existe **des** cinémas de guerre, profondément différents par leurs volumes, leurs rythmes et leurs centres de gravité historiques.

---

## II. Que filme-t-on quand on filme une guerre ?

Une fois admise la pluralité du genre, reste à comprendre ce qui le différencie. Si chaque pays filme la guerre à sa manière, c'est d'abord parce qu'il ne filme pas les mêmes guerres. La cartographie des conflits, croisée avec les pays producteurs, dessine ce qu'on pourrait appeler des **signatures nationales**.

<img width="1947" height="2376" alt="03_heatmap_conflict_country" src="https://github.com/user-attachments/assets/24f98d43-628b-4ded-a6e7-57c3971012a4" />

Cette heatmap fait apparaître presque mécaniquement une diagonale d'appropriations. La Seconde Guerre mondiale domine partout, mais inégalement : de 65,9 % aux États-Unis à 95,2 % au Japon, soit un écart de trente points. Ce chiffre japonais, à lui seul, mérite qu'on s'y arrête. Que le Japon consacre 95 % de son cinéma de guerre à un seul conflit n'est pas un trait culturel énigmatique : c'est la conséquence directe de l'article 9 de sa Constitution de 1947, par lequel le pays « renonce à jamais à la guerre comme droit souverain de la nation ». Si l'on peut filmer une guerre, encore faut-il en avoir une à filmer. Le cinéma japonais, privé depuis 1947 d'engagements militaires substantiels, est condamné à revenir au conflit de 1939-1945, vu depuis Hiroshima, Nagasaki, les bombardements de Tokyo et la mémoire impériale jamais entièrement réglée.

À l'autre extrémité du spectre, les États-Unis affichent le profil le plus diversifié : 65,9 % sur la Seconde Guerre mondiale, certes, mais aussi 14 % sur le Vietnam, 5,9 % sur l'Afghanistan, 4,2 % sur la Corée, 3,5 % sur l'Irak. Hollywood couvre à peu près une guerre par décennie depuis 1945, à mesure que les engagements militaires américains se renouvellent. La signature américaine n'est pas un conflit, c'est une boulimie, celle d'une superpuissance qui, plutôt que d'avoir un sujet, en produit en série.

Entre ces deux extrêmes, chaque pays décline sa propre signature. La France filme à 5,4 % la guerre d'Algérie, conflit dont personne d'autre ne s'empare significativement (0,2 % aux États-Unis, 0 % ailleurs). La Russie a fait des guerres de Tchétchénie son monopole quasi-exclusif (3,8 % sur la première guerre de Tchétchénie, contre 0 % partout ailleurs). L'Allemagne, plus surprenamment, consacre 5,7 % de son cinéma de guerre à la guerre froide, soit plus du triple de la part américaine (1,7 %). Cette anomalie statistique cesse d'en être une dès lors qu'on se souvient que l'Allemagne fut, pendant quatre décennies, le seul pays au monde à avoir été littéralement coupé en deux par la guerre froide. Le cinéma allemand qui s'empare de la guerre froide ne la regarde pas comme un événement géopolitique abstrait, à la manière dont Hollywood traite l'espionnage : il la filme depuis l'intérieur du pays, depuis la cuisine, la chambre, le bureau de l'écrivain surveillé. *La Vie des autres* (2006), qui valut à Florian Henckel von Donnersmarck l'Oscar du meilleur film étranger, *Good Bye, Lenin!* (2003), *Le Tunnel* (2001) forment un sous-genre proprement allemand, à la tonalité intime qu'aucune autre cinématographie ne pouvait produire.

Le Royaume-Uni, lui, présente le profil le plus dispersé du corpus. Sa signature n'est pas un conflit, mais un éparpillement : Malouines (1,6 %), Irlande du Nord (1,2 %), Kosovo, Malaisie, Révolution hongroise. Autant de petites taches sur la heatmap qui dessinent, en creux, la géographie d'un empire défait. Le cinéma britannique semble revisiter par fragments les marges de ce qui fut son territoire ; les confettis d'un empire continuent de produire des images, longtemps après que l'empire lui-même a cessé d'exister.

Mais une fois identifiées ces signatures, une question plus subtile se pose : chaque pays filme-t-il réellement ses propres guerres, ou aussi celles des autres ? C'est ici qu'une seconde analyse, sur la nature de la narration, révèle un trait inattendu.

<img width="1205" height="585" alt="image" src="https://github.com/user-attachments/assets/971621d6-9b35-49e2-b6ac-5a582ab8a947" />

<img width="1197" height="581" alt="image" src="https://github.com/user-attachments/assets/c80e0eee-fd93-485f-99ed-764f8252c533" />

Une fois la Seconde Guerre mondiale écartée (elle implique mécaniquement tous les pays et fausse la lecture), trois groupes apparaissent. Les États-Unis (95,9 %) et la France (93,9 %) sont des cinémas farouchement auto-centrés : ils filment leurs propres guerres et presque exclusivement les leurs. Le Royaume-Uni (75,6 % contre 24,4 %) et la Russie (66,7 % contre 33,3 %) présentent un profil mixte. Le Royaume-Uni filme largement les guerres des autres, mais avec une particularité frappante : sur dix films britanniques portant sur des conflits étrangers, six concernent la guerre du Vietnam, celle de l'Amérique, donc, à laquelle le Royaume-Uni n'a pourtant pas participé. On y lit peut-être l'écosystème anglo-américain à l'œuvre, qui fait du cinéma britannique un partenaire culturel constant du récit hollywoodien.

Le cas russe est plus singulier encore. Sur les sept films russes portant sur des conflits dans lesquels la Russie n'était pas impliquée, **tous les sept** traitent de la guerre d'Afghanistan post-2001, c'est-à-dire de la guerre américaine. La coïncidence n'en est pas une. L'Union soviétique a perdu sa propre guerre d'Afghanistan (1979-1989), et le cinéma russe contemporain, en filmant la guerre américaine sur le même théâtre, accomplit un geste qu'on serait tenté d'appeler une rétro-projection : commenter la défaite des autres pour ne pas avoir à dire la sienne, ou peut-être, plus subtilement, dire la sienne en disant celle des autres.

Restent les deux cas atypiques. L'Allemagne, avec son partage 50/50, présente le cinéma le plus ouvert sur l'extérieur du corpus, partageant son regard entre ses propres engagements post-Guerre froide (Bosnie, Kosovo, Afghanistan dans le cadre de l'OTAN) et les conflits étrangers (Vietnam, Irak, Golfe, Syrie). Et le Japon, dans une asymétrie inverse : ses trois films hors-1945 traitent tous, à 100 %, de conflits étrangers (Vietnam, Corée, Bosnie). Le constitutionnellement pacifiste Japon, quand il filme la guerre en dehors de la sienne, le fait en pur observateur, jamais en participant. On notera la fragilité statistique de cette dernière observation (trois films seulement), mais le profil global qui se dessine est cohérent.

---

## III. Quand filme-t-on la guerre ?

Reste, pour clore cette réflexion, à interroger la dimension qui structure secrètement toutes les autres : le temps. Une guerre se filme-t-elle pendant qu'elle se déroule, juste après, ou bien plusieurs décennies plus tard, le temps qu'une génération laisse à la suivante le soin de regarder ?

La réponse globale est sans appel : 74,5 % des films sortent plus de dix ans après la fin du conflit qu'ils représentent. Le cinéma de guerre est, d'abord et avant tout, un cinéma de la mémoire. Seuls 10,9 % des films sortent pendant le conflit lui-même, et 14,6 % dans la décennie qui suit. La guerre, pour devenir film, a besoin de temps, souvent beaucoup de temps. Mais cette moyenne masque des écarts considérables, qui prolongent et confirment ce que les signatures nationales avaient déjà laissé entrevoir.

<img width="1301" height="582" alt="image" src="https://github.com/user-attachments/assets/8433f52a-0eac-478b-9b8f-4bf22c330e52" />

Les États-Unis sont les plus contemporains de leurs guerres : 34 % de leurs films sortent pendant ou dans les dix ans suivant la fin du conflit, ce qui en fait le seul cinéma à filmer véritablement à chaud. Hollywood est, en quelque sorte, le chroniqueur en temps quasi réel des engagements militaires américains : *American Sniper* (2014) sort trois ans après la fin officielle de la guerre d'Irak, *Lone Survivor* (2013) ou *12 Strong* (2018) traitent de la guerre d'Afghanistan alors même que les troupes américaines y sont encore engagées. À l'autre extrême, le Japon (95,2 % en mémoire longue) et la Russie (84,1 %) cultivent un rapport à la guerre fondamentalement rétrospectif. Le Japon ne peut faire autrement, faute de conflits récents ; la Russie, plus paradoxalement, le choisit, accumulant les films sur 1945 quand ses conflits contemporains restent largement sous-traités à l'écran.

Mais c'est en raisonnant par conflit, et non plus par pays, que la distribution temporelle devient la plus révélatrice.

<img width="1197" height="732" alt="image" src="https://github.com/user-attachments/assets/aa8b8f17-189b-44aa-99e4-d34c12e158be" />

Trois catégories émergent. Les conflits dits « à chaud » se filment majoritairement pendant qu'ils ont lieu : la guerre d'Afghanistan post-2001 (83,3 %), la guerre froide (54,2 %) qui dura, il est vrai, assez longtemps pour devenir genre cinématographique en son sein même, par l'espionnage à la John Le Carré et les adaptations d'Ian Fleming, la guerre d'Irak (51,6 %). Les conflits « tièdes » se filment majoritairement dans la décennie qui suit leur fin : guerre du Golfe (80 % d'aftermath), guerre de Corée (63,3 %), guerre de Bosnie (53,8 %). Les conflits « froids », enfin, exigent plus de dix ans avant d'être filmés massivement : Seconde Guerre mondiale (87,4 % en mémoire longue), guerre d'Algérie (80 %), guerre du Vietnam (61,7 %).

Or il n'est pas anodin que les trois conflits les plus lents à devenir cinéma soient aussi les plus moralement complexes. La Seconde Guerre mondiale impliquait des questions de collaboration, de génocide, de bombardements atomiques. L'Algérie posait celle du colonialisme. Le Vietnam, celle de la défaite morale d'une superpuissance. La guerre du Golfe (1990-91) est rapidement filmable parce qu'elle est rapidement gagnée et politiquement consensuelle ; la guerre d'Algérie ne l'est pas parce qu'elle pose à la France une question qu'elle préfère, longtemps, ne pas se poser.

Cette dernière observation conduit à une question finale, peut-être la plus instructive : que filme-t-on, et que ne filme-t-on pas ?

<img width="2592" height="1968" alt="06_universality_ranking" src="https://github.com/user-attachments/assets/3a47b08a-3784-4af5-8623-dfb678ac0457" />

Sur les vingt-six conflits classifiés, cinq seulement (19 %) sont filmés par cinq ou six pays (et encore, l'« universalité » de ces cinq conflits est très relative). La guerre du Vietnam est filmée à 85 % par les Américains, la guerre d'Afghanistan à 63 %, la guerre froide à 46 %. La seule véritable universalité équilibrée concerne la Seconde Guerre mondiale, où les six pays participent dans des proportions à peu près comparables (États-Unis 39 %, autres entre 7 et 19 %). Pour le reste, ce qu'on prend pour de l'universel relève en réalité d'une hégémonie hollywoodienne avec contributions étrangères en sous-traitance.

Plus parlant encore : six conflits du corpus n'ont donné lieu qu'à **un seul film** chacun. La révolte des Mau Mau au Kenya (1952-1960), la Révolution hongroise de 1956, l'Émeute malayenne (1948-1960), la guerre civile libyenne, la guerre du Kosovo, la guerre du Kippour. Ces conflits ne sont pourtant pas mineurs : ils ont parfois mobilisé des dizaines de milliers de combattants, redessiné des frontières, déstabilisé des régions entières. Mais aucune cinématographie nationale, parmi les six étudiées, ne s'en est véritablement saisie. Plus frappant encore, le seul film sur la révolte des Mau Mau a été produit non par le Royaume-Uni (qui fut pourtant la puissance coloniale impliquée) mais par les États-Unis. Le cinéma britannique passe sous silence l'un de ses propres chapitres coloniaux les plus violents. Ce silence, statistiquement aberrant, est historiquement parlant : il s'inscrit dans une tradition de mise à distance britannique de la mémoire impériale.

Ces silences cinématographiques sont peut-être plus parlants que tout ce qui précède : ils dessinent en creux la part du monde que le cinéma ne sait pas, ou ne veut pas, regarder.

## Conclusion

Au terme de cette réflexion en trois mouvements, le film de guerre apparaît moins comme un genre mondial que comme une mosaïque de mémoires nationales, dont chacune obéit à sa propre temporalité, à ses propres obsessions, à ses propres silences. À la première question, celle de l'unité du genre, les chiffres répondent par la dispersion : il n'existe pas un mais six cinémas de guerre, profondément différents par leurs volumes et leurs rythmes. À la deuxième, celle de ce qui est représenté, ils répondent par les signatures nationales : la France et l'Algérie, l'Allemagne et la guerre froide, la Russie et la Tchétchénie, le Royaume-Uni et les marges de son empire, le Japon et la seule guerre qu'il ait perdue. À la troisième, celle du temps, ils répondent par l'asymétrie temporelle : certaines guerres se filment à chaud, d'autres demandent une génération de silence avant de pouvoir devenir image.

Ce que les chiffres laissent voir, *in fine*, c'est moins ce qui s'est passé que ce que chaque pays a décidé d'en retenir (ou de ne pas en retenir) sur ses écrans. Le cinéma de guerre est en cela une politique de la mémoire avant d'être une esthétique. À l'historien revient la tâche d'établir les faits ; au cinéma, celle, plus ambiguë, de décider lesquels, parmi ces faits, méritent de continuer à être regardés.

---

## Méthodologie

Le corpus de 2 343 films analysés a été constitué à partir de l'API de The Movie Database (TMDB), interrogée pour récupérer l'ensemble des films classés dans le genre « guerre » depuis 1939, dans les six pays cibles. La période 1945-2025 a ensuite été retenue pour l'analyse, à une exception près : la Seconde Guerre mondiale (1939-1945) a été conservée, faute de quoi le conflit fondateur du cinéma de guerre du XXᵉ siècle aurait été artificiellement exclu.

Un détail méthodologique mérite d'être signalé. Une première version du corpus présentait une anomalie frappante : zéro film russe classifié avant 1990. Après enquête, il s'est avéré que TMDB indexe les films de l'ère soviétique sous le code pays « SU » (Union soviétique), distinct du code « RU » (Russie). La collecte initiale, en n'interrogeant que « RU », avait donc raté près d'un demi-siècle de l'une des cinématographies de guerre les plus riches au monde. Une seconde version du pipeline a réintégré « SU » et fusionné les deux ensembles, récupérant 136 films classifiés supplémentaires et rendant possible la comparaison avec l'âge d'or du cinéma soviétique. La leçon vaut d'être retenue : lorsqu'un jeu de données présente un trou statistique aussi net, le premier suspect doit être le pipeline lui-même plutôt que le phénomène observé.

Après collecte, les données ont été nettoyées par déduplication des coproductions et par un filtrage adaptatif par pays, destiné à compenser autant que possible le biais anglo-centré de la base TMDB, biais qui aurait, sans cette correction, sur-filtré les cinématographies non anglophones par effet d'audience.

L'étape la plus délicate fut la classification des films par conflit. Deux couches successives ont été mises en œuvre. La première a interrogé les synopsis des films au moyen d'un dictionnaire de mots-clés construit conflit par conflit, avec une attention particulière aux bornes de mots, pour éviter par exemple qu'un mot-clé comme « ira » ne se déclenche à l'intérieur d'« iraqi ». La seconde couche, pour les films non classifiés par cette première passe, est allée interroger l'API des mots-clés communautaires de TMDB, qui propose pour chaque film une liste de tags thématiques curés par les utilisateurs de la plateforme. Tous les films présentant des incohérences temporelles évidentes (films classifiés à une guerre antérieure à leur sortie de plusieurs décennies) ont été reclassifiés manuellement. Au terme du processus, 1 445 films sur 2 185 « in-scope » ont été rattachés à un conflit, soit un taux d'efficacité de 66,1 %. Un audit manuel stratifié sur trente films a permis d'estimer la précision de la classification à 80-85 %.


## Limites de l'analyse

Trois limites doivent être gardées à l'esprit pour lire ce travail à sa juste mesure. Le corpus repose sur la base de données TMDB, dont la couverture structurellement anglo-centrée sous-représente les cinématographies non anglophones (particulièrement celles de l'Asie et de l'ancien bloc soviétique avant les années 1990). Le filtrage adaptatif évoqué plus haut compense partiellement ce biais, sans le corriger entièrement. La classification automatique des films, ensuite, atteint une précision estimée à 80-85 %, ce qui signifie qu'environ un film sur six pourrait être mal rattaché à son conflit ; cette marge d'erreur ne remet pas en cause les grandes tendances mises en évidence, mais invite à les lire pour ce qu'elles sont : des ordres de grandeur, et non des chiffres définitifs.
Enfin, une part de la mémoire cinématographique mondiale (celle qui n'a pas été indexée par TMDB, celle qui n'a pas été distribuée à l'international) échappe nécessairement à cette analyse.

