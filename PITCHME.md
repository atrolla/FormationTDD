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

CleanCode
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

+++?gist=kondo-takuto-mulodo/20968d8720c38cf3ff58&lang=Java

---

<img src="resources/img/CleanCode-Programme.jpg" style="height:560px;"  >

---

# SLAP

+++

<img src="resources/img/formatting.jpg" style="height:560px;"  >

Note:
Single Level of Abstraction Principle
On mélande ici des méthodes d'accès direct à une base de données et des méthodes métiers.
Cela rend le code difficile à lire, car on doit mentalement changer de monde.

+++

<img src="resources/img/slap.jpg" style="height:560px;"  >

---

#S.O.L.I.D.

---

## S.O.L.I.D.

#SRP

---