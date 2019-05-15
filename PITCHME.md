---?image=resources/img/arolla-software-craftsmanship.jpg

# Formation TDD

Note: 
Faire un tour de table, se présenter, demander pourquoi les gens sont là.

---

## TDD by the book

Note:
On rentre dans le vif du sujet direct, mais doucement.

+++

#### 3 lois du TDD

1. Vous ne devez pas écrire du code de production avant d’avoir écrit un test en échec.
2. Vous ne devez pas écrire plus de test unitaire que le minimum pour qu’il échoue et ne pas compiler est un échec.
3. Vous ne devez pas écrire plus de code de production que le minimum pour faire passer le test unitaire actuellement en échec.

+++

<img src="resources/img/3-rules-tdd.jpg" style="height:600px;" /> 

+++

#### Boucle Red - Green - Refactor 

<img src="resources/img/red-green-refactor.jpg" style="height:560px;" /> 

---

#### Anatomie d'un test
```java
@Test
public void should_be_able_to_send_an_email() throws Exception {
    //
    // GIVEN / Arrange
    //
    Session session = Session.getInstance(new Properties(), null);
    Message msg = createMessage(session);

    //
    // WHEN / Act
    //
    sendMessage(session, msg);

    //
    // THEN / Assert
    //     fetch messages from server
    MimeMessage[] messages = mailServer.getReceivedMessages();
    assertThat(messages).hasSize(1);
    assertThat(messages[0].getSubject()).isEqualTo(EMAIL_SUBJECT);
    assertThat(messages[0].getContent().toString().trim()).isEqualTo(EMAIL_TEXT);
    assertThat(messages[0].getFrom()[0].toString()).isEqualTo(EMAIL_TO);
}
```

Note:
Should
Arrange
Act
Assert/Verify

+++

#### FIRST

- Fast
- Independant
- Repeateable
- Self-validating
- Timely Fashion

Note:
Fast: on a des miliers de tests, ils doivent s'éxécuter rapidement

Independant: pas de dépendence entre tests, 3 As doivent être bien structurés et isolés

Repeatable: Ne doit pas dépendre de l'environnement, Déterministe -> bien isoler le contexte pour chacun

Self-Validating: on doit voir tout de suite si le teste passe ou pas

Timely: le but est de tester un use case et non couvrir 100% du code

---

#### Exemple : FizzBuzz

<div>
  <img style="vertical-align:top;height:500px;float:left;margin-right:10px;" 
  src="https://raw.githubusercontent.com/atrolla/FormationTDD/master/resources/img/fizzbuzz.png">
  <div class="alignLeft littleFont">Une méthode prend un nombre > 0 en argument et retourne :<br/><br/>
- Fizz pour tous les multiples de 3<br/>
- Buzz pour tous les multiples de 5<br/>
- Le nombre lui-même sinon</div>
</div>
<div style="clear:both"></div>


---


