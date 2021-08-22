## 適当なフォルダにhook名に対応するシェルスクリプトを作る

```
cat githooks/pre-commit
#!/bin/sh

echo 'pre-commit!!!'
```

## そのフォルダを `core.hooksPath` に設定する

```
git config --local core.hooksPath githooks
```


## するとそれぞれのタイミングでhookスクリプトが呼ばれる

```
% git commit -m "commit test"
pre-commit!!!
[main f78a94c] commit test
 1 file changed, 1 insertion(+)
```