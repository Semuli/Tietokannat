Yhteen tauluun kohdistuvien kyselyiden harjoitukset

Tehtävä 1
SELECT * FROM goal;
![Näyttökuva yteen tauluun teht 1](https://github.com/user-attachments/assets/264d4a02-c50f-403e-9869-768ccfe45bb8)

Tehtävä 2
SELECT name, type FROM airport WHERE iso_country = "FI";
![Näyttökuva yhteen tauluun teht 2](https://github.com/user-attachments/assets/d982b92a-1b0d-413d-9126-1d7083119829)

Tehtävä 3
SELECT name FROM airport where iso_country = "FI" ORDER by name;
![Näyttökuva yhteen tauluun teht 3](https://github.com/user-attachments/assets/0f743f86-703a-4fd9-a4fa-e1521e060e4a)

Tehtävä 4
SELECT name, type FROM airport WHERE iso_country = "FI" ORDER BY type, name;
![Näyttökuva yhteen tauluun teht 4](https://github.com/user-attachments/assets/0bb8e7db-639a-4769-a813-41290de04c96)

Tehtävä 5
SELECT name FROM country WHERE name LIKE "f%";
![Näyttökuva yhteen tauluun teht 5](https://github.com/user-attachments/assets/45a5e115-0222-4ff3-9b83-583700e51c33)

Tehtävä 6
SELECT name
FROM country
WHERE name LIKE "%f%";
![Näyttökuva yhteen tauluun teht 6](https://github.com/user-attachments/assets/58f8c168-b1fd-480a-a7d4-9aa67e32172a)


Tehtävä 7
SELECT location
FROM game
WHERE screen_name = "Vesa";
![Näyttökuva yhteen tauluun teht 7](https://github.com/user-attachments/assets/9d5c3f93-17a9-4b60-974c-215f3f46e751)


Tehtävä 8
SELECT co2_consumed
FROM game
WHERE screen_name = "Ilkka";
![Näyttökuva yhteen tauluun teht 8](https://github.com/user-attachments/assets/59717e98-c285-40dd-942e-9bbf998af2b0)


Tehtävä 9
SELECT DISTINCT co2_budget
FROM game;
![Näyttökuva yhteen tauluun teht 9](https://github.com/user-attachments/assets/f40b87ab-9d1a-4ac7-b8ca-a71bc2bd3352)


