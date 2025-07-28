# API gestion de produits en stock
Conception et développement d'une API  pour la gestion de produits, basée sur le framework Express.js et connectée à une base de données MongoDB pour le stockage des données.
##  Fonctionnalités
- Operation de CREUD
- Definition des routes pour le CREUD
- Tester l'API grace a l'outils REST CLEINT
## Technologies utilisées

- Node.js
- Express.js 
- MongoDB
- Dotenv
## Processus de test des requêtes
### Methode: `GET`: récuperer la liste de tous les produits.
- URL:`http://localhost:3000/produits` 
- Reponse:
  {
  "afficheProduit": [
    {
      "_id": "688366b3c1c791417a21c970",
      "productName": "banane",
      "price": 300.6,
      "stockStatus": "petite stock",
      "__v": 0
    },
    {
      "_id": "688366e5c1c791417a21c973",
      "productName": "salade",
      "price": 5000,
      "stockStatus": "pas en stock",
      "__v": 0
    },
    {
      "_id": "6883a0cf2883aa2c4340db11",
      "productName": "viande",
      "price": 2000,
      "stockStatus": "petite stock",
      "__v": 0
    },
    {
      "_id": "68874949f605ecc574781bd2",
      "productName": "Pomme",
      "price": 500.5,
      "stockStatus": "en stock",
      "__v": 0
    },
    {
      "_id": "68874a13f605ecc574781bd5",
      "productName": "Pomme de terre",
      "price": 1000,
      "stockStatus": "en stock",
      "__v": 0
    },
    {
      "_id": "688756eab7bc3d264336c7b2",
      "productName": "Pomme de terre",
      "price": 1000,
      "stockStatus": "en stock",
      "__v": 0
    }
  ]
}

 ### Methode: `GET`:récuperer un produit par son ID.
- URL: ` http://localhost:3000/produits/688366b3c1c791417a21c970`
- Reponse:
  {
  "recupereProduit": {
    "_id": "688366b3c1c791417a21c970",
    "productName": "banane",
    "price": 300.6,
    "stockStatus": "petite stock",
    "__v": 0
  }
}

### Methode: `POST`:ajouter un nouvel produit
- URL: `http://localhost:3000/produits`
- Reponse:
  {
  "message": "le produit a étè ajouter avec succes",
  "produit": {
    "productName": "Pomme de terre",
    "price": 1000,
    "stockStatus": "en stock"
  }
}

  ## Methode: `PATH`:mettre à jour un produit excepté son status en stock.
- URL: `http://localhost:3000/produits/688366b3c1c791417a21c970`
- Reponse:
  {
  "message": "produit mis a jour",
  "updatedProduit": {
    "_id": "688366b3c1c791417a21c970",
    "productName": "banane",
    "price": 300.6,
    "stockStatus": "petite stock",
    "__v": 0
  }
}

### Methode: `PATH`:mettre à jour le status du produit en stock.
- URL: `http://localhost:3000/produits/688366b3c1c791417a21c970/petite stock`
- Reponse:
  {
  "message": "produit mis a jour",
  "updatedProduit": {
    "_id": "688366b3c1c791417a21c970",
    "productName": "banane",
    "price": 300.6,
    "stockStatus": "petite stock",
    "__v": 0
  }
}

### Methode: `DELETE`:supprimer un produit
- URL: `http://localhost:3000/produits/688732375aabed82d9be3efb`
- Reponse:
  {
  "message": "produit mis a jour",
  "updatedProduit": {
    "_id": "688366b3c1c791417a21c970",
    "productName": "banane",
    "price": 300.6,
    "stockStatus": "petite stock",
    "__v": 0
  }


  <img width="800" height="690" alt="image" src="https://github.com/user-attachments/assets/727826af-f6f7-4e07-9eb8-5ce6dc161499" />
