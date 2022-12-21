# 1. Performance and Disk Efficiency
- NPM: when compared with yarn & PNPM. npm is bit slower

- Yarn uses the same flatten node_modules directory but is comparable to NPM in regards to speed and installs packages parallely.

- PNPM: PNPM is 3 times faster and more efficient than NPM.  With both cold and hot cache, PNPM is faster than Yarn.Pnpm simply links files from the global store, while yarn copies files from its cache. Package versions are never saved more than once on a disk. The algorithm of pnpm does not use a flatten dependency tree, which makes it easier to implement, maintain, and requires less computation

### Flattened Dependency Tree
![alt text](flattened.png)

- With hardlinks and symlinks, PNPM solved the issue above in contrast to NPM. PNPM grouped all dependencies by symlink, but retained all the dependencies.
![alt text](symlink.png)


# 2. Security
- NPM: There have been some security vulnerabilities that have directly affected many projects due to the way npm handles bad packages.

- YARN: Checksums stored in yarn.lock have been used by Yarn Classic and Yarn Berry ever since. Yarn also prevents you from installing malicious packages; if a mismatch is detected, the installation will be aborted.

- PNPM: Similar to Yarn, PNPM also uses checksums and in addition to the use of checksums, pnpm also verifies the integrity of its code before executing it.


# 3. Monorepo support

- NPM: The NPM package manager offers monorepo support with a variety of CLI commands to manage the multiple packages. However, unlike other package managers, it does not support advanced filtering or multiple workspaces.

- YARN: It also offers monorepo support as the feature workspaces. Using Lerna, a third-party application, before workspace feature was available, was the only way to use the package manager in a multi-package project.

- PNPM: NPM's doppelgangers problem can only be solved with PNPM. Monorepos are sometimes plagued with doppelgangers, so PNPM has an advantage in this regard.