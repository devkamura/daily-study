# いい加減覚えよう。 `command > /dev/null 2>&1`の意味

参照：https://qiita.com/ritukiii/items/b3d91e97b71ecd41d4ea

### 問題 1

```
$ ./echo_1.sh
> これは標準出力を標準エラー出力として表示します
```

### 問題 2

```
$ ./echo_1.sh > result.txt
これは標準出力を標準エラー出力として表示します
$ cat result.txt
$
```

```
$ ./echo_1.sh 2>result.txt
$ cat result.txt
これは標準出力を標準エラー出力として表示します
```

#### 最終問題

```
$ ./echo_2.sh 1>normal.txt 2>error.txt
$ cat normal.txt
これは標準出力です
$ cat error.txt
これは標準出力を標準エラー出力として表示します
```
