Angular source files are in /client folder

To re-build the angular files, go to the client folder on the command line and run:
$ npm install
$ ng build

Copy the contents in dist/client and paste in mvn static folder

Environment Variables:
<!-- generate the bearer token to access the twitter api and build filter stream rules -->
TWITTER_BEARER_TOKEN 

<!-- the gmail account to send emails from. access to less secure apps should be enabled in Goole account -->
GMAIL_USERNAME 
GMAIL_PASSWORD

<!-- mysql connection can be configured under application.properties -->
<!-- database password is in the environment variable DB_PASSWORD -->
DB_PASSWORD

<!-- for the demo project, a FTX API Key is used. this can be generated from creating a FTX account, then create a subaccount named 'Bot', and generate a API Key for the 'Bot' subaccount -->
FTX_KEY
FTX_SECRET

Database Deployment:
The database should be created with the schema and data provided in schema.sql
The database is written in MySQL dialect
Data in table `twitter` is built by adding rules to twitter api using an assigned bearer token. The fields `rule_id`, `value`, and `tag` needs to be re-build when using another twitter bearer token. For same results, copy the fields `value` and `tag` when adding rules to the twitter api