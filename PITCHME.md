---?image=resources/img/arolla-software-craftsmanship.jpg

# Formation Clean Code

Note: 
Faire un tour de table, se présenter, demander pourquoi les gens sont là.

---

## C'est quoi le Clean Code ?

Note: 
tour de table, on demande à chacun ce qu'il pense

+++

<img src="resources/img/CleanCode_WordCloud.png" style="height:600px;" />

+++

<img src="resources/img/WTFs_per_minute_Quotient.jpg" style="height:600px;" />

+++

> "Any fool can write code that a computer can understand.Good programmers write code that humans can understand."

_Martin Fowler_

+++

<img src="https://media.giphy.com/media/oFVr84BOpjyiA/giphy.gif" style="height:280px;" />
> “Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live.”

_Martin Golding_

+++

#### Broken Windows Theory
<img src="http://www.watchtower-security.com/wp-content/uploads/2016/11/broken_windows.png" style="height:500px;" />

+++

> “Clean code always looks like it was written by someone who cares.”

_Michael Feathers_

---

<img src="https://images-na.ssl-images-amazon.com/images/I/41wGTnmRTFL._SX375_BO1,204,203,200_.jpg" style="height:500px;" />

Note:
La formation est inspiré de ce livre, où les cas que l'on va voir sont étudiés plus en profondeur

---

#### Meaningful Name

- Use Intention Revealing Names
- Use pronounceable names
- No magical number
- Avoid Encoding (Hungarian notation)
- Avoid Mental Mapping
- Class names use only nouns
(try avoiding words like Manager, Data, Info)
- Method Names must contain a verb

+++ 

#### Comments

<img src="http://geekandpoke.typepad.com/photos/uncategorized/2008/07/24/goodcomments.jpg" style="height:560px;" >

+++

<img src="http://geekandpoke.typepad.com/.a/6a00d8341d3df553ef014e5f3e2868970c-800wi" style="height:560px;"  >

+++

#### Formatting

- Indentation
- Error Handling
- Code Convention

+++

<img src="resources/img/formatting.jpg" style="height:560px;"  >

---

<img src="resources/img/CleanCode-Programme.jpg" style="height:560px;"  >

---

# SLAP

+++

<img src="resources/img/slap.jpg" style="height:560px;"  >

Note:
Single Level of Abstraction Principle
On mélande ici des méthodes d'accès direct à une base de données et des méthodes métiers.
Cela rend le code difficile à lire, car on doit mentalement changer de monde.

+++

<img src="resources/img/slap2.jpg" style="height:560px;"  >

---

# S.O.L.I.D.

Note:
Principes pour l'orienté objet, recommandations d'expert dans le domaine.
Facilite la maintenant, l'évolution, l'adaptation, la scalabilité et le design des applications.

---

## S.O.L.I.D.

#### SRP

+++

<img src="resources/img/SRP.jpg" style="height:560px;"  >

+++

<img src="resources/img/SRP_knife.jpg" style="height:560px;"  >

+++

<img src="http://www.ana-white.com/sites/default/files/DIY%20Kids%20Workbench%20f-4.jpg" style="height:560px;"  >

+++

#### Single Responsibility Principle

###### A class should have one and only one reason to change, meaning that a class should have only one job.

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>Large Class</li>
<li>Long Method</li>
<li>Lot of methods</li>
<li>High Coupling/Low cohesion</li>
<li>Helper class</li>
<li>Multiple functional/technical concepts at the same place</li>
</ul>

---

## S.O.L.I.D.

#### OCP

+++

<img src="resources/img/OCP.jpg" style="height:560px;"  >

Note:
the method have to be changed each time we want to add support for a new directive. It’s therefore not closed for modification.
chaque cas du switch peut être mis à part dans une classe commande, où on lui passe le contexte

+++

<img src="resources/img/ocp2-1.jpg" style="height:560px;"  >

+++

<img src="resources/img/ocp2-2.jpg" style="height:560px;"  >

+++

<img src="resources/img/ocp2-3.jpg" style="height:560px;"  >

Note:
Notez la composition des filtres

+++

#### Open Closed Principle

