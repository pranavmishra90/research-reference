---
title: "Steps to creating a remotes on GitHub and GIN, using GIN as the common data source"
date: last-modified
date-format: full
author:
  - name: Pranav Mishra
    url: https://drpranavmishra.com
    orcid: 0000-0001-5219-6269 
    affiliation: Rush University
    affiliation-url: https://rushu.rush.edu 
citation: true
google-scholar: true

---



````sh
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

````