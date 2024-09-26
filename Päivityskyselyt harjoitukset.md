1.
UPDATE game
set co2_consumed = co2_consumed + 500
WHERE screen_name = "Vesa";
UPDATE game
set location = (
SELECT ident
FROM airport
WHERE name = "Nottingham Airport")
WHERE screen_name = "Vesa";


3.

delete FROM goal_reached;
SELECT * FROM goal_reached;


4.

delete FROM game;
SELECT id, co2_consumed, screen_name, location
FROM game;
