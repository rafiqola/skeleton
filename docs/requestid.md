# Implement Distributed Tracing (RequestID)

- Add requestid middleware to `dics/container.go`

```go
{
    Name:  "bima:middleware:requestid",
    Build: (*middlewares.RequestID)(nil),
    Params: dingo.Params{
        "RequestIDHeader": "X-Request-Id",
    },
}
```

- Add to `configs/middlewares.yaml`

```yaml
middlewares:
    - requestid
```

RequestID added to your response header

