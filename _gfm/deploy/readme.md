# Datalad with GitHub and GIN siblings
Pranav Kumar Mishra
Wednesday, October 11, 2023

``` sh
datalad create-sibling-gin --access-protocol https-ssh \
  --credential gin@g-node.org \
  -r research-reference \
  --dry-run

datalad create-sibling-github -s github --credential github_pm90_sibling -r research-reference --dry-run

dd if=/dev/zero of=binary.dat bs=1c count=1

git config --unset-all remote.gin.annex-ignore

datalad push --to gin

datalad siblings configure --name gin --as-common-datasrc gin-src

datalad push --to gin
```
