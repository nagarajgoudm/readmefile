Import and export keyspace or schema in cassandra
This command line will export a keyspace from Cassandra:

cqlsh -e "DESCRIBE KEYSPACE test" > /your/path/test.cql
this one will export a schema from Cassandra:

cqlsh -e "DESCRIBE SCHEMA" > /your/path/schema.cql
Then, you can import it with:

cqlsh -e "SOURCE /your/path/test.cql"

cqlsh -e "SOURCE /your/path/schema.cql"
You can also open the terminal in the location of cql file and then open cqlsh shell. Therefore, it is not necessary to write all path:

cd /your/path
cqlsh -e "SOURCE test.cql"
