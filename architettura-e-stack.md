# Architettura e Stack

L'applicativo si basa su un architettura distribuita e multi-livello, le tre componenti principali della stessa sono:

* RML - DB documentale MongoDB
* ALL e PL - Applicazione server in TypeScript

{% hint style="info" %}
Dato l'utilizzo del rendering lato server **ALL** e **PL** lavorano all'interno dello stesso livello, e sono   
quindi considerate un tutt'uno.
{% endhint %}

![Architettura dell&apos;applicativo](.gitbook/assets/image%20%281%29.png)

{% file src=".gitbook/assets/architetturasemplice.pdf" caption="Schema riassuntivo" %}

### Stack

L'applicazione è realizzata basandosi sul framework Nest \([https://docs.nestjs.com/](https://docs.nestjs.com/)\), in linguaggio TypeScript successivamente compilato in JavaScript per essere eseguito dalla runtime Node.

Il framework di cui sopra sfrutta il principio dell'inversione di controllo e fa ricco utilizzo dei decorator, consentendo così un approccio semplice e leggibile nella realizzazione di endpoint e controller.

Le visuali sono renderizzate dal server mediante l'utilizzo del pattern MVC \([https://www.codecademy.com/articles/mvc](https://www.codecademy.com/articles/mvc)\) e costruite seguendo le istruzioni dei template EJS.

