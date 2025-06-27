## How to add large file to git repo
The model file is too large for regular git repo. One need to use git lfs (git large file system) to store.
```
brew install git-lfs

git lfs install

git lfs track "models/diffusion_pytorch_model.bin"

git add models/diffusion_pytorch_model.bin

git commit -m "Add large file tracked by Git LFS"

git push origin main

git lfs ls-files
```

## How to checkout the repo with lfs
```
git clone git@github.com:penguin12b5/encode_decode.git
```
if the large file doesn't show up, try:
```
git lfs pull
```

