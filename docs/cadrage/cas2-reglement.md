# Fiche de cadrage : Questions sur le règlement intérieur

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Répondre aux questions des étudiants sur le règlement intérieur en indiquant l'article sur lequel la réponse repose.

## Utilisateur final (obligatoire)

Les étudiants, qui obtiennent une réponse à toute heure, et le secrétariat, qui n'a plus à répéter les mêmes réponses par courriel.

## Approche retenue (obligatoire)

- [ ] Règles métier
- [ ] Machine learning
- [x] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire)

(b) La réponse doit être vérifiable : on affiche l'article cité, ce qu'un modèle génératif seul ne garantit pas. (a) Nous n'avons aucune base de questions étiquetées, donc l'apprentissage supervisé n'est pas possible. (c) Il y a peu de questions par jour, donc le coût d'un appel à un modèle de langage reste acceptable.

## Données nécessaires et leur origine (obligatoire)

Le règlement intérieur en PDF et les notes de service de la direction, documents publics de l'école, découpés en passages et indexés. L'index est reconstruit à chaque mise à jour du règlement.

## Métrique de succès et seuil d'acceptation (obligatoire)

Part de réponses correctes avec la bonne citation, sur 20 questions fournies par le secrétariat ; acceptation à partir de 0,90, et aucune réponse ne doit citer un article inexistant.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une réponse fausse peut tromper l'étudiant sur ses droits ou ses obligations ; l'extrait cité est toujours affiché pour qu'il vérifie, et le secrétariat reste l'interlocuteur en cas de doute.

## Risques éthiques ou de confidentialité (obligatoire)

Une question peut contenir un nom ou un numéro d'étudiant : aucune question n'est conservée après la réponse, et seuls les documents officiels entrent dans l'index.

## Approche écartée et pourquoi (facultatif)

Modèle génératif seul : il donnerait des réponses plausibles mais pourrait inventer des numéros d'articles.
