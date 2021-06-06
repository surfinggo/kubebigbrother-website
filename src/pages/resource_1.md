```yaml
apiVersion: spongeprojects.com/v1alpha1
kind: Watcher
metadata:
  name: configmaps
  namespace: demo
spec:
  channelNames:
  - print-to-stdout
  noticeWhenAdded: true
  noticeWhenDeleted: true
  noticeWhenUpdated: true
  resource: configmaps
---
apiVersion: spongeprojects.com/v1alpha1
kind: ClusterWatcher
metadata:
  name: namespaces
spec:
  channelNames:
  - print-to-stdout
  noticeWhenAdded: true
  noticeWhenDeleted: true
  noticeWhenUpdated: true
  resource: namespaces
```