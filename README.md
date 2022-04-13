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

```bash
dvc repro
```

save the changes and commit to the git.

```bash
git add . && git commit -m "stage 2 complete" && git push origin main
```

Create "train_and_evaluate.py" file to train the model and evluate the metrics

Update "dvc.yaml" file to add stage 3 (i.e "train_and_evaluate")

run "dvc.yaml" to reproduce

```bash
dvc repro
```

save the changes and commit to the git.

```bash
git add . && git commit -m "stage 3 complete" && git push origin main
```

Run the following command to compares parameters currently present in the workspace (uncommitted changes) with the latest committed versions (required).

```bash
dvc params diff
```

Run the following command to see the metrics specified in dvc.yaml

````bash
dvc metrics show
````

Compare metrics between two commits in the DVC repository, or between a commit and the workspace

```bash
dvc metrics diff
```
Install pytest
```bash
pip install pytest
```

Create "tests" folder and "__init__.py", "conftest.py" and "test_config.py" files in it.

Write a simple test case in "test_config.py" file.

Create "tox.ini" file

Run with the following command

```bash
tox
```

for rebuilding
```bash
tox -r
```

pytest command
```bash
pytest -v
```

create a "setup.py" file to make the mentioned file as a package, so that we can make use of this package just by importing it.

Run the setup command

```bash
pip install -e .
```

To create ".tar" or distribution files [ Which helps to share the project] run the following command.

```bash
python setup.py sdist bdist_wheel
```

Update the changes and commit to the git.

```bash
git add . && git commit -m "setup done" && git push origin main
```
Write simple custom exception in "test_config.py" 

Update the changes and commit to the git.

Create a flask web app [including folders, files and all] and use "app.py" to run the application.

Update the changes and commit to the git.

 




