![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) 

# SQL Select Lab

![psql practice](https://cdn.pastemagazine.com/www/system/images/photo_albums/cheese-memes/large/h5b39f396.jpeg?1384968217)

You know that problem, where there's so many different types of cheeses in your fridge, that you lose track of 'em?!

Yeah, me neither, I've never had that issue. Never. Never, never, ever.

But say we did. To solve this "hypothetical" problem, let's build a psql database that will organize all the cheeses.

## Setup

- clone
- `cd` into the repo
- Create a `cheeses_db` database as a collection to store cheeses.

```SQL

# Enter psql
psql

# Create database
CREATE DATABASE cheeses_db;
```

-- OR --

directly from our bash terminal command line:
```BASH

createdb cheeses_db
```

## Schema and Seed

Use the `base.sql` as your "schema and seed file"

Create a table named `cheeses`. Each record should store a **name, color, origin, and stink_level**. This can all be written out inside of the `base.sql` file.

#### Buying Cheese

Add these cheeses to your database as seed data:

- Roquefort, a yellow french cheese with a stink level of 5
- Epoisses, an orange french cheese with a stink level of 9
- Charolais, a white french cheese with a stink level of 5
- Maroilles, a white french cheese with a stink level of 10
- Durrus, a yellow Irish cheese with a stink level of 2
- Hooligan, a yellow American cheese with a stink level of 3
- Teleme, a white american cheese with a stink level of 2
- Stichelton, a white English cheese with a stink level of 4

When you are ready to run this file, you can do so with the following command in terminal:

```
# Enter psql
psql

# Connect to cheeses_db
\c cheeses_db
\i base.sql
```

**Pro Tip:** You can do this in one step with the command:

```bash
psql -d cheeses_db -f base.sql
```

> if you ever need to reset your data, just re-run `base.sql`. It will clear out the database and then re-create everything, including the seed data.

## Selecting and Modifying data

Use the `cheesy.sql` as your "answer sheet". From here on out, we will be tinkering with our data.

Remember if your data gets too messy, you can always reset by re-running the `base.sql` file.

#### Choosing Cheese

Now write PostgreSQL queries to accomplish the following. Write out your answers in the provided `cheeses.sql`. You can check your answers by running the file the same way that you ran the `base.sql` file.

> If you prefer to test inside of the `psql` terminal repl, remember to record your working answers to the `cheeses.sql` file.

- Find all the cheeses
- Find all the French cheeses
- Find all the English cheeses
- Find all cheeses with a stink level of 2
- Find all cheeses with a stink level of 10
- Find all French cheeses with a stink level of 5
- Find all Irish cheeses with a stink level of 6
- Find all cheeses with a stink level of at least 4, but no greater than 8.
- Find all American and English cheeses.
- Find all cheeses that are not from France.

**TIP** Stuck? Check the [PG documentation](https://www.postgresql.org/docs/)!


#### Restocking Cheese

The cheese game is changing constantly. Let's update our cheeses.

- Change the stink level of Roquefort to 3
- Change the color of Teleme to "mauve"
- Delete the Hooligan cheese
- Change the stink level of Stichelton to be 7
- Add the cheese "Monterey Jack", an American cheese with a stink level of 0
- Add a column named animal_milk with a datatype of VARCHAR(50) to the cheeses table
- Add a column named pasteurized with a boolean datatype to the cheeses table 
- Add the new cheese data (see table below)
- Change "Monterey Jack" to "Pepper Jack"


| name | animal_milk | pasteurized |
| ------------- | ------:| ------------:|
| Epoisses | cow | true |
| Charolais | goat | false |
| Maroilles | cow | false |
| Durrus | cow | false |
| Roquefort | sheep | false |
| Teleme | cow | true |
| Stichelton | cow | true |
| Monterey Jack | cow | true |

