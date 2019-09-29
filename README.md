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

# travis-lab for Continuous Intergreation
Once a change is committed to your repository, this will result in the trigger of a new run of your job on Travis CI. 
On the page https://travis-ci.org/lambodoug/travis-lab, click Build History. You may see your build in progress.

[![Build status](https://travis-ci.org/lambodoug/travis-lab.svg?master)](https://travis-ci.org/lambodoug)

## Requirements

* Python 3.0 or higher
* Apply requirements.txt with pip

## Exit codes

* User not found: 255
* User has not published any gists: 1
* Success (first or subsequent queries): 0

## License

GNU General Public License v3.0
