# Entités Nommées

Plugin pour SPIP qui permet de découvrir des entités nommées dans un corpus. On essaie notamment de trouver les personnalités évoquées par période de temps.

On peut trouver des noms de personnalités dans un texte en recherchant le masque suivant : Xxx Xxx xx xx Xxx
Ce masque est cependant perturbé par les mots courants de la langue francaise en début de phrases, et les pays, les villes et les institutions qui font également usage des capitales.

On essaie donc d'isoler ces entités nommées connues avant de rechercher le masque sur le reliquat du texte.

On s'appuie pour cela sur des listes issues du site typo.mondediplo.net, ou monde-diplomatique.fr
- Lieux
-- Pays
-- Capitales
-- Villes

- Intitutions
-- Entreprises
-- ONG
-- Institutions publiques
-- Partis politiques


Enfin on cherche en Regexp le masque Xxx Xxx xx xx Xxx sur le reliquat du texte en ignorant les mots de la langue française les plus fréquents constatés

On obtient :
-> Des Personnalités
-> D'autres entités pour gonfler les listes prédéfinies.


Installer un spip avec une base de donnée d'articles et le plugin itérateurs, puis appeler /?page=importer_entites et se rendre sur /?page=entites_nommees.