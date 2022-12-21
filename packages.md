# Performance and Disk Efficiency
- NPM: when compared with yarn & PNPM. npm is bit slower

- Yarn uses the same flatten node_modules directory but is comparable to NPM in regards to speed and installs packages parallely.

- PNPM: PNPM is 3 times faster and more efficient than NPM.  With both cold and hot cache, PNPM is faster than Yarn.Pnpm simply links files from the global store, while yarn copies files from its cache. Package versions are never saved more than once on a disk. The algorithm of pnpm does not use a flatten dependency tree, which makes it easier to implement, maintain, and requires less computation

### Flattened Dependency Tree
![alt text](flattened.png)