# GQ-GISTQUERY (gq)

gq is a utility to query a single user's GitHub gists

## Syntax

`gq <username>`

Where `<username>` is the Github user's username.

The first time you query a user's gist it will register the current
gists for that user and show the date of the latest gist. The user
will be registered in a file named `/tmp/gq.<username>`. Subsequent
executions for the same username will tell you if a new gist has been added by the user.

To reset an individual query, delete `/tmp/gq.<username>`.
To reset all queries, delete `/tmp/gq.*`

## Requirements

* Python 2.7 or higher
* Apply requirements.txt with pip

## Exit codes

* User not found: 255
* User has not published any gists: 1
* Success (first or subsequent queries): 0

## License

GNU General Public License v3.0
