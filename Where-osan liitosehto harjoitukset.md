Where-osan liitosehto harjoitukset

1:
SELECT country.name AS "country name", airport.name AS "airport name"
FROM country, airport
WHERE country.name = "Iceland"
AND country.iso_country = airport.iso_country;
![Näyttökuva where teht 1](https://github.com/user-attachments/assets/253919bb-66b5-44c9-83c8-ef155856df6e)

2:
SELECT airport.name AS "airport name"
FROM country, airport
WHERE country.name = "France"
AND country.iso_country = airport.iso_country
AND airport.type = "large_airport";
![Näyttökuva where teht 2](https://github.com/user-attachments/assets/097e9d41-7a50-492f-b90f-2b51bdfffad5)

3:
SELECT country.name AS country_name, airport.name AS airport_name
FROM country, airport
WHERE country.continent = "AN"
AND country.iso_country = airport.iso_country;
![Näyttökuva where teht 3](https://github.com/user-attachments/assets/764e0a9e-6958-4b83-aeec-99d585b9ad62)

4:
SELECT elevation_ft
FROM airport, game
WHERE screen_name = "Heini"
AND game.location = airport.ident;
![Näyttökuva where teht 4](https://github.com/user-attachments/assets/b18eb654-9fff-4aeb-822c-c921eaf01bb7)

5:
SELECT elevation_ft*0.3048 AS elevation_m
FROM airport, game
WHERE screen_name = "Heini"
AND game.location = airport.ident;
![Näyttökuva where teht 5](https://github.com/user-attachments/assets/2abc58b5-6df9-49b9-8068-da569bee115d)

6:
SELECT airport.name
FROM airport, game
WHERE screen_name = "Ilkka"
AND game.location = airport.ident;
![Näyttökuva where teht 6](https://github.com/user-attachments/assets/7f16ac96-0bb0-4d11-938b-c3912a6d4311)

7:
SELECT country.name
FROM airport, game, country
WHERE game.screen_name = "Ilkka"
AND game.location = airport.ident
AND airport.iso_country = country.iso_country;
![Näyttökuva where teht 7](https://github.com/user-attachments/assets/b66cfd8d-5e5a-49dc-b8be-c02305b20e35)

8:
SELECT goal.name
FROM goal, goal_reached, game
WHERE game.screen_name = "Heini"
AND game.id = goal_reached.game_id
AND goal_reached.goal_id = goal.id;
![Näyttökuva where teht 8](https://github.com/user-attachments/assets/32b8cdd9-5255-4c1b-baa5-2b447c6a1939)

9:
SELECT airport.name
FROM airport, game, goal_reached, goal
WHERE game.screen_name = "Ilkka"
AND game.location = airport.ident
AND game.id = goal_reached.game_id
AND goal_reached.goal_id = goal.id
AND goal.name = "CLOUDS";
![Näyttökuva where teht 9](https://github.com/user-attachments/assets/2712fbff-dd20-4031-9241-1317ed44e045)

10:
SELECT country.name
FROM airport, game, goal_reached, goal, country
WHERE game.screen_name = "Ilkka"
AND game.location = airport.ident
AND airport.iso_country = country.iso_country
AND game.id = goal_reached.game_id
AND goal_reached.goal_id = goal.id
AND goal.name = "CLOUDS";
![Näyttökuva where teht 10](https://github.com/user-attachments/assets/4ffae3e9-e6fa-4aa1-bb29-48a2ecc040cc)
