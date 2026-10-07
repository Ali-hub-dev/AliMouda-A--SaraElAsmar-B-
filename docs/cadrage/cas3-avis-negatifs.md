# Fiche de cadrage : Priorisation des avis négatifs

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Repérer automatiquement les avis clients négatifs d'un site e-commerce pour que l'équipe les traite en premier.

## Utilisateur final (obligatoire)

Les agents du service client, qui ouvrent chaque matin une liste où les clients mécontents sont déjà en haut.

## Approche retenue (obligatoire)

- [ ] Règles métier
- [x] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire)

(a) Chaque avis est accompagné d'une note en étoiles, ce qui donne des milliers d'exemples étiquetés sans effort. (c) Les avis arrivent en grand nombre chaque jour : un classifieur coûte presque rien par avis, alors qu'un modèle de langage serait facturé à chaque appel. (d) Un avis mal classé est lu un peu plus tard, sans conséquence grave.

## Données nécessaires et leur origine (obligatoire)

Les avis du site avec leur note, exportés et anonymisés (suppression des noms, adresses et numéros de commande), séparés en jeux d'entraînement, de validation et de test avant toute modélisation.

## Métrique de succès et seuil d'acceptation (obligatoire)

Rappel sur la classe « négatif » sur un jeu de test mis de côté ; acceptation à partir de 0,88. On privilégie le rappel, car oublier un client mécontent coûte plus cher que relire un avis positif.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Un avis négatif classé positif attend quelques heures de plus. L'agent peut changer la classe d'un avis en un clic, et ces corrections servent à réentraîner le modèle.

## Risques éthiques ou de confidentialité (obligatoire)

Un avis peut contenir un nom, une adresse ou un numéro de commande : anonymisation avant tout stockage. Il faut aussi vérifier que les avis très courts ne sont pas systématiquement mal classés.

## Approche écartée et pourquoi (facultatif)

Règles par mots-clés : elles ne comprennent pas la négation (« pas mauvais ») ni l'ironie, donc trop d'erreurs.
