# Sunshine Coffee API

Sunshine Coffee API er et api med brugerstyring og mulighed for at hente produkter, oprette brugere og logge ind.
Dette API er lavet så du blot skal downloade det og sætte det op.

## Guide til installation

1. Start med at hente projektet ned. Herefter skal du navigere til roden og køre
   `npm install`

2. Opret en ny fil .env i roden og indsæt følgende:
   _Husk at indsætte USER, PASSWORD og DB, som kommer fra din database_
   _Bruger du en anden DB end MySQL skal DIALECT også tilrettes_

```
PORT=8081
JWT_REFRESH_EXPIRATION=30000000
JWT_EXPIRATION=1400000
JWT_SECRET=64_CIFRE_LANG_KODE_HER
HOST=localhost
USERNAME=root
PASSWORD=DIT_ROOT_PASSWORD
DIALECT=mysql
DB=sunshine
```

3. Åben dit foretrukne program til at styre din database (mysql workbench) og opret en ny database ved navn: `sunshine`

4. Gå ind i filen config.json og ændre password til dit DB password

5. Kør kommandoen: `node server.js` for at oprette tables i databasen

6. Luk serveren igen og kør kommandoen: `npx sequelize-cli db:seed:all`

7. Nu skulle du kunne starte serveren ved at skrive i terminalen:
   `node server.js`

## Api dokumentation

[Link til postman dokumentation](https://documenter.getpostman.com/view/31531123/2sB2j6BB2o)

#### USER MANAGEMENT

```
    - /sign-up (params: email, password)
    - /sign-in (params: email, password )
```

#### PRODUCTS - Hent alle eller hent efter specifikt ID

```
    - /products/
    - /products/:id
```
