dataserv-client-falsy
=====================



Summary
-------

This simple tool emulates the communication of Storj's `dataserv-client` to announce an arbitrary client Shard height.

You can announce an arbitrary Shard height without consuming any disk spaces.



Install
-------

You should install and setup `dataserv-client` before running `dataserv-client-falsy`.

For installations of `dataserv-client`, read the original documentations ([DriveShare official web](http://driveshare.org/dataserv.html), [GitHub repo](https://github.com/Storj/dataserv-client)).



Running
-------

Run
```bash
$ ./dataserv-client-falsy MAX_HEIGHT [CURRENT_HEIGHT]
```
where `MAX_HEIGHT` is the maximum number of Shards (a.k.a. Shard height) you want to announce,
and the second argument `CURRENT_HEIGHT` is the starting Shard height.

If you omit `CURRENT_HEIGHT`, `dataserv-client-falsy` will query to the `dataserv` server
to fetch the currently announced height for the current user.



Motivation
----------

I have warned the Storj team members and communities repeatedly that one can announce arbitrary Shard height
by simple hacking, since there are no data auditing mechanism in both server and client code.

As is mentioned in [Storj's original white paper](http://storj.io/storj.pdf) in Chap.3 *Proof-of-Storage*,
auditing data stored in server (farmer) nodes is a key feature for trustless P2P cloud storage services.

So I created this tool in order to raise warnings to the Storj users that `dataserv-client` is totally not of use
unless the auditing mechanism described in the Storj's original white paper is implemented.



Disclaimer
----------

This tool is for experimenting or testing only.

I do not take any responsibilities if your account or funds are banned or freezed by using this tool.



Authors
-------

 * Vis Virial &lt;visvirial-at-gmail.com&gt; (Twitter: [@visvirial](https://twitter.com/visvirial))



