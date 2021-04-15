# CI/CD

## Qu'est-ce que la CI/CD ?

"L'approche CI/CD permet d'augmenter la fréquence de distribution des applications grâce à l'introduction de l'automatisation au niveau des étapes de développement des applications. Les principaux concepts liés à l'approche CI/CD sont l'intégration continue, la distribution continue et le déploiement continu."

"L'approche CI/CD représente une solution aux problèmes posés par l'intégration de nouveaux segments de code pour les équipes de développement et d'exploitation (ce qu'on appelle en anglais « integration hell », ou l'enfer de l'intégration)."


![CICD](./Images/ci-cd-flow-desktop_1.png)


"Il suffit de retenir que l'approche CI/CD se rapporte à un processus, souvent représenté sous forme de pipeline, qui consiste à introduire un haut degré d'automatisation et de surveillance continues dans le processus de développement des applications."

(source: [https://www.redhat.com/fr/topics/devops/what-is-ci-cd](https://www.redhat.com/fr/topics/devops/what-is-ci-cd)  )

Concrétement, c'est un ensemble de processus qui favorise grandement la vie des développeurs (et donc la qualité du code et la vitesse de production).


---

## Exemple de CI/CD

Trois exemples pour mieux comprendre:
+   Chez magellium (PME en imagerie), lorsque j'y travaillais, la CI/CD était utilisé pour construire et déployer des images docker dans un registry docker. Si on modifiait le dockerFIle sur le git, ça déployait une nouvelle image. Ceci permettait à tous les développeurs de travailler strictement sur le même environnement de travail.

+   Lorsque j'ai créer le site [linto demo](https://demo-linto.netlify.app/), j'ai utilisé [Netlify](https://www.netlify.com/). C'est un outil de CI/CD. En conséquence, chaque fois que je fais une modification sur le git du projet, netlify va récupérer les sources du site, les déployer, et les servir en ligne. Concrétement, j'ai juste à modifier mes sources, et le site est déployé automatiquement en cas de changement. 

+    EsLint est un Linter (un logiciel faisant de l'analyse statique de code pour être certain qu'il n'y ait pas d'erreurs). Il est possible de rajouter EsLint à une pipeline CI/CD pour vérifier qu'il n'y a aucune erreurs ou sources possibles d'erreurs lorsqu'on pousse du code sur gitlab, (cf [eslint CI/CD]( https://dev.to/karltaylor/getting-started-with-gitlab-cicd-eslint-1m80))



---

## Intêret potentiel de la CI/CD sur CAPT-L2


Le déploiement d'une CI/CD est toujours relativement couteux en temps. C'est pour ça que des rôles spécialisées apparaissent (DevOps) dans les entreprises. C'est aussi pour ça que le gitlab de l'irit de dispense pas, à l'heure où j'écris ces lignes, de CI/CD.

Idéalement, dans le meilleur des mondes, ce serait bien d'avoir deux choses:

+   La compilation des images docker servies (par les serveur) en CI/CD

    Il suffirait alors de juste de faire des changements sur une branche, et les images docker comprennant les modifications seraient automatiquement servies (et déployées sur internet).

+   Avoir un environnement de ***staging***

    Ce n'est pas une contrainte forte non plus, juste une suggestion.
    Un environnement de stagging est un environnement de test entre le ***dev*** et la ***prod***.

    Un ***dev*** est un environnement local. C'est ce sur quoi développe les gens.

    La ***prod*** est l'environnement de production. C'est l'environnement final auquel peuvent accèder les personnes extérieurs. Dans le cas de CAPT-L2, c'est ce site: [51.255.78.130](51.255.78.130)

    Un ***staging*** est un environnement intermédiaire, entre prod et test. Il permets de déployer des modifications sans impacter la production.
    Dans un cas concret, si une modification effectuer sur le code provoque des crash, si il y a un stagging, on pourra le voir à ce moment là. Sans stagging, le bug risque d'être vu que sur la prod, ce qui fait que les utilisateurs finaux ne pourrons plus accéder au site (et donc un coût économique pour l'entreprise).


---

+ ## [Retour sommaire](../README.md)