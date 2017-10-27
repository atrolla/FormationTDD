---?image=resources/img/arolla-software-craftsmanship.jpg

# Formation TDD

Note: 
Faire un tour de table, se présenter, demander pourquoi les gens sont là.

---

## Pourquoi le TDD ?

Note: 
Pourquoi on teste ? TDD selon vous ? (permet de voir si public sensibilisé)
-> ce n'est pas au client de tester
-> preuve que cela marche dans des conditions (de tests)
-> confiance - image de soi/société

+++

<img src="resources/img/tester-c-est-douter.jpg" />

---

#### Comment on teste ?

- Manuel vers Automatique
- QA pour la conception, Dev pour la réalisation
- Tests à postériori vers Tests avant implémentation

---

#### TDD : Les promesses (le ROI)

- Documentation vivante Agile

.. Dans le même repo que le code de production : synchronisée
.. Exécutable : sa validation est à jour
.. L’intégration continue, valide cette spécification systématiquement

- Spécification technique par l’exemple

.. Écrite avant le code pour implémenter et maintenir la fonctionnalité
.. Vérifie le comportement attendu, pas les détails d’implémentation

- Outil de design ?

.. Les mocks/stubs servent à définir l’usage des composants de votre architecture
.. Outil de VOTRE design que vous faites « émerger »


Note:
Documentation c'est les tests, ce sont des exemples
Spécifications par l'exemple, ATDD, on prouve (à soi et au métier s'il faut)
BBD peut être vu comme une spécification fonctionnelle vivante et agile
Outil, et non la silver bullet. Donc ça aide, mais ne fait pas la travail à votre place.