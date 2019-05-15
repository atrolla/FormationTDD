# RPN Calculator

public double calculate(String formula)
où la formule est une expression valide en notation polonaise inversée.


- 5 3 + => 5+3 => 8
- 6 2 / => 6/2 => 3
- 5 2 - 7 + => 10
- 7 5 2 - + => 10
- 3 5 8 x 7 + x => 3x((5x8)+7) => 141
- 3 4 2 1 + x + 2 / => (3 + (4 x (2+1)))/2 => 7.5
- 1 2 + 4 × 5 + 3 − => ((1+2) x 4) + 5 - 3 => 14

***

# Wallet

Given a Wallet containing currencies, build a function that compute the value of wallet in a currency.

To value the wallet in a Currency you can use external api to provide rate exchanges (some are provided below).

Implementation example:
```
Wallet(Money(5, USD)).value(EUR, rateProvider)
```

With rateProvider:
```
rateProvider.rate(FromCurrency, ToCurrency)
```

Suggested rates sources
Some APIs can be used to provides rates:

- http://api.fixer.io/
- https://1forge.com/forex-data-api
- https://finance.google.com/

derived from http://codingdojo.org/kata/Wallet/

***

