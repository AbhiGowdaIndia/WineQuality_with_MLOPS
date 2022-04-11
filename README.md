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