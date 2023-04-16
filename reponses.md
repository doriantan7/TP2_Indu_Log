# TP2 indu Tan

## Ex1.b

### Quelles étapes (steps) sont réalisées par cette action ?

- Setup de python 3.10
- Installation des dependances
- Lintage
- Tests

### Une étape est définie au minimum par 2 éléments, lesquels sont-ils et à quoi servent-ils ?

Elements <i>run</i> et <i>name</i>, le premier est la commande à lancer pour le step et le second est le nom de l'étape qui sera affiché à la suite de l'execution.

### La première étape contient le mot-clé ‘with’, à quoi sert-il ?

C'est une dépendence pour une version de logiciel précis.

## Ex 2.d

### Sur l’onglet Summary d’une analyse de code, SonarCloud fournit 4 indicateurs. Quels sont-ils et quelles sont leurs utilités ?

1. Bugs: Les nombre de bugs que sonar cloud a trouvé
2. Code Smells: Les bouts de code compliqués et durs a maintenir
3. Vulnerabilities: Code pouvant être exploité par des hackers
4. Security hotspots: Code sensible necessitant une verification manuelle de la sécurité

## Ex 2.a

## Sur l’onglet Summary d’une analyse de code, SonarCloud fournit 4 indicateurs. Quels sont-ils et quelles sont leurs utilités ?

## À quoi sert l’indicateur Quality Gate ?

Cela sert à savoir si un code est prêt à être mit en production.

## Ex 2.b

### Quelle est la différence entre les sections New code et Overall Code dans l’onglet Summary ?

- <i>new code</i> analyse uniquement le dernier push de code
- <i>Overall Code</i> analyse tout le code

### Y a-t-il des Code Smells ? Si oui, combien et pour quelle(s) raisons(s)?

- des paramètres non utilisé dans une fonction
- une fonction en double, à modifier ou supprimer

### Y a-t-il des Security Hotspots ? Si oui, combien et pour quelle(s) raison(s) ?

Oui, 1, utilisation de l'utilisateur par default `root` pour python dans l'action.

## Ex3.a

### 1. Que fait le job pytest ?

Il s'occupe de créer un <i>env virtuel</i>, puis lance les tests python.

### 2. Que fait le job image-creation ?

D'après le dockerfile existant, il crée une image.

### 3. Que fait le job package-creation ?

Crée le package.

### 4. Les jobs s’exécutent-ils dans le même ordre que défini dans le fichier ? Sinon, pourquoi?

Non, les jobs se lancent tous simultanement par défaut, cependant avec la commande <i>after:</i> il est possible d'indiquer l'odre nous-même.

Non, les jobs se lancent simultanement sauf on spécifie l'ordre avec la commande `after:`.

### 5. Le stage 2 génère une image Docker. Où est-elle stockée et comment pouvez-vous la retrouver ?

Sur le repo qui l'a créé.

### 6. Le stage 3 génère un wheel Python. Où est-il stocké et comment pouvez-vous le retrouver ?

Dans les artefacts du repo.
