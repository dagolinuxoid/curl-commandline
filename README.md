# How to create a new GitHub repo purely via command line.

`curl -u USER https://api.github.com/user/repos -d '{ "name": "REPO"}'`
Change only USER and REPO with your github username and the name of the repository.

So in my case, since USER=dagolinuxoid, REPO=curl-commandline I've prompted this:
`curl -u dagolinuxoid https://api.github.com/user/repos -d '{ "name": "curl-commandline"}'`
