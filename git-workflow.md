## git init 

```sh
git init 
```

### github cli 

```sh 
gh auth login
gh repo clone <url> 
cp <photo> . 
git add .
git commit --amend --no-edit 
git push origin main --force 
```

## git-workflow for feature-branch1 

```sh 
mkdir feature-branch1
git branch feature-branch1
git push origin feature-branch1 --force 
touch feature-branch1/fbranch1.txt 
touch feature-branch1/fbranch2.txt 
touch feature-branch1/fbranch3.txt 
git add .
git commit -m "feature branch 1"
git push origin feature-branch1 --force
```


## git-workflow for feature-branch2 

```sh
git checkout main
mkdir feature-branch2
git checkout -b feature-branch2
git push origin feature-branch2 --force
touch feature-branch1/fbranch1.txt
touch feature-branch1/fbranch2.txt
touch feature-branch1/fbranch3.txt
git add .
git commit -m "feature branch 2"
git push origin feature-branch2 --force
```

## git merge from feature-branch2 to main 

```sh 
git checkout main
git merge feature-branch2
git push origin main
mkdir feature-branch2-merge
touch feature-branch2-merge/fbranch_merge1.txt
touch feature-branch2-merge/fbranch_merge2.txt
touch feature-branch2-merge/fbranch_merge3.txt
git add . 
git commit -m "feature branch 2 update merge"
git push origin main 
```

## create the production branch 
```sh
git checkout -b production 
git merge main 
git tag 1.2.0
git push origin --tags
```

## update the feature branch1 for production 

```sh 
git merge main
git push origin feature-branch1
mkdir feature-branch1-merge
touch feature-branch1-merge/fbranch_merge1.txt
touch feature-branch1-merge/fbranch_merge2.txt
touch feature-branch1-merge/fbranch_merge3.txt
git add . 
git commit -m "feature branch 1 update merge" 
git push origin feature-branch1
```

## merge prodution from feature-branch1 

```sh
git merge feature-branch1
git push origin production 
git tag 1.3.0
git push origin --tags
```






