Callback:

```yaml
apiVersion: spongeprojects.com/v1alpha1
kind: Channel
metadata:
  name: my-callback
spec:
  type: callback
  callback:
    url: "http://my-service.com/api/callback"
```

Print:

```yaml
apiVersion: spongeprojects.com/v1alpha1
kind: Channel
metadata:
  name: print-to-stdout
spec:
  type: print
  print:
    writer: stdout
```