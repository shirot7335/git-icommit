# git-icommit

## Description
Rough initial commit setup tool.

## Install

```
make
    install      install git-icommit on PREFIX directory.
    uninstall    uninstall git-icommit from PREFIX directory.
```

## Usage

```
Usage: git-icommit [OPTION]...
Create an empty Git repository and empty commit.

[OPTION]
    -m <msg>               Use the given <msg> as the INITIAL commit message.
    -r                     Set remote repository. (github only)
    -p                     Push main branch to github. (Basically, use it with the -r option.)
    -a <access_type>       Use the given <access_type> for remote repository access. ('ssh' or 'https')
    -n <repository_name>   Use the given <repository_name> when setting up a remote repository.
    -o <repository_owner>  Use the given <repository_owner> when setting up a remote repository.
    -s                     Display DEFAULT settings and exit.
    -h                     Display this help and exit.

```

## Example

```
$ git icommit -s

{
  "branch": {
    "origin": "main"
  },
  "commit": {
    "message": "initial commit"
  },
  "remote_repository": {
    "owner": "mochisuki",
    "name": "test",
    "type": "github",
    "access": "ssh"
  }
}
```

```
# Set up a remote repository and push it over https to github.
# The first commit message is "first commit".
$ git icommit -m "first commit" -r -p -a 'https'
```
