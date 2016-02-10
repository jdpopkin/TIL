# Specifying Password in a Script
`psql` will use the `PGPASSWORD` environment variable as a password if it is set. This makes it easy to run psql with a password in a script: `PGPASSWORD=foo psql -U somebody -d something -h somewhere`

This isn't ideal from a security perspective, though, since other users might be able to see your process's environment variables.
