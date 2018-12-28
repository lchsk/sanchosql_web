---
title: How to connect to Postgres on AWS?
created: 2018-12-28T00:00:00Z
description: Use SanchoSQL database client to set up a connection to a PostgreSQL instance running on AWS.
keywords: AWS, RDS postgres instance, help, SanchoSQL help and FAQ, How to connect to Postgres on AWS?, desktop database client, postgres, linux, SanchoSQL, GTK+, GTKmm, PostgreSQL on AWS, amazon, postgres RDS on aws
---

**SanchoSQL** can be used with a Postgres instance running on AWS (Amazon RDS). Here's how to do it.

### Create a new Postgres database in [Amazon RDS (Relational Database Service) console](https://aws.amazon.com/rds/).

When creating a new instance, note username and password.

If you already have one, go to the dashboard.

You should see something similar to this:

![AWS Postgres RDS dashboard](./data/aws_rds_dashboard.png)

Take note of `DB Name`, `Endpoint`, `Port`, and `Public accessibility` (should be set `Yes`)

### Set up access in security group rules

**Warning!** The following example will enable establishing connections from all over the Internet. Before doing this, consider your use case and make sure it's safe!

Go to security group rules settings and click on the **Inbound** entry.

![AWS security groups](./data/aws_security_group_rules.png)

Then, check the **Inbound** tab. The settings below enable access from anywhere, so be careful!

![AWS security groups](./data/aws_postgres_inbound_settings.png)

You can also click **Edit** and alter the configuration so that only connections from your IP will be accepted:

![AWS postgres inbound rules](./data/aws_postgres_inbound_rules.png)

After that, we can configure the connection in **SanchoSQL**!

### Configuring connection in SanchoSQL

1. Open SanchoSQL

2. Select **Connections** (shortcut Control-N) option from the menu (**File** -> **Connections**)

3. Click **Add** button in the next window to create a new connection.

![SanchoSQL - AWS connection configuration](./data/sanchosql_aws_connection.png)

Now, you need to fill in the connection details:

- **Connection name** - name that describes this connection

- **Host** - corresponds to **Endpoint** from the AWS dashboard

- **Database name** - **DB Name** from the AWS dashboard

- **Port** - `5432` by default

- **Username** - you've set it when you have created new database

- **Password** - you've set it when you have created new database

When you set all fields - you can click on the **Test connection** button to check if a connection can be established successfully. If you see **Success** - congratulations! It works as expected!