###### Objects or entities should be open for extension, but closed for modification.

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>High cyclomatic complexity</li>
<li>Complex switch/Lot of ifs </li>
<li>Heavy use of polymorphism</li>
</ul>

---

## S.O.L.I.D.

#### LSP

+++

<img src="resources/img/lsp.jpg" style="height:560px;"  >

+++

<img src="https://lostechies.com/derickbailey/files/2011/03/LiskovSubtitutionPrinciple_52BB5162.jpg" style="height:560px;"  >

+++

#### Liskov Substitution Principle

###### Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>You have to check for the type provided (e.g. instanceof)</li>
<li>Every subclass/derived class should be substitutable for their base/parent class</li>
</ul>

+++

#### Liskov Substitution Principle

###### if S is a subtype of T, an object of type T may be substituted with any object of a subtype S

###### without altering any of the desirable properties of T (correctness, task performed, etc.)

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>You have to check for the type provided (e.g. instanceof)</li>
<li>Every subclass/derived class should be substitutable for their base/parent class</li>
</ul>

---

<img src="https://media.giphy.com/media/eBCnpuRGBhQGY/giphy.gif" style="height:560px;"  >

Note:
C'est bon vous suivez toujours ?

---

## S.O.L.I.D.

#### ISP

+++

<img src="resources/img/isp-printer.jpg" style="height:560px;"  >

+++

<img src="resources/img/isp-printer-java.jpg" style="height:560px;"  >

+++

<img src="resources/img/isp-printer-java2.jpg" style="height:560px;"  >

+++

<img src="resources/img/isp-servlet.jpg" style="height:560px;"  >

+++

<img src="resources/img/isp-servlet2.jpg" style="height:560px;"  >

+++

#### Interface Segregation Principle

###### A client should never be forced to implement an interface that it doesn’t use
or
###### clients shouldn’t be forced to depend on methods they do not use

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>Fat interface/Class with lot of methods</li>
<li>Interface has multiple responsibilities</li>
<li>Difficulties to expose a subset of responsibilities</li>
</ul>

---

## S.O.L.I.D.

#### DIP

+++

<img src="resources/img/dip.jpg" style="height:560px;"  >

+++

<img src="resources/img/dip-2.jpg" style="height:560px;"  >

+++

#### Dependency Inversion Principle

###### Entities must depend on abstractions not on concretions. 

###### It states that the high level module must not depend on the low level module, but they should depend on abstractions.

<p class="smallerFont alignLeft" >Smells : </p>
<ul class="smallerFont">
<li>Dependencies between classes (vs interface)</li>
<li>Monolithic architecture</li>
<li>Abstraction depends on details/implementation</li>
</ul>


+++

#### How to inject with Spring and Annotations !

###### (joking)

+++

<img src="resources/img/annotations.jpg" style="height:560px;"  >

---

<img src="https://media.giphy.com/media/VUgs2T6uHERXO/giphy.gif" style="height:560px;"  >

---

#### YAGNI

###### You Ain't Gonna Need It

+++

#### KISS

###### Keep It SImple Stupid

+++

#### DRY

###### Don't Repeat Yourself

---

#### Go Further

+++

<img src="resources/img/livres.jpg" style="height:560px;"  >

---

#### RPN Calculator

###### Calisthenics

###### Review

+++

#### Calisthenics

- Only One Level Of Indentation Per Method
- Don’t Use The ELSE Keyword
- Wrap All Primitives And Strings
- First Class Collections
- One Dot Per Line
- Don’t Abbreviate
- Keep All Entities Small
- No Classes With More Than Two Instance Variables
- No Getters/Setters/Properties

<p class="smallerFont alignLeft">http://williamdurand.fr/2013/06/03/object-calisthenics/</p>

---

#### Birthday Greeting Kata

Problem: write a program that
- Loads a set of employee records from a flat file
- Sends a greetings email to all employees whose birthday is today

+++

<img src="resources/img/layered-archi.jpg" style="height:560px;"  >

+++

<img src="resources/img/hexa-archi.jpg" style="height:560px;"  >

+++

<img src="resources/img/hexa-archi2.jpg" style="height:560px;"  >

+++

<img src="resources/img/hexa-archi3.jpg" style="height:560px;"  >