#### TDD c'est facile ?
![Trop facile](https://media.giphy.com/media/3o7btNa0RUYa5E7iiQ/giphy.gif)

---

# Test Driven Development

---

# Test @color[green](Driven) Development

Note: 
Accompagner et Montrer le chemin = aide, oriente + dirige

Test first , importance du guide -> qualité (on y reviendra plus tard)

---

# Test Driven @color[green](Development)

Note: 
Quel est le but ?
Utiliser les avantages des ordinateurs pour aider à résoudre un problème

Avantages :
- Puissance de calcul
- Coût
- Disponibilité

Problème :
Besoin en amont (souvent externe = vient pas de nous)
Attente forte du résultat - Concurrence marché / Optimisation ...

Résultats
Valeur ajoutée (ROI) / Besoin de qualité / Besoin de feedback (frustration)

Qualité -> Clean code ?

+++

#### Extreme Programming

<img src="resources/img/Extreme_Programming.png" style="height:560px;" />

"Agilité appliquée au développement"

Note:
Feedback client => long (ex: notations applis mobiles)

3 lois du TDD => Secondes / Minutes

Red/green/refactor => 10aines de minutes

Green/Refactor/green => Secondes / Minutes

Acceptance tests (BDD ou autre) => Heures

Aka « double loop TDD »


---

# @color[green](Test) Driven Development

Note: 
Pourquoi on teste ?
-> ce n'est pas au client de tester
-> preuve que cela marche dans des conditions (de tests)
-> confiance - image de soi/société

+++

<img src="resources/img/tester-c-est-douter.jpg" style="height:600px;" />

+++

#### Tester

- Casser les illusions
- Découvrir, Comprendre (Documenter)
- Manuel vers Automatique
- Ce n'est pas utiliser le système

Note: 

- Code qui marche et répond au besoin
- Produit qui fait ce qui est attendu
- Process de livraison réactif...

Plusieurs types de tests www.testinsane.com 

- Property Based
- Preuve formelle ?
- Test UI ?

+++


1. A software system can best be designed if the testing is interlaced with the designing instead of being
used after the design.
2. A simulation which matches the requirements contains the control which organizes the design of the
system.
3. Through successive repetitions of this process of interlaced testing and design the model ultimately
becomes the software system itself. 

@snap[south-east text-05 text-right]
http://homepages.cs.ncl.ac.uk/brian.randell/NATO/nato1968.PDF
@snapend

Note:
NATO Software Engineering Conference 1968

+++

@snap[west text-left]
Today a usual technique is to make a program and then to test it. [...]
But one should not first make the program and then prove its correctness, because then the requirement of providing the proof would only increase the poor programmer’s burden.

@css[text-bold](On the contrary: the programmer should let correctness proof and program grow hand in hand.)
@snapend

@snap[south-east text-05 text-right]
Djikstra 1972 - https://www.cs.utexas.edu/~EWD/transcriptions/EWD03xx/EWD340.html
@snapend

Note:
Dijkstra

connu pour son algorithme du plus court chemin ou le diner des philosophes

---

#### Lunch break
![Salt Bae](https://media.giphy.com/media/3o7P4F86TAI9Kz7XYk/giphy.gif)

---

#### TDD : Les promesses (le ROI)

- Documentation vivante Agile
- Spécification technique par l’exemple
- Outil de design ?

Note:
Dans le même repo que le code de production : synchronisée
Exécutable : sa validation est à jour
L’intégration continue, valide cette spécification systématiquement
Documentation c'est les tests, ce sont des exemples

Spécifications par l'exemple, ATDD, on prouve (à soi et au métier s'il faut)
BBD peut être vu comme une spécification fonctionnelle vivante et agile
Écrite avant le code pour implémenter et maintenir la fonctionnalité
Vérifie le comportement attendu, pas les détails d’implémentation

---

#### Inside Out

(Classic Chicago school, bottom-up)

#### Outside In

(London School, top-down, mockist TDD)

Note:
Les mocks/stubs servent à définir l’usage des composants de votre architecture
Outil, et non la silver bullet. Donc ça aide, mais ne fait pas la travail à votre place.
Outil de VOTRE design que vous faites « émerger »

Dummy = coquille vide
Fake = Implementations partielles/simples
Spy = verification appel
Stub = Renvoie des valeurs en dur
Mock = Spy/Stub/Fake

https://www.martinfowler.com/articles/mocksArentStubs.html

+++

#### Double loop TDD

<img src="http://coding-is-like-cooking.info/wp-content/uploads/2013/05/london_school_001.jpg" style="height:560px;" /> 

+++

#### Guide
- Entrainez-vous !
- Focus sur le use-case
- Pas de précipitation
- Réfléchissez avant de coder

---

#### Maintenant : A vous !
![Coffee Break](http://media.giphy.com/media/687qS11pXwjCM/giphy.gif)


---

# Kata(s)

![Kata](https://media.giphy.com/media/gIujbgH7FAkKY/giphy.gif)

---

#### TDD
- Ce n'est pas que du test
- Ce n'est pas du Test First
- Méthodologie
- Outil/Assistant pour le design/développement

---

#### Approfondir le sujet
- Test Commit & Revert
- Behaviour Driven Development
- Autres Paradigmes
- Legacy 
- Clean Code / Design

---

#### Bibliographie / Personnalités
- Kent Beck
- Uncle Bob
- Martin Fowler
- Emilie Bache
- Llewellyn Falco
- Sandro Mancuso
