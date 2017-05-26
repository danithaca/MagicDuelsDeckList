README
======

Toy project playing with Magic Duels deck list. Features:

* Directly import card collections and decks into the cloud.
* Automatically create new versions for your decks.
* Share decks with other people.
* Search decks: by cards, popularity, etc.
* Comments decks and cards.
* Look at recommendations for similar decks and similar cards.
* and more ...

Architecture
------------

This project is to try out 1) AWS's serverless architecture, and 2) embeddings for cards/decks.


Components
----------

#### Static web ####

Jekyll + AWS S3 static web hosting

#### User management ####

AWS Cognito: https://github.com/aws/amazon-cognito-identity-js
