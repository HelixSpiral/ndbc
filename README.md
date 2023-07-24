NDBC - National Data Buoy Center
---

This is a simple Golang wrapper for parsing data from the [NDBC](https://www.ndbc.noaa.gov/).

There weren't any packages that I could find that performed the functions I needed, so I wrote this one. Woefully incomplete in it's current state but PRs are welcome.

I do intend to fully flesh this out at some point in the future, but for now it solves the immediate problem I had.

# Usage

Craete a new wrapper
```go
n := ndbc.NewAPI()
```

Call any of the exported functions
```go
resp, err := n.GetPictureFromBuoy(44027)
if err != nil {
    panic(err)
}

log.Println(resp)

resp2, err := n.GetLatestDataFromBuoy(44027)
if err != nil {
    panic(err)
}

log.Println(resp2)
```