= dependencies =
  * tuf         <- for the client
  * tuf[tools]  <- for the repo


= How to use it =
# create a repo and it's keys
  $ ./tuf create
# add something to the repo and update the targets
  $ echo "test" > repo/targets/foo
  $ ./tuf targets
# create a client
  $ ./tuf setup-client
# run a web server to distribute the repo
  $ cd repo; python -m SimpleHTTPServer 8001
# update your client
  $ ./tuf update
