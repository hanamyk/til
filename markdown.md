# Block Elements

## Headers 見出し

先頭に`#`をレベルの数だけ記述します。  
またh1とh2だけ別の記述方法があり、文章の改行後にイコール`==`を2つ以上記述するとh1に、マイナス`--`を2つ以上記述するとh2になります。  
```
# h1
## h2
### h3
#### h4
##### h5
###### h6
h1
==
h2
--
```

# h1
## h2
### h3
#### h4
##### h5
###### h6
h1
==
h2
--

## Block 段落

空白行を挟むことで段落となります。

```
段落1
(空行)
段落2
```

段落1

段落2

## Br 改行

改行の前に半角スペース`  `を2つ記述します。

```
hoge
fuga(スペース2つ)
piyo
```

hoge
fuga  
piyo

## Blockquotes 引用

先頭に`>`を記述します。ネストは`>`を多重に記述します。

```
> 引用  
> 引用
>> 多重引用
```

> 引用  
> 引用
>> 多重引用

## Code Block コードブロック

バッククオート` ``` `３つ、あるいは チルダ` ~~~ `３つで囲みます。

~~~
```
print 'hoge'
```
~~~
```
print 'hoge'
```

### シンタックスハイライト

コードブロック記法のあとに言語名を指定してください。

~~~ 
```php
class Sample()
{
	private int $a;
	
	public function __construct(int $a)
	{
		$this->a = $a;
	}
	
	public function hoge(int $x, int $y):int
	{
		return ($x + $y) * $this->a;
	}
}
```
~~~

```php
class Sample()
{
	private int $a;
	
	public function __construct(int $a)
	{
		$this->a = $a;
	}
	
	public function hoge(int $x, int $y):int
	{
		return ($x + $y) * $this->a;
	}
}
```

### インラインコード

バッククオート `` ` ``で単語を囲むとインラインコードになります。

```
これは `インラインコード`です。
```

これは `インラインコード`です。

## pre 整形済みテキスト

半角スペース4個もしくはタブで、コードブロックをpre表示できます

```
    class Hoge
        def hoge
            print 'hoge'
        end
    end
```

    class Hoge
        def hoge
            print 'hoge'
        end
    end

## Hr 水平線

アンダースコア`_` 、アスタリスク`*`、ハイフン`-`などを3つ以上連続して記述します。

```
hoge
***
hoge
___
hoge
---
```

hoge
***
hoge
___
hoge
---

# Lists

## Ul 箇条書きリスト

ハイフン`-`、プラス`+`、アスタリスク`*`のいずれかを先頭に記述します。  
ネストはタブで表現します。

```
- リスト1
    - リスト1_1
        - リスト1_1_1
        - リスト1_1_2
    - リスト1_2
- リスト2
- リスト3
```

- リスト1
    - リスト1_1
        - リスト1_1_1
        - リスト1_1_2
    - リスト1_2
- リスト2
- リスト3

## Ol 番号付きリスト

`番号.`を先頭に記述します。ネストはタブで表現します。  
番号は自動的に採番されるため、すべての行を1.と記述するのがお勧めです。

```
1. 番号付きリスト1
    1. 番号付きリスト1-1
    1. 番号付きリスト1-2
1. 番号付きリスト2
1. 番号付きリスト3
```

1. 番号付きリスト1
    1. 番号付きリスト1-1
    1. 番号付きリスト1-2
1. 番号付きリスト2
1. 番号付きリスト3

# Inline Elements

## Link リンク

`[表示文字](URL)`でリンクに変換されます。

```
[Google](https://www.google.co.jp/)
```

[Google](https://www.google.co.jp/)

### 外部参照リンク

URLが長くて読みづらくなる場合や同じリンクを何度も使用する場合は、リンク先への参照を定義できます。

```
[Googleを見る][Google]
[Google]: http://www.yahoo.co.jp
```

[Googleを見る][Google]  
[Google]: http://www.yahoo.co.jp

## 強調
### em

アスタリスク`*`もしくはアンダースコア`_`1個で文字列を囲みます。

```
これは *イタリック* です
これは _イタリック_ です
```

これは *イタリック* です  
これは _イタリック_ です

### strong

アスタリスク`*`もしくはアンダースコア`_`2個で文字列を囲みます。

```
これは **ボールド** です
これは __ボールド__ です
```

これは **ボールド** です  
これは __ボールド__ です

### em + strong

アスタリスク`*`もしくはアンダースコア`_`3個で文字列を囲みます。

```
これは ***イタリック＆ボールド*** です
これは ___イタリック＆ボールド___ です
```

これは ***イタリック＆ボールド*** です  
これは ___イタリック＆ボールド___ です

### 取り消し線
チルダ`~~`2個で文字列を囲むことで取り消し線を利用できます。  
```
~~取り消し線~~
```
~~取り消し線~~

## Images 画像

先頭の`!`で画像の<img>と認識されます。画像の大きさなどの指定をする場合はimgタグを使用します。

```
![alt](画像URL)
![代替文字列](URL "タイトル")

<img src="attach:cat.jpg" alt="attach:cat" title="attach:cat" width="200" height="200">
```
![hed.gif](hed.gif)


# Table 表

`-`と`|`を使ってtableを作成します。

```
| TH1 | TH2 |
----|---- 
| TD1 | TD3 |
| TD2 | TD4 |
```

| TH1 | TH2 |
----|---- 
| TD1 | TD3 |
| TD2 | TD4 |

```
| 左揃え | 中央揃え | 右揃え |
|:---|:---:|---:|
|1 |2 |3 |
|4 |5 |6 |
```

| 左揃え | 中央揃え | 右揃え |
|:---|:---:|---:|
|1 |2 |3 |
|4 |5 |6 |
