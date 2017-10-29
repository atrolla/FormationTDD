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

<img src="resources/img/tester-c-est-douter.jpg" style="height:600px;" />

---

#### Comment on teste ?

- Manuel vers Automatique
- QA pour la conception, Dev pour la réalisation
- Tests à postériori vers Tests avant implémentation

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

Les mocks/stubs servent à définir l’usage des composants de votre architecture
Outil, et non la silver bullet. Donc ça aide, mais ne fait pas la travail à votre place.
Outil de VOTRE design que vous faites « émerger »

---

#### La méthodologie

<img src="resources/img/Extreme_Programming.png" style="height:560px;" />

"Agilité appliquée au développement"

Note:
3 lois du TDD => Secondes / Minutes
Red/green/refactor => 10aines de minutes
Green/Refactor/green => Secondes / Minutes
Acceptance tests (BDD ou autre) => Heures
Aka « double loop TDD »

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

+++

#### Inside Out

(Classic Chicago school, bottom-up)

#### Outside In

(London School, top-down, mockist TDD)

+++

#### Double loop TDD

<img src="http://coding-is-like-cooking.info/wp-content/uploads/2013/05/london_school_001.jpg" style="height:560px;" /> 

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
  <img style="vertical-align:top;height:500px;float:left" src="https://raw.githubusercontent.com/atrolla/FormationTDD/master/resources/img/fizzbuzz.png" style="">
  <div class="alignLeft littleFont">Une méthode prend un nombre > 0 en argument et retourne :<br/><br/>
- Fizz pour tous les multiples de 3<br/>
- Buzz pour tous les multiples de 5<br/>
- Le nombre lui-même sinon</div>
</div>
<div style="clear:both"></div>

+++

#### Maintenant : A vous !
![Coffee Break](http://media.giphy.com/media/687qS11pXwjCM/giphy.gif)

+++

#### A vous : Leap Year

<p class="alignLeft">Une méthode qui retourne vrai ou faux selon 
que l’entier en argument est une année bissextile ou non.</p>
<p class="alignLeft">
Une année bissextile est divisible par 4, mais n’est pas divisible par 100 
à moins qu’elle soit aussi divisible par 400.</p>
<p class="alignLeft">
2001 est une année normale typique<br/>
1996 est une année bissextile typique<br/>
1900 est une année normale atypique<br/>
2000 est une année bissextile atypique<br/>
</p>

+++

#### Lunch break
![Salt Bae](https://media.giphy.com/media/3o7P4F86TAI9Kz7XYk/giphy.gif)