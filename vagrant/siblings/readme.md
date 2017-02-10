This instance of Riak-KV comes with a sibling problem. Data can be read via
curl http://localhost:8098/riak/docs/foo
curl http://localhost:8098/riak/docs/bar
curl http://localhost:8098/riak/docs/baz
curl http://localhost:8098/riak/docs/qux
but all of these return a list of siblings rather than the most recent version of the data.

Locate the source of the problem and resolve the siblings.
