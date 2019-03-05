![psql practice](https://cdn.pastemagazine.com/www/system/images/photo_albums/cheese-memes/large/h5b39f396.jpeg?1384968217)

You know that problem, where there's so many different types of cheeses in your fridge, that you lose track of 'em?!

Yeah, me neither, I've never had that issue. **Never.** Never, never, ever.

But say we did. To solve this "hypothetical" problem, let's build a `psql` database that will organize all the cheeses.

## Mission

Create a `cheeses_db` database as a collection to store cheeses. Each document should store a **cheese_id, name, color, origin, and stink_level**.

Keep track of your commands! Write out your answers in the provided `cheeses.sql.`



## Setup
Write out your table structure before coding. Which columns will have text or integers? Will you use VARCHAR?

Work directly in PSQL. Run `psql` in your terminal.

Create a table named cheeses.

**Exception** - Wanna write a seed file for all the cheese info (located in the section below)? Go for it! 

#### Buying Cheese

Add these cheeses to your database:

- Roquefort, a yellow french cheese with a stink level of 5
- Epoisses, an orange french cheese with a stink level of 9
- Charolais, a white french cheese with a stink level of 5
- Maroilles, a white french cheese with a stink level of 10
- Durrus, a yellow Irish cheese with a stink level of 2
- Hooligan, a yellow American cheese with a stink level of 3
- Teleme, a white american cheese with a stink level of 2
- Stichelton, a white English cheese with a stink level of 4

#### Choosing Cheese

Now write PostgreSQL queries to accomplish the following:

- Find all the cheeses
- Find all the French cheeses
- Find all the English cheeses
- Find all cheeses with a stink level of 2
- Find all cheeses with a stink level of 10
- Find all yellow cheeses with a stink level of 5
- Find all Irish cheeses with a stink level of 6
- Find all cheeses with a stink level of at least 4, but no greater than 8.
- Find all American and English cheeses.
- Find all cheeses that are not from France.

**TIP** Stuck? Check the [PG documentation](https://www.postgresql.org/docs/)!
Also, [postgresqltutorial.com](http://www.postgresqltutorial.com/postgresql-select/)

#### Restocking Cheese

The cheese game is changing constantly. Let's update our cheeses. Save your queries after you get them working in the command line.

- Change the stink level of Roquefort to 3
- Change the color of Teleme to "mauve"
- Delete the Hooligan cheese
- Change the stink level of Stichelton to be 7
- Add the cheese "Monterey Jack", an American cheese with a stink level of 0
- Add a column named animal_milk with a datatype of VARCHAR(50) to the cheeses table (see table below)
- Add a column named paseurized with a boolean datatype (see table below)
- Add the new cheese data (see table below)
- Change "Monterey Jack" to "Pepper Jack"


|name| animal_milk | pasteurized|
|-------------|------:|------------:|
| Epoisses | cow | true |
| Charolais | goat | false |
| Maroilles | cow | false |
|Durrus | cow | false |
|Roquefort | sheep | false |
|Teleme | cow | true |
|Stichelton | cow | true |
|Monterey Jack| cow | true |

