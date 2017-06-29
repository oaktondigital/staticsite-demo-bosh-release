#!/bin/bash

set -eu -o pipefail

cd bosh-release

bosh add-blob ${BLOB} ${BLOB}
bosh upload-blobs

git config --global user.name "CICD Robot"
git config --global user.email "cicd@oakton.digital"

git commit -am 'bump release blob'

cd ..

cp -a git-bosh-release-get pushme

echo "finished uploading a new source blob"
exit 0
