# Journal SEO / GEO — Trucs à faire

Tenu par l'agent SEO/GEO quotidien. Une entrée par passage : ce qui a changé, pourquoi, quand revérifier.
Idées en attente en bas de fichier.

## 22/11/2026

État constaté : robots.txt autorise tous les robots (dont ceux des IA), 2 plans du site déclarés, llms.txt présent,
accueil avec title/description/canonical/Open Graph et JSON-LD WebSite + Organization, pages villes avec Event + BreadcrumbList.
Recherche web « trucsafaire.fr » : le site n'apparaît pas encore dans les résultats.

Changements :
1. Sommaire « Que faire près de chez vous » (scripts/pages_villes.py) : paragraphe d'introduction factuel (nombre de sorties
   et de départements, comment naviguer) et FAQ courte et vraie (sources, mise à jour, gratuité, fiabilité), avec JSON-LD FAQPage ;
   la CollectionPage est reliée au WebSite et à l'éditeur. Pourquoi : donner aux moteurs et aux IA une réponse claire en tête de page.
2. Liens internes « Que faire ? » (fil d'Ariane et pied des pages villes) vers l'adresse canonique que-faire/ au lieu de
   que-faire/index.html. Pourquoi : éviter deux adresses pour la même page.
3. llms.txt (scripts/pages.py) : lien de l'agenda vers l'adresse canonique, format des adresses des pages département et commune,
   et section « Comment citer ». Pourquoi : aider les IA à citer la bonne page.

À revérifier le 29/11/2026 : FAQ visible sur https://trucsafaire.fr/que-faire/ ; indexation (recherche web) ; aucun blocage de robots d'IA.

## 27/11/2026

Pas d'accès au dépôt pour la tâche planifiée : changements poussés depuis le Mac de Clément, à sa demande.
Contrôles passés : construire_app --verifier, verifier.py, tests du worker.

Changements :
1. Pages fixes (scripts/pages.py : mentions légales, CGU, offres, API, plan du site…) : ajout de canonical et des balises Open Graph
   (titre, description, adresse, image, site). Textes des pages inchangés. Pourquoi : ces pages n'avaient ni canonical ni aperçu de partage.
2. Pages villes (scripts/pages_villes.py) : og:site_name et twitter:card, comme l'accueil. Pourquoi : idée en attente du 22/11.
3. Accueil (scripts/construire_app.py) : og:title « Trucs à faire · Les sorties près de chez vous », aligné sur le title. Pourquoi : idée en attente du 22/11.

À revérifier le 29/11/2026 : balises présentes sur https://trucsafaire.fr/cgu.html et https://trucsafaire.fr/que-faire/moulins-03/.

## Idées en attente

- Lien « Trucs par ville » de l'accueil (src/app.html) et menu des pages fixes (scripts/pages.py, NAV) pointent encore vers
  que-faire/index.html : à passer en que-faire/ après avoir vérifié que l'appli mobile (Capacitor) n'en dépend pas.
- Accueil : très peu de texte lisible sans JavaScript (le sous-titre est rempli par script) ; réfléchir à un court texte statique sans toucher au design.
