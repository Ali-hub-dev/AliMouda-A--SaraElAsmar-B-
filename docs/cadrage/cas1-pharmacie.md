# Fiche de cadrage : Ordonnances incomplètes en pharmacie

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Signaler au pharmacien les ordonnances auxquelles il manque une mention obligatoire (date, posologie, signature...).

## Utilisateur final (obligatoire)

Le pharmacien au comptoir, qui reçoit une alerte à la saisie au lieu de tout relire.

## Approche retenue (obligatoire)

- [x] Règles métier
- [ ] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire)

(a) Aucune ordonnance étiquetée n'est disponible, et la liste des champs obligatoires est déjà écrite dans la réglementation. (b) Le pharmacien doit pouvoir dire au patient quel champ manque : une règle se lit, un modèle non. (d) Une erreur touche la santé du patient, donc chaque décision doit être explicable.

## Données nécessaires et leur origine (obligatoire)

Liste des mentions obligatoires issue du texte réglementaire ; pour les tests, ordonnances fictives écrites par l'équipe, aucune donnée réelle.

## Métrique de succès et seuil d'acceptation (obligatoire)

Taux de champs manquants détectés sur 40 ordonnances fictives (20 incomplètes) ; acceptation à 100 %, avec moins de 10 % de fausses alertes.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une alerte manquée peut mener à délivrer sur une ordonnance non conforme ; l'outil ne bloque rien, le pharmacien valide chaque ordonnance avant la remise.

## Risques éthiques ou de confidentialité (obligatoire)

Données de santé (loi 09-08, RGPD) : ordonnances fictives uniquement, aucun nom de patient, rien d'envoyé à un service externe.

## Approche écartée et pourquoi (facultatif)

Machine learning : il faudrait d'abord constituer des milliers d'ordonnances annotées, pour un gain nul sur une règle déjà connue.
