---
title: How to connect to Postgres on Heroku?
created: 2018-12-28T00:00:00Z
description: Use SanchoSQL database client to set up a connection to a PostgreSQL instance running on Heroku.
keywords: Heroku postgres instance, help, SanchoSQL help and FAQ, How to connect to Postgres on Heroku?, desktop database client, postgres, linux, SanchoSQL, GTK+, GTKmm, PostgreSQL on Heroku, heroku
---

**SanchoSQL** can be used with a Postgres instance running on Heroku. Here's how to do it.

### Get credentials for Postgres running on Heroku

Go to configuration of your Postgres add-on. Click on **View credentials** button.

![Heroku Postgres credentials](./data/heroku_postgres_credentials_1.png)

Then, you should see credentials for your database. We'll use them to set up a connection in **SanchoSQL**!

![Heroku Postgres credentials](./data/heroku_postgres_credentials_2.png)


### Configure connection in Heroku Postgres in SanchoSQL

1. Open SanchoSQL

2. Select **Connections** (shortcut Control-N) option from the menu (**File** -> **Connections**)

3. Click **Add** button in the next window to create a new connection.

![SanchoSQL - Heroku connection configuration](./data/sancho_heroku_postgres_setup.png)

Now, you need to fill in the connection details (using the values from Heroku):

- **Connection name** - name that describes this connection

- **Host**

- **Database name**

- **Port** - `5432` by default

- **Username**

- **Password**

When you set all fields - you can click on the **Test connection** button to check if a connection can be established successfully. If you see **Success** - congratulations! It works as expected!

