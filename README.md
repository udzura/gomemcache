## About

This is a memcache client library for the Go programming language
(http://golang.org/).

## Forked version

We add some features to this library, in order to fit to our use case.

* Support option function pattern
* Delete old connections preriodically

We plan to send patches to original someday.

## Installing

### Using *go get*

    $ go get github.com/bradfitz/gomemcache/memcache

After this command *gomemcache* is ready to use. Its source will be in:

    $GOPATH/src/github.com/bradfitz/gomemcache/memcache

## Example

    import (
            "github.com/bradfitz/gomemcache/memcache"
    )

    func main() {
         mc := memcache.New("10.0.0.1:11211", "10.0.0.2:11211", "10.0.0.3:11212")
         mc.Set(&memcache.Item{Key: "foo", Value: []byte("my value")})

         it, err := mc.Get("foo")
         ...
    }

## Full docs, see:

See https://pkg.go.dev/github.com/bradfitz/gomemcache/memcache

Or run:

    $ godoc github.com/bradfitz/gomemcache/memcache

