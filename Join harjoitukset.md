1.
SELECT country.name AS "country name", airport.name AS "airport name"
FROM airport
INNER JOIN country ON airport.iso_country = country.iso_country
AND country.name = "Finland"
AND airport.scheduled_service = "yes";
![Näyttökuva join teht 1](https://github.com/user-attachments/assets/d1b901eb-d963-402f-a027-c13459ce7f9a)

2.
SELECT screen_name, name
FROM game
INNER JOIN airport ON location = ident;
![Näyttökuva join teht 2](https://github.com/user-attachments/assets/c702c79a-c0b5-4afa-ae28-f610534ccf71)

3.
SELECT screen_name, country.name
FROM game
INNER JOIN airport ON location = ident
INNER JOIN country ON airport.iso_country = country.iso_country;
![Näyttökuva join teht 3](https://github.com/user-attachments/assets/eb19b771-3629-448b-80cc-99bba8a7eaca)

4.
SELECT airport.name, screen_name
FROM airport
LEFT JOIN game ON ident = location
WHERE airport.name LIKE "%hels%";
![Näyttökuva join teht 4](https://github.com/user-attachments/assets/d6bcc3b6-32c9-4d73-8a89-1162577f62ce)

5.
SELECT name, screen_name
FROM goal
LEFT JOIN goal_reached ON goal_reached.goal_id = goal.id
LEFT JOIN game ON goal_reached.game_id = game.id;
![Näyttökuva join teht 5](https://github.com/user-attachments/assets/3f541519-68a7-4ca2-8999-1ded4dfa35d8)
