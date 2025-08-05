# ducklake-api

A simple HTTP server implementation for querying a DuckLake with DuckDB

## Usage

### Example only

As an example only (creates local, unsecured datastore and Postgres catalog):
```sh
./example.sh
```

### General setup

Create `.env` based on `.env.example`

```sh
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### Flask server

```sh
python app.py
```


### Gunicorn server

```sh
gunicorn app:app --workers 4 --threads 2 --bind 0.0.0.0:8000
```

### Query

`POST` to `http://localhost:8000/query` with payload: `{"sql": "your-query"}` and header: `X-API-Key` set to `your-secret-key`