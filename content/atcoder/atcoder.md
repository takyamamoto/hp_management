Title:AtCoder Beginners Selection 雑感
Date: 2019.04.14
Category: atcoder
Tags: atcoder
Slug: atcoder
Author:
Summary:AtCoder Beginners Selection 雑感

<section class="pdf_page" aria-label="Page 1">
<div class="textlayer">
<div>プログラミング初心者の加藤です。勉強会の時に、とりあえずやってみたらいいよと言われたので、</div>
<div>よく分からないままやってみました。その概要と雑感です。</div>
<h2>・AtCoderとは？</h2>
<div>まず始めにAtCoderの説明から。AtCoderとは、オンライン上で競技プログラミングのコンテストを提供しているサイトのことです(https://atcoder.jp/?lang=ja)。</div>
<div>定期的にコンテストを主催していたり、企業から(広告や人材獲得戦略の一環として)</div>
<div>コンテストが開かれることもあります。</div>
<div>コンテストに参加する以外にも、コンテストで使用された問題を解くこともでき、初心者でも、「プログラミング勉強したいけど本をなぞるだけじゃつまらない！」っていう僕みたいなわがままな人にはちょうどいいモチベーションアッパーになると思います。</div>
<h2>・AtCoder Beginners Selectionを解こう！</h2>
<div>チュートリアルを読むと、「何をすれば良いか分からない人は、AtCoder Beginners Selection</div>
<div>から、まずいくつかの問題を解いてみましょう。」と書いてあります。ページに飛んでみると、さらに、「このコンテストは、『AtCoderに登録したけど何をしていいか分からない・・・！』という人に向けて作られた初心者向け問題集です。」とも書いてます。</div>
<div>何も分かってない子羊ちゃんは素直に優しい言葉に付いて行くのでした。</div>
<div>以下いくつかの問題をピックアップしてみます。</div>
<h3>・問題０：はじめてのあっとこーだー</h3>
<div>わざわざ平仮名で表記しちゃってまあどんな接待をしてくれるのやら...。問題文を読みます。&lt;/
<div>問題文</div>
<div>高橋君はデータの加工が行いたいです。</div>
<div>整数 a,b,cと、文字列 s が与えられます。</div>
<div>整数 a+b+c と、文字列 s を並べて表示しなさい。</div>
<div>入力</div>
<div>入力は次の形式で与えられる。</div>
<div>a</div>
<div>b c</div>
<div>　s</div>
<div>1 行目は、整数 a (1≦a≦1,000) が与えられる。</div>
<div>2 行目は、整数 b,c (1≦b,c≦1,000) が与えられる。</div>
<div>3 行目は、文字列 s が与えられる。この文字列の長さは 1文字以上</div>
<div>100文字以下であ</div>
<div>る。</div>
</div>
</section><section class="pdf_page" aria-label="Page 2">
<div class="textlayer">
<div>ん？</div>
<div>入力ってなんだ？(競プロ初心者並感)</div>
<div>いや入力はinputを使えばいい、でも「b c」はどうやって入力するんだ？(Python初心者並感)</div>
<div>そもそも複数行の入力ってどうするんだ？(プログラミング初心者並感)</div>
<div>......(思考停止)</div>
<div>数問解いた後の話ですが、気付きました。</div>
<div>ああこれが競技プログラミングなのか。</div>
<div>あれです、初心者あるあるの「思ってたのと違う」ってやつです。今回のは悪い意味ではないので</div>
<div>すが。</div>
<div>言語つながりで、例えば英語の問題なら、文法や読解、和文英訳など受験でさんざんやった形式</div>
<div>のものが思い浮かびます。てっきりそういう類いの問題が出るのかなと思っていたら、完全に実</div>
<div>践形式の問題で驚きました。英語始めたばっかりで、いきなり英会話しようと言われたら誰だっ</div>
<div>てそうなるでしょう。</div>
<div>このように競技プログラミングでは答えが決まってはなく、かなりのバリエーションがあり、独</div>
<div>自に考えたプログラムが答えになり得るというのが面白みの一つですね。また、同じ方針でも表</div>
<div>記の仕方がたくさんあって、まるで方言のようです。</div>
<div>まとめっぽくなりましたが問題に戻ります。</div>
<div>考えても分かる訳なさそうなので、この問題にだけついている解答例を見ます。</div>
<div>いまさらですが言語はPython3です。</div>
<div>なるほど、入力が複数行に分かれているのは文字列にエンターが含まれているからなのか、input</div>
<div>１回だけで全て読み込めるのではないのだな。行が分かれているというのは本質的ではなく、入</div>
<div>力をそのまま表示した結果なのか。いつものインタプリタと同じだ。というのがこの問題で一番</div>
<div>印象に残った事です。</div>
<div>map</div>
<div>とかフォーマットとか、多分見るのが２ヶ月ぶりとかで、ああそういえばそんなのあったな</div>
<div>状態です。</div>
<div>1.</div>
<div>a = int(input())</div>
<div>2.</div>
<div>b, c = map(int, input().split())</div>
<div>3.</div>
<div>s = input()</div>
<div>4.</div>
<div>print(“{} {}”.format(a+b+c, s))</div>
</div>
</section><section class="pdf_page" aria-label="Page 3">
<div class="textlayer">
<div>・問題４：Coins</div>
<div>コンピューターっぽくて印象的な問題です。</div>
<div>よくみる整数問題ですね。これは簡単に解けると思いきや...？</div>
<div>こういう問題は受験数学的にはパパッと場合分けが浮かびますが、その条件分けを実装するのは</div>
<div>面倒です。そう、受験問題では入力が１つだけですが、競技プログラミングでは複数の入力がな</div>
<div>されるため、全ての場合分けに対応しないといけません。できないことはないですが、正直言っ</div>
<div>てかなり面倒です。</div>
<div>(</div>
<div>http://delta114514.hatenablog.jp/entry/2018/03/15/014555</div>
<div>　より引用)</div>
<div>問題文</div>
<div>あなたは、500円玉をA枚、100円玉をB枚、50円玉をC枚持っています。これらの硬貨</div>
<div>の中から何枚かを選び、合計金額をちょうどX</div>
<div>円にする方法は何通りありますか。</div>
<div>同じ種類の硬貨同士は区別できません。２通りの硬貨の選び方は、ある種類の硬貨につ</div>
<div>いてその硬貨を選ぶ枚数が異なるとき区別されます。</div>
<div>制約</div>
<div>0</div>
<div>≤</div>
<div>A,B,C</div>
<div>≤</div>
<div>50</div>
<div>A+B+C</div>
<div>≥</div>
<div>1</div>
<div>50</div>
<div>≤</div>
<div>X</div>
<div>≤</div>
<div>20,000</div>
<div>A,B,C は整数である</div>
<div>Xは50の倍数である</div>
<div>入力</div>
<div>入力は以下の形式で標準入力から与えられる。</div>
<div>　A</div>
<div>　B</div>
<div>　C</div>
<div>　X</div>
<div>出力</div>
<div>硬貨を選ぶ方法の個数を出力せよ。</div>
<div>1.</div>
<div>a, b, c, x = map(int, [input() for i in range(4)])</div>
<div>2.</div>
<div>ans = 0</div>
<div>3.</div>
<div>for i in range(a+1):</div>
<div>4.</div>
<div>for j in range(b+1):</div>
<div>5.</div>
<div>for k in range(c+1):</div>
<div>6.</div>
<div>if i * 500 + j * 100 + k * 50 == x:</div>
<div>7.</div>
<div>ans += 1</div>
<div>8.</div>
<div>print</div>
<div>(ans)</div>
</div>
</section><section class="pdf_page" aria-label="Page 4">
<div class="textlayer">
<div>しばらく場合分けを考えていましたが、ギブアップして答えを検索。ABS</div>
<div>は有名らしく色んな人</div>
<div>が色んな言語で解答をあげています。</div>
<div>このコードはつまるところ、総当たりをして条件を満たすものをカウントしてるんですね。</div>
<div>なるほど！ヒトが計算するならこんな面倒なことはしないけれどコンピューターならできる。はっ</div>
<div>としました。</div>
<div>・問題７：Kagami Mochi</div>
<div>：普通の解法</div>
<div>(</div>
<div>http://delta114514.hatenablog.jp/entry/2018/03/15/014555</div>
<div>　より引用)</div>
<div>入力をリストにしてからセットにして要素数を数える。当然ですね。</div>
<div>僕はセットの存在を思い出せなかったので、次のようにしました。</div>
<div>問題文</div>
<div>X段重ねの鏡餅(X</div>
<div>≥</div>
<div>1) とはX枚の円形の餅を縦に積み重ねたものであって、どの餅もそ</div>
<div>の真下の餅より直径が小さい（一番下の餅を除く）もののことです。例えば、直径10、</div>
<div>8、6センチメートルの餅をこの順に下から積み重ねると 3 段重ねの鏡餅になり、餅を</div>
<div>一枚だけ置くと 1 段重ねの鏡餅になります。</div>
<div>ダックスフンドのルンルンはN枚の円形の餅を持っていて、そのうち i 枚目の餅の直径は</div>
<div>diセンチメートルです。これらの餅のうち一部または全部を使って鏡餅を作るとき、最</div>
<div>大で何段重ねの鏡餅を作ることができるでしょうか。</div>
<div>制約</div>
<div>1</div>
<div>≤</div>
<div>N</div>
<div>≤</div>
<div>100</div>
<div>1</div>
<div>≤</div>
<div>di</div>
<div>≤</div>
<div>100</div>
<div>入力値は全て整数である。</div>
<div>入力</div>
<div>入力は以下の形式で標準入力から与えられる。</div>
<div>　N</div>
<div>d1</div>
<div>　：</div>
<div>dN</div>
<div>出力</div>
<div>作ることのできる鏡餅の最大の段数を出力せよ。</div>
<div>1.</div>
<div>n = int(input())</div>
<div>2.</div>
<div>print(len(set(map(int, [input() for i in range(n)]))))</div>
</div>
</section><section class="pdf_page" aria-label="Page 5">
<div class="textlayer">
<div>：僕の解法</div>
<div>ソートしてからリストのままでなんとか数えあげました。</div>
<div>明らかに汚いですね。長いですし、n=1</div>
<div>で場合分けしてますし。こんな初心者じみた答えでも合っ</div>
<div>てたらいいんです。</div>
<div>・問題９：Daydream</div>
<div>問題文の通りに、後ろから４単語のどれかを検索していくのが一番わかりやすいと思われます。が、</div>
<div>わざわざerase</div>
<div>という単語を選んできたということは、こういうことでしょう。</div>
<div>僕の解法：</div>
<div>1.</div>
<div>n = int(input())</div>
<div>2.</div>
<div>a = sorted(list(map(int, [input() for i in range(n)])))</div>
<div>3.</div>
<div>ans = 1</div>
<div>4.</div>
<div>if n != 1:</div>
<div>5.</div>
<div>for i in range(n-1):</div>
<div>6.</div>
<div>if a[i] &lt; a[i+1]:</div>
<div>7.</div>
<div>ans += 1</div>
<div>8.</div>
<div>print(ans)</div>
<div>問題文</div>
<div>英小文字からなる文字列 S が与えられます。 Tが空文字列である状態から始め、以下の</div>
<div>操作を好きな回数繰り返すことで S=T とすることができるか判定してください。</div>
<div>Tの末尾にdream dreamer erase eraser のいずれかを追加する。</div>
<div>制約</div>
<div>1≦|S|≦105</div>
<div>Sは英小文字からなる。</div>
<div>入力</div>
<div>入力は以下の形式で標準入力から与えられる。</div>
<div>S</div>
<div>出力</div>
<div>S</div>
<div>=Tとすることができる場合YESを、そうでない場合NOを出力せよ。</div>
<div>1.</div>
<div>s = input()</div>
<div>2.</div>
<div>a=s.replace("eraser"," ")</div>
<div>3.</div>
<div>b=a.replace("erase"," ")</div>
<div>4.</div>
<div>c=b.replace("dreamer"," ")</div>
<div>5.</div>
<div>d=c.replace("dream"," ")</div>
<div>6.</div>
<div>if d.strip() == "":</div>
<div>7.</div>
<div>print("YES")</div>
<div>8.</div>
<div>else:</div>
<div>9.</div>
<div>print("NO")</div>
</div>
</section><section class="pdf_page" aria-label="Page 6">
<div class="textlayer">
<div>文字列の後ろからだけでなく、途中から抜いても、抜く単語の順番をうまく決めれば問題ないは</div>
<div>ずです。</div>
<div>変数をいちいち置いているのが恥ずかしいですが、通ればいいんです。</div>
<div>別解答：</div>
<div>(</div>
<div>http://delta114514.hatenablog.jp/entry/2018/03/15/014555</div>
<div>　より引用)</div>
<div>通ればなんでもいいはずなんですが、これはどうでしょう。</div>
<div>この解答例だと、”d erase r erase e erase a erase m” という文字列(スペースは抜いてくださ</div>
<div>い)もYESになってしまうはずなのですが、試しにこのコードを提出してみるとacceptされました。</div>
<div>(嘘解法なんでしょうか？にしては同じような答えを書いてる人が大勢います。)</div>
<div>・初学者にとっての競技プログラミング</div>
<div>解いてみた感想ですが、やはり考えるのは楽しいです。久々に数学的な頭の使い方をして懐かしさ</div>
<div>も覚えました。</div>
<div>また、何より、競技プログラミングは初学者にかなり便利なものだと感じました。</div>
<div>ほんとに基礎的な部分しか学習してなくても解けるというのは取り組みやすいですし、結果がだ</div>
<div>せることは嬉しいです。過去問ならネット上にたくさん解説があるのでつまってもなんとかなりま</div>
<div>す。</div>
<div>他の人のコードを見ることができ、考え方の幅も広がります。上手く書けなかったコードを見直</div>
<div>したり、異なった方針で書かれたコードを見るのはいい刺激になります。</div>
<div>特に基礎の文法に慣れるという点では一番だと思います。基礎を洗練させることは必ずこの先モ</div>
<div>ジュールやパッケージを使っていくにしても、理解して扱えることができ役に立つことでしょう。</div>
<div>もちろん万能ではありません。競技プログラミングの内容はプログラミング一般から見て偏って</div>
<div>いるらしいです。「競技プログラミング　デメリット」で調べると批判がたくさん出てきます。</div>
<div>でも少なくともPython</div>
<div>会に入ってる初心者の人は、ソフト開発のような能力ではなく、プログラ</div>
<div>ミングをツールとして扱える能力を求めている人がほとんどでしょうから、うってつけの教材だ</div>
<div>と思います。</div>
<div>簡単なブロック崩しのゲームを作ったことがありますが、今回の方がよっぽど練習になりました。</div>
<div>もし興味があれば皆さんも是非試してみてください。</div>
</div>
</section>
