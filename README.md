# Test

update

update from the base repo

```
git remote add subrepo https://github.com/Nakakiyo092/subtree-sub
git fetch
git subtree add --prefix test --squash subrepo main
git subtree push --prefix test subrepo main
git subtree pull --squash --prefix test subrepo main
```

