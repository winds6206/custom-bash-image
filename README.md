# custom-bash 映像檔

已安裝 tzdata/curl 套件，帶入環境變數 `TZ=Asia/Taipei` 可修正時區

## 使用方式

K8s YAML 增加環境變數

```
apiVersion: apps/v1
kind: Deployment
metadata:
...
spec:
  template:
    metadata:
      ...
    spec:
      restartPolicy: Always
      containers:
        ...
          env:
            - name: TZ
              value: Asia/Taipei
```
