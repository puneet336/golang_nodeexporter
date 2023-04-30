# golang_nodeexporter
setup for golang to create a node exporter

1. Install golang and extract

1. set PATH variable

1. download the required prometheus libraries as - 

```
[puneet@server]~/27042023/nodeexporters/lsfnodeexporter>go get github.com/prometheus/client_golang/prometheus
go: go.mod file not found in current directory or any parent directory.
        'go get' is no longer supported outside a module.
        To build and install a command, use 'go install' with a version,
        like 'go install example.com/cmd@latest'
        For more information, see https://golang.org/doc/go-get-install-deprecation
        or run 'go help get' or 'go help install'.
```

> NOTE1: here, fix is to run go env and check GO111MODULE , in my case setting was GO111MODULE="". so i set that to go env -w GO111MODULE=auto
> NOTE2: after setting GO111MODULE to auto i got :
```
# github.com/prometheus/common/expfmt
../../../go/src/github.com/prometheus/common/expfmt/decode.go:89:38: cannot use v (variable of type *io_prometheus_client.MetricFamily) as protoreflect.ProtoMessage value in argument to pbutil.ReadDelimited: *io_prometheus_client.MetricFamily does not implement protoreflect.ProtoMessage (missing method ProtoReflect)
../../../go/src/github.com/prometheus/common/expfmt/encode.go:120:40: cannot use v (variable of type *io_prometheus_client.MetricFamily) as protoreflect.ProtoMessage value in argument to pbutil.WriteDelimited: *io_prometheus_client.MetricFamily does not implement protoreflect.ProtoMessage (missing method ProtoReflect)
```
then i tried golang 1.19.8 version




