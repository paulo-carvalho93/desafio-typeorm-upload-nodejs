# Node.js TypeORM and Upload File
Node.js fundamentals challenge applied for the GoStack Bootcamp

## :rocket: About the challenge

In this challenge, I've must continue to develop the transaction management application, GoFinances. Now I will practice what I've have learned so far in React.js along with TypeScript, using routes and sending files by form.

This will be an application that will connect to my [Challenge 06](https://github.com/paulo-carvalho93/desafio-fundamentos-nodejs) back-end, and display the transactions created and allow the import of a CSV file to generate new records in the database.

## :hammer: Do you want to check it out?

Clone the repository:

```sh
  $ git clone https://github.com/paulo-carvalho93/desafio-typeorm-upload-nodejs.git
```

```sh
  $ desafio-typeorm-upload-nodejs
  # Installing project dependencies
  $ yarn # or npm install
  
  # Running unit tests
  $ yarn test # or npm test

  # Start API
  $ yarn dev:server # or npm dev:server

```

## POST - IMPORT CSV http://localhost:3333/transactions/import
```sh

You can find the file inside the test folder.
```

## POST - http://localhost:3333/transactions
```sh
    {
      "title": "House",
      "value": 140000,
      "type": "outcome",
			"category": "Properties"
    },
    {
      "title": "Lottery",
      "value": 2000000,
      "type": "income",
			"category": "Lucky"
    }

```

## GET - http://localhost:3333/transactions
```sh
{
  "transactions": [
    {
      "id": "62500601-fa5f-4359-8358-bb884566ce8d",
      "title": "Loan",
      "type": "income",
      "value": "1500.00",
      "category_id": "6d205f93-6d38-4228-bc8f-ac6292639f91",
      "created_at": "2020-11-12T02:29:21.346Z",
      "updated_at": "2020-11-12T02:29:21.346Z"
    },
    {
      "id": "4c06b395-4ffe-416e-88ef-4070774290f1",
      "title": "Website Hosting",
      "type": "outcome",
      "value": "50.00",
      "category_id": "6d205f93-6d38-4228-bc8f-ac6292639f91",
      "created_at": "2020-11-12T02:29:21.346Z",
      "updated_at": "2020-11-12T02:29:21.346Z"
    },
    {
      "id": "0850d442-359d-468c-93a8-b34faad13d5a",
      "title": "Ice cream",
      "type": "outcome",
      "value": "3.00",
      "category_id": "6cffd494-2bfa-4318-ab11-056a0c34a765",
      "created_at": "2020-11-12T02:29:21.346Z",
      "updated_at": "2020-11-12T02:29:21.346Z"
    }
  ],
  "balance": {
    "income": 1500,
    "outcome": 53,
    "total": 1447
  }
}
```

## DELETE - http://localhost:3333/transactions/{ID-TRANSACTION}

