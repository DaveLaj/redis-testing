# Redis Commands

Redis has a rich set of commands that can be used to interact with the datastore.

## Basic Commands

- `SET key value`: Set the value of a key.
- `GET key`: Get the value of a key.
- `DEL key`: Delete a key.
- `EXISTS key`: Check if a key exists.
- `TYPE key`: Get the type of a key.
- `KEYS pattern`: Get all keys matching a pattern.
- `RANDOMKEY`: Get a random key.
- `RENAME key newkey`: Rename a key.
- `RENAMENX key newkey`: Rename a key if the new key does not exist.
- `MOVE key db`: Move a key to another database.
- `DBSIZE`: Get the number of keys in the current database.
- `FLUSHDB`: Delete all keys in the current database.
- `FLUSHALL`: Delete all keys in all databases.

## Diagnostic Commands

- `PING`: Ping the server.
- `ECHO message`: Echo a message.
- `TIME`: Get the current server time.
