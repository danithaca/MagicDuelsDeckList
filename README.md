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

Data Structure
--------------

#### Deck ####

```json
{
  "user_name": "danithaca",
  "deck_name": "Mardu Vehicle",
  "description": "A deck example",
  "private_note": "Private note, not to be shared with other people",
  "created": "2017-05-12T01:12:23.111Z",
  "updated": "2017-05-12T01:12:23.111Z",
  "is_public": false,
  "user_rating": 8.0,
  "tags": ["...", "..."],
  "values": {"strength": 6.9},
  "builds": {
      "2017-05-12T01:12:23.111Z": { 
        "cards": [],
        "lands": {}
      }
  }
}
```

#### Profile Deck List ####

```json
[
  {
    "deck_name": "Mardu Vehicle",
    "cards": [
      {
        "duels_id": 111,
        "multiverse_id": 1112,
        "count": 111
      }
    ],
    "lands": {"plains": 15, ...}
    "values": {"strength": 0.56},
    "online_number": 11112
  }
]
```