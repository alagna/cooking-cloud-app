## nginx-deployment
```
          volumeMounts:
            - mountPath: /opt/bitnami/nginx/html/
              name: nginx-docs
      volumes:
        - name: nginx-docs
          configMap:
            name: nginx-docs-cm
```


## nginx-docs-cm
```
  index.html:  <h2>Welcome from NGINX in the {{ .Values.global.env }} environment</h2>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome</title>
    <link rel="icon" href="./favicon.ico" type="image/x-icon">
  </head>
  <body>
    <main>
        <h1>Welcome to My Website</h1>
    </main>
  </body>
</html>

```

