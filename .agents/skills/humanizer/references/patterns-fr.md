# Patterns d'écriture IA (français)

Catalogue **natif** — pas une traduction de `patterns.md`. Les LLM
surutilisent des formes statistiques propres au français. Corriger seulement
les patterns présents.

**Règle critique :** nominalisation, passif et registre soutenu ne sont **pas**
des marqueurs IA en français (prose française classique). Ne les flaguer que
combinés à d'autres patterns, ou en densité anormale.

Sources : `sources-fr.md`. Gravités : P0 = artefact immédiat, P1 = forte odeur
IA, P2 = juger selon le contexte.

## Vocabulaire (3 niveaux)

### Tier 1 — Flaguer dès la première occurrence (P1)

| Mot / expression IA | Préférer | Note |
|---|---|---|
| crucial | important / décisif / (chiffre) | top tic FR |
| essentiel | nécessaire / (reformuler) | « il est essentiel » = tic fréquent |
| fondamental | de base / central / (reformuler) | surutilisé hors sciences |
| captivant / fascinant / troublant | (décrire concrètement) | adjectifs d'inflation |
| harmonieux / harmonie | (décrire) | générique IA |
| réinventé | transformé / modifié / (verbe précis) | très surreprésenté vs prose humaine |
| verdoyant | (garder seulement en description nature) | surreprésenté hors contexte |
| dynamique | (supprimer ou préciser) | affirmation vide |
| innovant / innovation | (dire ce qui est nouveau) | claim sans preuve |
| au cœur de | dans / (concret) | métaphore générique |
| naviguer (métaphorique) | gérer / traverser / (verbe concret) | calque de *navigate* |

### Tier 2 — Flaguer si ≥ 2 occurrences dans le même texte (P2)

notamment ; particulièrement ; essentiellement ; dorénavant ; en outre ;
cependant (en tête de phrase à répétition) ; permettre de ; s'inscrire dans ;
mettre en lumière ; s'articuler autour de ; contribuer à ; constituer ;
se traduire par ; mettre en œuvre (hors juridique) ; une multitude de ;
un large éventail de ; efficacement ; transparent / transparence (buzz)

**Préférer :** verbe direct, chiffre, ou supprimer l'adverbe vide.

### Tier 3 — Flaguer à haute densité (≥ 2× la même formule, ou ≥ 3 formules
distinctes)

- « Dans le paysage actuel de… »
- « À l'ère de… » / « À l'heure de… »
- « Dans un monde qui évolue à un rythme effréné… »
- « Il est important / crucial de noter que… »
- « En conclusion » / « Pour conclure » / « En résumé » / « En somme »
- « besoin urgent » ; « nous devons » (appel rhétorique vide)
- « non seulement X, mais aussi Y » (répété) ; « à la fois X et Y »
- « enjeux et opportunités » ; « défis et perspectives »
- « transformation digitale / numérique » (formule managériale vide)
- « bonnes pratiques » (sans dire lesquelles)

## Contenu

### 1. Inflation de sens (P1)

**Avant :** « un tournant décisif pour l'ensemble du secteur »
**Après :** « l'entreprise est passée de 200 à 400 clients payants ce trimestre »

### 2. Crédibilité par nommage vague (P1)

**Avant :** « selon plusieurs experts et de nombreuses études récentes »
**Après :** « selon l'étude INSEE 2024 (n=2 400) » — ou supprimer si pas de source

### 3. Participes / -ant vides (P1)

**Mots :** illustrant, reflétant, soulignant, mettant en lumière, favorisant
**Après :** faits concrets ou coupe

### 4. Vocabulaire publicitaire / brochure (P1)

**Avant :** « au cœur du dynamique écosystème innovant de la French Tech »
**Après :** « basé à Paris 11e »

### 5. Sources vagues (P1)

**Avant :** « les experts s'accordent à dire… »
**Après :** source nommée, ou flaguer le trou factuel (ne pas inventer)

### 6. Défis formulaïques + pivot positif (P1)

**Avant :** « malgré les défis, l'entreprise continue de prospérer »
**Après :** nommer le défi et la réaction réelle

### 7. Inflation de nouveauté (P2)

Couper « un concept que je n'avais jamais rencontré » s'il n'apporte rien ;
garder une observation personnelle concrète.

## Langue et grammaire

### 8. Vocabulaire Tier 1/2/3

Voir tableaux ci-dessus. Un mot Tier 1 isolé peut être coïncidence hors cluster ;
un cluster ou une formule Tier 3 justifie l'édition.

### 9. Évitement de la copule (P1)

**Remplacer :** s'inscrit dans, se traduit par, s'articule autour de, constituer,
mettre en lumière → **est / a / fait / montre / porte sur**

### 10. Chaînes de synonymes (P1)

Répéter le mot juste (« développeurs ») au lieu de faire tourner
ingénieurs / codeurs / concepteurs dans le même passage.

### 11. Phrases gabarit (P2)

« une [adj] avancée vers une [adj] infrastructure » → résultat concret

### 12. Transitions en tête de phrase (P1)

Par ailleurs, De plus, En outre, Ainsi, Dès lors, Par conséquent, Enfin,
Cependant (en série) → et / aussi / restructurer

