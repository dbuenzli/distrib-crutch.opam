opam distribution crutch 
========================

An opam repository with a few packages that your distribution may be
missing.

To add it to your opam repos and swiches do:

```
opam repo add --all --set-default distrib-crutch \
          git+https://github.com/dbuenzli/distrib-crutch.opam.git
```

The packages can be listed with:
   
```
opam update distrib-crutch
opam list -a --repo=distrib-crutch
```

Note that some of the packages here install the [`conf-c-env`] package
which tweaks environment variables to look for C libraries in your
opam switch prefix.

[`conf-c-env`]: packages/conf-c-env/conf-c-env.1/opam

## Purpose and limitations

It is not the aim of this repo to supplant your system packager.  In
general it is a better idea to try to help your distribution to work
towards inclusion of the dependencies you need as this take time to
stabilize.

Packages from this repository may be removed once
<https://repology.org/> indicates good support for a given package.

## Packaging

In general we try to follow how the `opam` depexts would end up 
being named for [`debian`](https://wiki.debian.org/Packaging)
which is often `$(PKG)-dev`. 

Otherwise see [this example]. In particular include a 
`x-distrib-status` with a link on the package's status on 
<https://repology.org/>.

[this example]: packages/libblake3-dev/libblake3-dev.1.5.1/opam

## License

All the metadata contained in this repository is licensed under the
[CC0-1.0](LICENSE.md) license
