# db.sh
Key value file parsed in bash.

Using bash, you can easily manage key value pairs inside of a file.

It's this simple:

```bash
source db.sh

db.connect "my.db"
db.set key "value"
let someval=$(db.get key)

db.save
```

The db files look like this:

```
key value
hi hello
username jack
password sup3rs3cur3
```
