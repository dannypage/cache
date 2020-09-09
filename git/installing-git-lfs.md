# Installing Git LFS (Large File System)
## Aka the only way to get 50mb files onto Github (why)

### Ubuntu install

```
sudo apt-get install git-lfs
git lfs install
git lfs track '*.csv' 
git add . 
git commit -m "Adding CSV files to LFS"
git lfs push --all origin master
git push -u origin master
```

### Sources
General advice: https://towardsdatascience.com/uploading-large-files-to-github-dbef518fa1a

When I messed up and Github got angry about a commit: https://stackoverflow.com/a/54846502
