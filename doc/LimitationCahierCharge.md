# Limitation d'évolution

---

## **Dépréciations des librairies / python**

(cf problèmes rencontrées)

La dépréciation des librairies / de la version de python utilisée engendre deux conséquences :

+  Des problèmes de sécurités

    Des failles vont sûrement être découvertes dans les librairies / la version de python considéré(s). Là où ces failles seraient corrigées sur des version non-dépréciées, les librairies dépréciées ne seront officiellement pas mise à jour. En conséquence, nous aurons des problèmes à long terme.

+  Des librairies qui disparaissent de dépots officielles

    Nous utilisons des dépots ""connexes""" pour certaines libraiies car elles ne sont plus présents sur des dépots officielles.
    Dans le cadre de certaine librairies (librairies archean), il faut les re-packager pour s'en servir après (vu qu'elle n'est disponible sur aucun dépots)


---

## **Django**

Django n'est pas encore une technologie dépassée. C'est une technologie qui est encore assez utilisée.

Le point fort de Django est son accesibilitée. C'est du python, c'est une framework très acessible pour les personnes qui se réorientent dans le web (notamment issue de formation de data learning). Cependant, le web moderne s'oriente sur des technologies plus récentes, type nodejs (par exemple, react en front, avec une back en nextjs). 

Il n'est peut⁻être judicieux de baser une future plateforme web commerciale sur une technologie qui tends à devenir assez peu utilisée.

Pour aller plus loin: [https://hackr.io/blog/what-is-django-advantages-and-disadvantages-of-using-django](https://hackr.io/blog/what-is-django-advantages-and-disadvantages-of-using-django)

🔴 Tout dépend de votre vision à long terme de la plateforme. Cependant, nous nous permettons de ré-itérer sur le fait que Django n'est peut-être pas le meilleure framework pour constituer une plateforme à long terme (alors que ce framework est en "pré-maison de retraite") 🔴


---

## **Problème de scalabilité**

Sur le papier, la scalabilité (proportion à mettre un site sur lequel des milliers d'utilisateur) est aisée. Cependant, il faut des moyens associées avec. 

Actuellement le serveur est sur une machine chez Archean. Il faudrait potentiellement un serveur bien plus puissant herbergée autre part si vous voulez faire une version commerciale.

De plus, rappellons qu'une bonne pratique serait d'avoir une version de stagging en marge de la version de production.



---

+ ## [Retour sommaire](../README.md)