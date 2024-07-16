# 一番外側
教科名を書く。

# 教科
## 記号
使う記号を書く。
基本的にそのままの記号で出てくるが、"+"は"±"と出るようになる。
いちいち"ぷらすまいなす"と打つのが面倒だからである。
## 解答記号
解答記号を選ぶ。
配列のtrue/falseは、大問ごとに番号がリセットされるかどうかを
* `1` 数値(1, 2, 3, ...)
* `ア` カタカナ(ア, イ, ウ, ..., ワ, ヲ, ン)
## 問題数
それぞれの大問に対し、問題数と配点を書く。
## 順番
読み込んだときに中身が崩れている可能性があるので順番を正すために書く。
これがなかった場合、読み込まれた順に出てくる。
## 満点
基本書かなくても良い。
書いてない場合、それぞれの問の点数の総和となる。
## 配点
中は解答と点数を書く。
### 解答
特に記号がなければそれが解答である。
<!-- `,`、`.`を使った場合、それぞれ別で解答記号が割り振られるが、`;`を使った場合、割り振られない。 -->
* `,` 全問正解で点数が入る。
* `.` 全問正解(順不同)で点数が入る。
* `;` 部分点。
### 点数
部分点は後ろの方に書く。

`["1;2;3", 5,2,1]`と書かれたとき、解答と点数はそれぞれ以下となる。
* `1` 5点
* `2` 2点
* `3` 1点
* それ以外 0点

# 例
ページのサンプルを選ぶとこれが出てくる。
```json
{
    "数学": {
        "記号": "-+0123456789abcd",
        "解答記号": ["ア", true],
        "順番": ["第一問", "第二問", "第三問[A]", "第三問[B]"],
        "問題数": {
            "第一問": [5, 25],
            "第二問": [9, 19],
            "第三問[A]": [4, 12],
            "第三問[B]": [3, 10]
        },
        "解答": {
            "第一問": [
                ["1", 5],
                ["2", 5],
                ["3", 5],
                ["2", 5],
                ["1", 5]
            ],
            "第二問": [
                ["1,2", 3],
                ["2.3", 3],
                ["1;2", 5, 2],
                ["3,3,4", 3],
                ["1;2;3", 5,2,1]
            ],
            "第三問[A]": [
                ["1", 3],
                ["1", 3],
                ["2", 3],
                ["2", 3]
            ],
            "第三問[B]": [
                ["a", 3],
                ["+", 4],
                ["2", 3]
            ]
        }
    },
    "国語": {
        "記号": "0123456789",
        "解答記号": ["1", false],
        "順番": ["1", "2", "3"],
        "満点": 60,
        "問題数": {
            "1": [3, 30],
            "2": [3, 30],
            "3": [3, 30]
        },
        "解答": {
            "1": [
                ["1", 10],
                ["1", 10],
                ["1", 10]
            ],
            "2": [
                ["1", 10],
                ["1", 10],
                ["1", 10]
            ],
            "3": [
                ["1", 10],
                ["1", 10],
                ["1", 10]
            ]
        }
    }
}
```