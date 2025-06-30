# ducklake-api

## Usage

### Example only

As an example only (creates local, unsecured Postgres):
```sh
./example.sh
```

### General

Create `.env` based on `.env.example`

```sh
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

#### Flask

```sh
python app.py
```


#### Gunicorn

```sh
gunicorn app:app --workers 4 --threads 2 --bind 0.0.0.0:8000
```