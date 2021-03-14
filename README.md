# docker build on copr

This is the rpm spec for generating rpm and/or src.rpm to build [docker](https://www.docker.com/).
The resulting builds can be found on https://copr.fedorainfracloud.org/coprs/runlevel5/docker/.

## build it yourself

The `./Makefile` has a couple of convenience targets.
Notably:

```shell
make srpm
```

Will produce you a src.rpm, for use on your own copr, or build system, or even then:

```shell
rpmbuild --rebuild ...src.rpm
```

If you are building local, just:

```shell
make rpm
```

which builds through to the binary rpm.


## Major versions

This git repo, `main` will track my latest iteration on the build.
But as upstream docker have a release cycle for major version with breaking changes, there will be a corresponding branch.

## Prior versions

If you need a prior version than is found on the COPR repo, check out the [tagged releases](https://github.com/vbatts/copr-build-docker/releases).
(Whether downloading that source bundle or git checkout the tag)
