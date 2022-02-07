# Proglog - Distributed Logger in Go

## Start the HTTP server

```bash
git clone git@github.com:ton3s/proglog.git
cd proglog/cmd/server
go run .
```

## Test server

```bash
# Save a record to the log
curl -X POST localhost:8080 -d '{"record": {"value": "TGV0J3MgR28gIzEK"}}'

# Expected output
{
  "offset": 0
}

# Retrieve the record from the log
curl -X GET localhost:8080 -d '{"offset": 0}'

# Expected output
{
  "record": {
    "value": "TGV0J3MgR28gIzEK",
    "offset": 0
  }
}
```
