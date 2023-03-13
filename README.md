# db.sh

`db.sh` allows you to easily manage key value pairs inside of a file.

## Example

Script file:
```bash
source ../db.sh

function main ()
{
    # Start off with connecting.
    db.connect "mydb.db"

    echo "Database before saving:"
    db.visualize_db
    echo

    # Get something
    local let username=$(db.get username)

    # Set something
    db.set username "carl"

    # Finally, save it.
    db.save

    echo "Database after saving:"
    db.visualize_db
}

main
exit 0
```

DB file:
```
password username
username joe
```

Output:
```
Database before saving:
password : username
username : joe

Database after saving:
password : username
username : carl
```
