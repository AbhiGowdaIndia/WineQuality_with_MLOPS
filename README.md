create env

```bash
conda create -n WineQuality_With_MLOPS python=3.7 -y
```

activate env 

```bash
conda activate WineQuality_With_MLOPS
```

Create Requirements file
install the requirements 

```bash
pip install -r requirements.txt
```

download the data from

```bash
https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5
```

Initiate git

```bash
git init
```

initiate dvc

```bash
dvc init
```

add data (to dvc to track the data)

```bash
dvc add data_given/winequality.csv
```

add all the things in the current directry to git staging area.

```bash
git add .
```

Commit git

```bash
git  commit -m "First commit"
```

One liner git update for README.md
```bash
git add . && git commit -M "Updated README.md"
```

pushing an existing repository from the command line

```bash
git remote add origin https://github.com/AbhiGowdaIndia/WineQuality_with_MLOPS.git
git branch -M main
git push origin main
```

add parameters and update it to the git
```bash
git add . && git commit -m "Parameters added"
git push origin main
```

add "get_data.py" file to read and process parameters and return dataframe.

add "load_data.py" file to read data from source and save it in data/raw directory.

write "dvc.yaml" file to state stage (i.e "load_data")

run "dvc.yaml" to reproduce

```bash
dvc repro
```
save the changes and commit to the git.

```bash
git add . && git commit -m "stage 1 complete" && git push origin main
```

Create "split_data.py" file to split the data into train and test datasets

Update "dvc.yaml" file to add stage 2 (i.e "split_data")

run "dvc.yaml" to reproduce

save the changes and commit to the git.

```bash
git add . && git commit -m "stage 1 complete" && git push origin main
```





