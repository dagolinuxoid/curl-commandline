# How to create/delete a new/existing GitHub repo purely via command line using github API. 
— TO CREATE

`curl -u USER https://api.github.com/user/repos -d '{ "name": "REPO"}'`
Change only USER and REPO with your github username and the name of the repository.

So in my case, since USER=dagolinuxoid, REPO=curl-commandline I've prompted this:
`curl -u dagolinuxoid https://api.github.com/user/repos -d '{ "name": "curl-commandline"}'`


— TO DELETE

:username = your username(github handler) :repo = a name of a repo you want to get rid of
`curl -u :username -X "DELETE" https://api.github.com/repos/:username/:repo`
BTW you can create a simple script such as killrepo 
```
#!/bin/bash
REPO=$1
echo "do you REALLY wan to DELETE your GitHub $REPO ?"
curl -u dagolinuxoid -X 'DELETE' https://api.github.com/repos/dagolinuxoid/$REPO
```
