# Base tree

This repository includes two external repositories as subtrees.

```
subtree-base/
├── test/
│   └── subtree-sub/             # Git subtree (external repo)
└── doc/
    └── subtree-base.wiki/       # Git subtree (external wiki repo)
```

The commands below set up `subtree-sub` as a subtree.

```
git remote add subrepo https://github.com/Nakakiyo092/subtree-sub
git fetch
git subtree add --prefix=test subrepo main --squash
```

The commands below sync changes between the base and the sub.

```
git subtree push --prefix=test subrepo main
git subtree pull --prefix=test subrepo main --squash
```

