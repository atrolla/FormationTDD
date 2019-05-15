# Racing Cars

https://github.com/emilybache/Racing-Car-Katas

***

# Birthday Greeting

Problem: write a program that
- Loads a set of employee records from a flat file
- Sends a greetings email to all employees whose birthday is today

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

