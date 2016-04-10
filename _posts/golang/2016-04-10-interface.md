---
layout: post
title:  "Interface"
tags: golang
---

- 하나의 인터페이스는 보통 하나의 method를 가진다
- __interface embedding__

```go
type ReadCloser interface {
    Reader
    Closer
}
```
- type이 interface의 요구 method 가진다 = a type __satisfy__ an interface
- __empty interface__ 는 어떤 method도 없이 비어있다. 대신 어떤 type도 assign 될 수 있다. (가변 변수 등에 사용)

```go
  type any interface{}
  var x any
  x = true
  x = 1
  fmt.Printf(...interface{})
```
- 값에 변경이 발생하는 동작의 interface에는 pointer 형태의 type이 연결되는 경우가 많다 (_golang에서 pointer에 대해서 더 파악 필요_)