### 13. Fausse amplitude (P2)

« de la recherche fondamentale à la mise sur le marché » → lister les sujets réels

### 14. Accumulation de hedges (P1)

« pourrait éventuellement peut-être » → une seule modalité

### 15. Conditionnel-hedge / adverbes d'ouverture (P2)

« il serait intéressant de noter » ; « Fondamentalement… » ; « Globalement… »
→ affirmation directe ou coupe

### 16. Faux contraste / fausse concession (P1)

« Si X a des limites, il reste remarquable » → trade-off réel

## Structure et mise en forme

### 17. Formatage excessif (P1)

Tirets cadratins en série, gras mécanique, titres emoji, listes lourdes

### 18. Uniformité structurelle (P1)

Phrases toutes 15–25 mots, paragraphes clones, grammaire trop lisse

### 19. Puces nominales nues (P1)

`• Performance stable • Infrastructure fiable` → prose ou phrases avec verbe + chiffre

### 20. Title Case dans les titres (P2)

« Les Enjeux De La Transformation » → « Les enjeux de la transformation »

### 21. Inflation de listes / trilogie forcée (P2)

« Voici 7 raisons… » ; toujours exactement 3 conseils → longueur justifiée par le fond

### 22. Ouverture rhétorique par question (P1)

« Et si la solution existait déjà ? » → commencer par la thèse

## Communication

### 23. Ouvertures chatbot (P0)

Bien sûr !, Avec plaisir !, Absolument !, Certainement !, Je serais ravi(e) de…

### 24. Constructions « plongée » (P1)

Plongeons dans…, Explorons ensemble…, Regardons de plus près…, Parcourons…

### 25. Disclaimers de lacune (P1)

À ma connaissance…, Selon les informations dont je dispose…,
À la date de mes connaissances…

### 26. Clôtures génériques (P0)

L'avenir s'annonce prometteur. ; Seul le temps nous le dira. ;
Une nouvelle ère s'ouvre. ; Des temps passionnants nous attendent.

### 27. Ouvertures de résumé IA (P0)

En conclusion, il convient de souligner… ; Il ressort de cette analyse que… ;
Pour résumer… ; Il y a lieu de noter que…

### 28. Marqueurs d'emphase IA (P1)

Il est important / à noter que… ; Notons que… ; Il convient de souligner que… ;
Il est intéressant de constater que… ; Il faut souligner que…

### 29. Ton sycophante (P0)

Excellente question ! ; Vous avez tout à fait raison ! ;
Merci pour cette question stimulante.

### 30. Boucles de confirmation / artefacts de raisonnement (P1)

Vous me demandez… ; Pour répondre à votre question… ;
Regardons cela étape par étape ; Laissez-moi décomposer cela

## Spécifique français (management / LinkedIn)

### 31. Langue de bois managériale (P1)

s'inscrit dans une démarche de… ; mise en œuvre d'une approche globale ;
dans une logique de… ; démarche qualité ; leviers de performance ;
atout différenciateur ; résilience impressionnante

→ faits, chiffres, actions, dates

### 32. Formules impersonnelles de distanciation (P1)

Il s'avère que… ; Il apparaît que… ; Il semblerait que… ;
Force est de constater que… → X montre que… / les données indiquent…

### 33. Substantifs managériaux en liste (P1)

`• Transformation numérique • Enjeux stratégiques • Vision globale`
→ phrases avec verbe et donnée (style Grandes Écoles / direction)

### 34. Hashtag stuffing (P0)

≥ 4 hashtags génériques (#Innovation #Leadership #Transformation…) → 0–2 ciblés

### 35. Narratif prospectif en clôture (P1)

« pourrait devenir l'un des enjeux majeurs de la prochaine décennie »
→ prédiction falsifiable ou coupe

## Tells de « humanisation » ratée (équivalents FR des EN 29–31)

### 36. Théâtre d'intégrité / esprit trop malin (P1)

Listes de refus pour faire genre (« Pas de X, pas de Y ») ; punchlines de vertu
dans une blurb README ; anti-exemples miniatures. Dire ce que l'outil fait,
pas prouver qu'on est honnête.

### 37. Mots savants / jargon de boutique inutiles (P1)

prose, bullets, levier, paradigme, narratif, artefact, surface (verbe), unpack,
cadence, registre — quand le mot ordinaire suffit (*texte*, *lignes*, *outil*).

### 38. Faux décontracté (P1)

Forcer *carrément*, *grave*, *vibes*, *low-key*, *ça hit différent* dans une note
interne, un README ou un communiqué. Préférer le mot juste et ennuyeux sauf si
c'est déjà la voix du texte (blog perso, dialogue).

## Préférer une syntaxe humaine

- Prédicats simples : est, a, fait
- Verbes concrets : écrit, lance, manque, signe (pas « met en œuvre une démarche »)
- Chiffres, noms, dates fournis par la source — ne jamais inventer pour « humaniser »
- Laisser une irrégularité naturelle ; ne pas découper en fragments staccato
- Ne pas coller du « je » / de l'anecdote absents de la source

## Hors périmètre sauf demande

Wikicode FR, artefacts AfC, DOI hallucinés — seulement si l'utilisateur édite
Wikipédia.
