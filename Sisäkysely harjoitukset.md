1.
SELECT name
FROM country
where iso_country in (
SELECT iso_country
FROM airport
WHERE name LIKE "Satsuma%");
![Sisäkysely teht 1](https://github.com/user-attachments/assets/74c7dbf0-cb1d-4a40-a6a3-96cd5329915d)

2.
SELECT name
FROM airport
WHERE iso_country IN (
SELECT iso_country
FROM country
WHERE name like "monaco");
![Sisäkysely teht 2](https://github.com/user-attachments/assets/ed64ddb7-a710-40a8-8796-90387c91c2a8)

3.
SELECT screen_name
FROM game
WHERE id IN (
SELECT game_id
FROM goal_reached
WHERE goal_id IN (
SELECT id
FROM goal
WHERE name LIKE "clouds"));
![Sisäkysely teht 3](https://github.com/user-attachments/assets/fe3434ee-f771-4349-9637-94ff456b86af)

4.
SELECT name
FROM country
WHERE iso_country NOT IN (
SELECT iso_country
FROM airport);
![Sisäkysely teht 4](https://github.com/user-attachments/assets/731ab3f9-5d97-4b7f-92b9-5cc54ef62268)

5.
SELECT name
FROM goal
WHERE id NOT IN (
SELECT goal_id
FROM goal_reached
WHERE game_id IN (
SELECT id
FROM game
WHERE screen_name LIKE "Heini"));
![Sisäkysely teht 5](https://github.com/user-attachments/assets/3f13a5c8-8a66-4755-8064-c3b4d010f604)
