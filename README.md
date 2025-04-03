## Local Installation

The following instructions are for running the project locally for development.

1. Clone the repository and switch to the project directory

   ```bash
   git clone https://github.com/lukevella/rallly.git
   cd rallly
   ```

2. Install dependencies

   ```bash
   yarn
   ```

3. Setup environment variables

   Create a `.env` file by copying `.env.development`. This will be were you can set your [configuration options](https://support.rallly.co/self-hosting/configuration-options).

   ```bash
   cp .env.development .env
   ```

   **Note:** `.env.development` is preconfigured with default values for development. You can leave these as is for local development.

4. Generate Prisma client

   ```bash
   yarn db:generate
   ```

5. Setup database

   You will need to have [Docker](https://docs.docker.com/get-docker/) installed and running to run the database using the provided docker-compose file.

   To start the database, run:

   ```bash
   yarn docker:up
   ```

   Next run the following command to setup the database:

   ```bash
   yarn db:reset
   ```

   This will:

   - delete the existing database (if it exists)
   - run migrations to create a new database schema
   - seed the database with test users and random data

6. Start the Next.js server

   ```bash
   yarn dev
   ```

 
### Translators 🌐

You can help translate Rallly to another language by following our [guide for translators](https://support.rallly.co/contribute/translations).

 

## Sponsors

Thank you to our sponsors for making this project possible.
 