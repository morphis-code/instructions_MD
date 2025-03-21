### ORM Prism Settings

Prisma installation
`npm i prisma @prisma/client @prisma/cors`

execution:
`npx prisma db pull` Synchronizes the existing database, if you do not have a database already created with a table, do a skima

Migrate:
`npx prisma migrate dev --name fix_users_schema`

**1. `npx`** 
This command executes packages directly from Node.js without needing them globally. In this case, it runs Prisma only for this execution, without leaving anything fixed in the environment.

**2. `prisma`** 
This is the CLI (command line interface) of Prisma, a tool that you are using to manage the database.

**3. `migrate developer`** 
This creates a command and a migration application in the development environment. A migration is basically a “script” that updates the database to reflect the changes made in the `schema.prisma` file.

- Create a `prisma/migrations/` folder with migration files.

- Apply the changes to the database automatically.

**4. `--name fix_users_schema`** 
This is just a descriptive name to identify the migration. Choose something that makes sense for the change you are making — in this case, we are “fixing the users schema”.

After running this, Prisma generates the migration, applies the changes to PostgreSQL, and keeps the change history. This way, you always know what has changed in the database and can revert or adjust it whenever necessary.