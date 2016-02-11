# Setting an Environment Variable in a Piped Command
If you want to set an environment variable for one command, you can do this:

```PGPASSWORD=foo psql -U $user -d $db -h $host```

Before today, I hadn't realize that this also works within pipes:

```echo "select count(*) from foo;" | PGPASSWORD=foo psql -U $user -d $db -h $host```

And if you need it to apply to _more than one_ command within the pipe, you can do this:

```echo "select count(*) from foo;" | (export PGPASSWORD=foo psql -U $user -d $db -h $host | other_command) | grep...```

(assuming you've already exported `user`, `db`, and `host` from the parent shell).
