# EthereumJS Monorepo Fork

This is a fork of the [ethereumjs monorepo](https://github.com/ethereumjs/ethereumjs-monorepo) used to temporarily publish our own versions under the `@nomicfoundation` npm org.

We are doing this to publish a version of Hardhat that uses the first RC version of the new ethereumjs v6 packages that won't break if there are breaking changes in subsequent RC versions or in the final stable version.

### Why not use a fixed version of these dependencies?

We could use a fixed version of each ethereumjs package instead. For example, we could do `"@ethereumjs/vm": "6.0.0-rc.1"` instead of `^6.0.0-rc.1`. The problem is that the `@ethereumjs/vm` package, in turn, has a `^` dependency in other ethereumjs packages. If those are bumped, and there are breaking changes, a user that upgrades their dependency could run into an error anyway. Since this has happened in the past, we are (temporarily) using a forked, fixed version of the ethereumjs packages to completely prevent that possibility.
