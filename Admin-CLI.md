While you are able to manage user accounts through raw HTTP requests (Admin APIs), it's bit bothering to make raw HTTP requests by `curl` command or some library. That's where akashic-admin CLI comes in handy.

The akashic-admin CLI is entirely written in Go and has the following sub commands:

* config - Make a config file under HOME directory
* add - Add a user
* get \<userId\> - Get a user
* list - List users
* update \<userId\> \<flags...\> - Update a user's attributes

**Installation**

```
$ cd admin-cli
$ make
# make install
```

Note that Golang compiler is prerequisite and the actual binaries are installed at `/usr/local/bin`. To uninstall, just do `make clean`.