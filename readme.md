# postgresql & fastapi

## installation
(Use uv if that's your relevant tech)
* `$ pip install "fastapi[standard]"`
* `$ pip install "psycopg[binary]"`
* `$ pip install "psycopg[pool]"`

# Run App
* `$ fastpi dev main.py`

## Storing data - philosophy

* What's the purpose of our data?
  * Bulk uploading
  * JSON data storage
  * Unorganized data
  * PostgreSQL database
* What's the datatype of said data?
  * Unorganized 
  * unstructured
  * Json

## Database - PostgreSQL
A newly created database does NOT contain any TABLES by default.

Step #1 - Create new Table (products)
```postgresql
CREATE TABLE IF NOT EXISTS products_raw (
id BIGSERIAL PRIMARY KEY,
created_at TIMESTAMPTZ NOT NULL DEFAULT now(),
product JSONB NOT NULL
);
```

Step #2 - Implement function for Insert (fastAPI)

## TODO : Difference between: uvicorn vs fastapi dev main.py 