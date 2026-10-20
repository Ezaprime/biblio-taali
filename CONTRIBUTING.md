# Contribuer à Biblio

## Avant de coder
- Vérifiez qu'une issue existe pour ce que vous voulez faire. Sinon, ouvrez-en une avec le bon modèle : Signaler un bug, Proposer une évolution ou Poser une question.
- Assignez-vous l'issue pour que les autres sachent que vous êtes dessus.
- Une issue = un seul sujet. Si le sujet grossit, découpez-le en plusieurs issues.

## Branches
- On ne pousse jamais directement sur `main` : la branche est protégée, GitHub refuse.
- Une branche par issue, créée depuis `main` à jour, nommée `type/<numéro>-sujet-court` (règle de l'ADR 0004) : `fix/7-double-pret`, `docs/4-contributing`, `feat/12-export-csv`.
- Une branche est supprimée dès que sa PR est mergée.

## Commits
- Format : `type: message` à l'infinitif, en minuscules, sans point final.
- Types : `feat` (fonctionnalité), `fix` (correction), `docs` (documentation), `test` (tests), `refactor` (réorganisation sans changement de comportement).
- Exemple : `fix: refuse un livre deja emprunte`. Un commit = un changement cohérent.

## Pull requests
- Remplissez le modèle de PR : contexte, changements, impact, comment tester, checklist.
- La description contient `Closes #n` : l'issue se ferme toute seule au merge.
- Les tests (`tests`) doivent être verts : une PR au test rouge ne peut pas être mergée.

## Review
- Chaque PR est relue par au moins un autre membre, désigné dans `.github/CODEOWNERS`. L'auteur ne peut pas approuver sa propre PR.
- Le relecteur répond sous 24 h ouvrées.
- On refuse (Request changes) si : les tests sont rouges, la PR mélange plusieurs sujets, il manque `Closes #n`, ou le code ne fait pas ce que dit l'issue.
- L'auteur merge lui-même après l'approbation, puis supprime la branche.

## Definition of Done
Une tâche est finie quand :
- le code fait ce que demande l'issue et les critères d'acceptation sont cochés ;
- les tests passent (`python -m unittest`) ;
- la documentation concernée (README, docs/) est à jour ;
- la PR est approuvée, mergée dans `main` et la branche supprimée ;
- l'issue est fermée.

## Signaler un blocage
- Bloqué depuis plus d'une demi-journée ? Ouvrez une issue avec le modèle « Signaler un blocage ».
- Remplissez les cinq champs : tâche, erreur exacte (copiée, pas résumée), ce que vous avez essayé, ce dont vous avez besoin (en mentionnant une personne), échéance (une date).
- La personne mentionnée répond avec une action concrète : qui fait quoi, et quand.
