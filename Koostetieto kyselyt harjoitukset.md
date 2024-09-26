1.
SELECT max(elevation_ft)
FROM airport;
![kooste teht 1](https://github.com/user-attachments/assets/c22f7b91-8caf-4c80-8aed-708c6e240cb8)

2.
SELECT continent, count(*)
FROM country
GROUP BY continent;
![kooste teht 2](https://github.com/user-attachments/assets/1ac2b7ea-fc7f-49b1-ae4f-5f7b5b712e6b)

3.
SELECT screen_name, count(*)
FROM game, goal_reached
WHERE game_id = id
GROUP BY screen_name;
![kooste teht 3](https://github.com/user-attachments/assets/1a98d9a7-33b4-4aaf-99a1-714107c065bf)

4.
SELECT screen_name
FROM game
WHERE co2_consumed IN(
SELECT min(co2_consumed)
FROM game);
![kooste teht 4](https://github.com/user-attachments/assets/dd9531c1-9883-4e21-b615-1d20ff7d4f5a)

5.
SELECT country.name, count(*)
FROM country, airport
WHERE country.iso_country = airport.iso_country
GROUP BY airport.iso_country
ORDER BY count(*) DESC
LIMIT 50;
![kooste teht 5](https://github.com/user-attachments/assets/14b342f8-723f-4765-be6b-05811dcf32ed)

6.
SELECT name
FROM country
WHERE iso_country IN (
SELECT iso_country
FROM airport
group BY iso_country
HAVING count(*) >1000);
![kooste teht 6](https://github.com/user-attachments/assets/e9d9bf4a-f302-47bb-ac52-63e1d48b0698)

7.
SELECT name
FROM airport
WHERE elevation_ft IN (
SELECT max(elevation_ft)
FROM airport);
![kooste teht 7](https://github.com/user-attachments/assets/287700bc-4c95-44e7-ac62-0f62949630af)

8.
SELECT name
FROM country
WHERE iso_country IN (
SELECT iso_country
FROM airport
WHERE elevation_ft IN (
SELECT max(elevation_ft)
FROM airport));
![kooste teht 8](https://github.com/user-attachments/assets/f00abc72-d694-47a1-8a3f-bd27c59003dc)

9.
SELECT count(*)
FROM game
WHERE screen_name = "Vesa"
group BY id IN (
SELECT game_id
FROM goal_reached);
![kooste teht 9](https://github.com/user-attachments/assets/05d6e408-3784-4e14-8d12-62b8fd747383)

10.
SELECT name
FROM airport
WHERE latitude_deg IN (
SELECT min(latitude_deg)
FROM airport);
![kooste teht 10](https://github.com/user-attachments/assets/ebfdeb0e-5211-4705-8636-fcbe41fd2310)
