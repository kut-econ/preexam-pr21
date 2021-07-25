# プログラミング2021 期末試験対策問題

- [プログラミング2021 期末試験対策問題](#プログラミング2021-期末試験対策問題)
  - [第1回　プログラミング概論](#第1回プログラミング概論)
    - [課題2とよく似た問題を出題します](#課題2とよく似た問題を出題します)
  - [第2回 VS Code/仮想環境入門](#第2回-vs-code仮想環境入門)
    - [こちらの範囲からは出題しません](#こちらの範囲からは出題しません)
  - [第3回 バージョン管理入門](#第3回-バージョン管理入門)
    - [Q3-1](#q3-1)
    - [Q3-2](#q3-2)
    - [Q3-3](#q3-3)
    - [Q3-4](#q3-4)
  - [第4回 変数とメモリ](#第4回-変数とメモリ)
    - [Q4-1](#q4-1)
    - [Q4-2](#q4-2)
    - [Q4-3](#q4-3)
    - [Q4-4](#q4-4)
    - [Q4-5](#q4-5)
  - [第5回 データ型と制御構文](#第5回-データ型と制御構文)
    - [Q5-1](#q5-1)
    - [Q5-2](#q5-2)
    - [Q5-3](#q5-3)
    - [Q5-4](#q5-4)
    - [Q5-5](#q5-5)
    - [Q5-6](#q5-6)
    - [Q5-7](#q5-7)
    - [Q5-8](#q5-8)
    - [Q5-9](#q5-9)
    - [Q5-10](#q5-10)
    - [Q5-11](#q5-11)
    - [Q5-12](#q5-12)
  - [第6回 標準ライブラリ(1) – タプル、文字列、ファイル入出力](#第6回-標準ライブラリ1--タプル文字列ファイル入出力)
    - [Q6-1](#q6-1)
    - [Q6-2](#q6-2)
    - [Q6-3](#q6-3)
    - [Q6-4](#q6-4)
    - [Q6-5](#q6-5)
    - [Q6-6](#q6-6)
  - [第7回 標準ライブラリ(2) – 辞書、集合](#第7回-標準ライブラリ2--辞書集合)
    - [Q7-1](#q7-1)
    - [Q7-2](#q7-2)
    - [Q7-3](#q7-3)
    - [Q7-4](#q7-4)
    - [Q7-5](#q7-5)
    - [Q7-6](#q7-6)
  - [A 応用問題](#a-応用問題)
    - [QA-1](#qa-1)
    - [QA-2](#qa-2)

## 第1回　プログラミング概論

### 課題2とよく似た問題を出題します

## 第2回 VS Code/仮想環境入門

### こちらの範囲からは出題しません

## 第3回 バージョン管理入門

### Q3-1

ローカルリポジトリrepo内に存在するファイルcode.pyに編集を加えたあと、ステージングしたとします(まだコミットはしていません)。このステージングをキャンセルし、ステージングする前の状態に戻すためのコマンドとして正しいものを一つ選びなさい。

1. git reset --mixed HEAD^
2. git reset --mixed HEAD
3. git reset --hard HEAD^
4. git reset --soft HEAD^

### Q3-2

ローカルリポジトリrepo内で4つのコミットcommit0, commit1, commit2, commit3を行った直後、次のコマンドを続けて実行したとします。

```bash
git reset --soft HEAD^
git reset --hard HEAD^
```

このあと、作業エリアの状態として正しいものを一つ選びなさい。

1. commit0と同じ内容
2. commit1と同じ内容
3. commit2と同じ内容
4. commit3と同じ内容

### Q3-3

Github上のリモートリポジトリrepoは唯一のブランチmasterを持っているとします。これを自身のパソコン上にクローンしてローカルリポジトリrepoを作成したとします。ローカルのrepo内で次の一連のコマンドを実行したあと、リモートとローカルの状態として正しいものを一つ選びなさい。

```bash
git checkout -b new
git push -u origin new
git checkout master
git branch -d new
```

1. リモート、ローカルともにmasterブランチのみが存在
2. リモートはmasterのみ、ローカルはnewのみが存在
3. リモートはmasterのみ、ローカルはmasterとnewが存在
4. リモートはmasterとnew、ローカルはmasterのみが存在
5. リモート、ローカルともにmasterとnewが存在

### Q3-4

ローカルリポジトリrepo内で4つのコミットcommit0, commit1, commit2, commit3を行ったとする。次のようにrevertコマンドを2回連続で実行したあと、作業エリアの状態として正しいものを一つ選びなさい。

```bash
git revert HEAD
git revert HEAD
```

1. commit0と同じ内容
2. commit1と同じ内容
3. commit2と同じ内容
4. commit3と同じ内容

## 第4回 変数とメモリ

### Q4-1

次のRコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```R
x <- c(1,2,3)
y <- x
x[2] <- 8
y[1] <- 5
print(x)
```

1. `[1] 5 2 3`
2. `[1] 5 8 3`
3. `[1] 1 2 8`
4. `[1] 1 5 8`
5. `[1] 1 8 3`

### Q4-2

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,3]
y = x
x[1] = 5
print(y)
```

1. `[1,5,3] False`
2. `[5,2,3] False`
3. `[1,5,3] True`
4. `[5,2,3] True`

### Q4-3

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,3]
y = x
z = y[:]
y[:] = [4,5,6]
print(x,y,z)
```

1. `[4,5,6] [4,5,6] [4,5,6]`
2. `[1,2,3] [4,5,6] [4,5,6]`
3. `[4,5,6] [4,5,6] [1,2,3]`
4. `[1,2,3] [4,5,6] [1,2,3]`

### Q4-4

次のPythonコードを実行したあと、続けて実行したときにエラーが出ないコードを全て選びなさい。(部分点あり)

```python
x = "String"
```

1. `y = x[6]`
2. `x[0:2] = "st"`
3. `y = x[3:-1]`
4. `y = x + str(1)`
5. `x[2] = "R"`
6. `y = x * "2"`
7. `y = x[-3]`
8. `x = x + x`
9. `x = "Variable"`
10. `x[:] == x`

### Q4-5

次のRコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```R
library(pryr)
x <- c(1,2,3)
add <- address(x)
y <- x
z <- y
x[3] <- 4
print(c(address(x) == add, address(y) == add, address(z) == add))
```

1. `[1] TRUE FALSE FALSE`
2. `[1] TRUE TRUE TRUE`
3. `[1] FALSE FALSE FALSE`
4. `[1] FALSE TRUE TRUE`

## 第5回 データ型と制御構文

### Q5-1

次のPythonコードを実行した際に、変数xに格納されている値を整数値で答えなさい。ただしリストのオーバーヘッド(=`sys.getsizeof([])`の戻り値)を56バイトとし、処理系は64ビットとする。

```python
import sys
x = sys.getsizeof([[1,2,3],[“Py”,[“thon”]]])
```

### Q5-2

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,[3]]
y = x[:]
y[2] = 4
print(x,x is y)
```

1. `[1,2,[3]] False`
2. `[1,2,[4]] True`
3. `[1,2,[4]] False`
4. `[1,2,4] False`
5. `[1,2,4] True`

### Q5-3

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,[3]]
y = x[:]
y[2][:] = [4]
print(x,x is y)
```

1. `[1,2,[3]] False`
2. `[1,2,[4]] True`
3. `[1,2,[4]] False`
4. `[1,2,4] False`
5. `[1,2,4] True`

### Q5-4

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,[3]]
y = x[:]
y[:] = [4,5,y[2]]
y[2][0] = 6
print(x)
```

1. `[1,2,[3]]`
2. `[4,5,[3]]`
3. `[1,2,[6]]`
4. `[4,5,[6]]`

### Q5-5

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
import copy
x = [1,2,[3],’Python’]
y = copy.deepcopy(x)
print(x[2] is y[2],x[3] is y[3])
```

1. `True True`
2. `True False`
3. `False True`
4. `False False`

### Q5-6

次のPythonコードを実行した結果得られる出力を記述しなさい。解答例：`[[1],2,[3,4]]`

```python
x = [1,2,3]
x.append([4] + [5])
print(x)
```

### Q5-7

次のPythonコードを実行したあと、変数yにリスト[6,4,2]を代入するためのコードとして正しいものを一つ選びなさい。

```python
x = list(range(10))
```

1. `y = x[-3:-8:-2]`
2. `y = x[-4:1:-2]`
3. `y = x[2:7:-2]`
4. `y = x[7:2:-2]`

### Q5-8

次のPythonコードを実行した結果得られる出力を記述しなさい。解答例：`[[1],2,[3,4]]`

```python
x = [[1,2]*2]*2
x[0][2] = 3
print(x)
```

### Q5-9

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(20):
    if i % 2 == 0:
        x += 1
    elif i % 3 == 0:
        x -= 1
print(x)
```

### Q5-10

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(20):
    if i % 2 == 0:
        x += 1
    if i % 3 == 0:
        x -= 1
print(x)
```

### Q5-11

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(20):
    if i % 2 == 0:
        x += 1
        if i % 3 == 0:
            x -= 1
print(x)
```

### Q5-12

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(10):
    for j in range(i,10):
        x += 1
    x -=1
print(x)
```

## 第6回 標準ライブラリ(1) – タプル、文字列、ファイル入出力

### Q6-1

次のPythonコードを実行したところ、下記の出力が得られたとします。

```python
import sys
x = sys.getsizeof("a")
y = sys.getsizeof("あ")
print(x,y)
```

```python
#出力
50 76
```

このとき、次のコードを実行したときの出力を整数値で答えなさい。

```python
print(sys.getsizeof("abcあいう"))
```

### Q6-2

次のPythonコードを実行した際に得られる出力を文字列で答えなさい。解答例：`abCDefg`

```python
print("c".join("AbkBCebg".lower().split("b"))
```

### Q6-3

次のPythonコードを実行した際に得られる出力を文字列で答えなさい。解答例：`abCDefg`

```python
text = "eeeeeee"
print(text.replace("ee","a").replace("aa","e"))
```

### Q6-4

次のPythonコードを実行した結果出力として得られる文字列を答えなさい。解答例：`abCDefg`

```python
trans = {i:chr(i-1) for i in range(ord('b'),ord('e')+1)}
print("abcdef".translate(trans))
```

### Q6-5

次のうち、Pythonのタプルであるものを全て選びなさい。

1. `()`
2. `(100)`
3. `({})`
4. `(())`
5. `[()]`
6. `([],)`

### Q6-6

次のPythonコードを実行したとします。そのあと、ファイル`output.txt`をテキストエディタで開くと、どのような文字が書いてあるか、ひらがなで答えなさい。

```python
str_byte = bytes([0xe3,0x81,0x9b,0xe3,0x81,0x84,0xe3,0x81,0x8b,0xe3,0x81,0x84])
with open('./output.txt','bw') as file:
    file.write(str_byte)
```

ただし、ひらがなの`utf-8`エンコーディングは次で与えられます。

```bash
あいうえお --> e38182 e38184 e38186 e38188 e3818a 
かきくけこ --> e3818b e3818d e3818f e38191 e38193 
さしすせそ --> e38195 e38197 e38199 e3819b e3819d 
たちつてと --> e3819f e381a1 e381a4 e381a6 e381a8 
なにぬねの --> e381aa e381ab e381ac e381ad e381ae 
はひふへほ --> e381af e381b2 e381b5 e381b8 e381bb 
まみむめも --> e381be e381bf e38280 e38281 e38282 
や　ゆ　よ --> e38284 e38080 e38286 e38080 e38288 
らりるれろ --> e38289 e3828a e3828b e3828c e3828d 
わ　　　を --> e3828f e38080 e38080 e38080 e38292 
ん　　　　 --> e38293 e38080 e38080 e38080 e38080 
```

## 第7回 標準ライブラリ(2) – 辞書、集合

### Q7-1

Python辞書を作成するコードとして正しいものを全て選びなさい（部分点あり）。

1. `x = {'foo':1,'bar':2,'baz':3}`
2. `x = dict(foo=1,bar=2,baz=3)`
3. `x = dict((['foo',1],['bar',2],['baz',3]))`
4. `x = dict(zip(('foo','bar','baz'),range(1,4)))`
5. `x = dict.fromkeys(('foo','bar','baz'),0)`
6. `x = dict(zip(('foo','bar'),(1,2)),baz=3)`
7. `x = dict(foo=1,{'bar':2,'baz':3})`

### Q7-2

次のPythonコードを実行した際に得られる出力を整数値で答えなさい。ただし64ビット処理系を仮定する。

```python
import sys
x = dict()
for i in range(0,7):
    x[i] = i
overhead = sys.getsizeof(dict()) - 128
print(sys.getsizeof(x)-overhead)
```

### Q7-3

次のPythonコードを実行したとします。

```python
x = dict()
x['dog']='bowwow'
x['cat']='meow'
```

ただし、各文字列のハッシュ値は次の通りであるとします。

|文字列|ハッシュ値|
|--|--|
|'dog'|0x5b505070f40ff0be|
|'cat'|0x7f913288756f7978|
|'bowwow'|0x5f1fbec67091743e|
|'meow'|0x569f937d03758c22|

辞書`x`内部にあるインデックス配列の状態として正しいものを一つ選びなさい。

1. `1 -1 -1 -1 -1 0 -1`
2. `-1 -1 1 -1 -1 0 -1`
3. `6 0 -1 -1 -1 -1 -1`
4. `6 2 -1 -1 -1 -1 -1`

### Q7-4

次のPythonコードを実行したとします。

```python
x = {'dog','cat','horse'}
y = x.copy()
y.discard('dog')
z = x.copy()
z.add('rabbit')
```

次のうち、TrueになるものにはT、FalseになるものにはFと答えなさい。(部分点あり)

1. `z.issuperset(x)`
2. `x.issubset(y)`
3. `'dog' in (x - y)`
4. `'cat' in (z & y)`

### Q7-5

次のPythonコードのうち、エラーが出ずに実行できるものを全て選びなさい。（部分点あり）

1. `{range(5):3}`
2. `{1:[]}`
3. `{{''}}`
4. `{():{}}`
5. `{[]:''}`
6. `{([],)}`

### Q7-6

次のPythonコードを実行した際に出力される整数を書きなさい。

```python
print({i % 3:i for i in range(10)}[1])
```

## A 応用問題

### QA-1

次のPythonコードは100以下の素数を全て印字するプログラムです。(a)-(d)に当てはまるコードを1~4から選びなさい。

```python
for i in range(2,100):
    (a)______
    for j in range(2,i):
        (b)______
            (c)_____
            break
    (d)_____
        print(i)
```

1. `prime = False`
2. `if prime:`
3. `prime = True`
4. `if i % j == 0:`

### QA-2

次のPythonコードは、"This exam has too many questions."という文字列に含まれる各アルファベットの出現回数を印字するものである。

```python
string = 'This exam has too many questions.'
trans_rule = {' ':'','.':''}
trans = str.maketrans(trans_rule)
string_clean = string.lower().translate(trans)
for c in (a)________:
    print("{}/{}".format(c,(b)______.count(c)))
```

出力は次のようになります。

```bash
a/3
e/2
h/2
i/2
m/2
n/2
o/3
q/1
s/4
t/3
u/1
x/1
y/1
```

(a)-(b)に当てはまる正しいコードを次から選びなさい。

1. `list(string_clean).sort()`
2. `string_clean`
3. `sorted(string_clean)`
4. `sorted(set(string_clean))`
