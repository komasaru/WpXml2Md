WpXml2Md
========

# 概要
WordPress からエクスポートした投稿データの XMLファイルを読み込み Markdown に変換し、記事別にファイル出力する。

# 使用方法
1. 当 Ruby スクリプトと同じディレクトリ内に WordPress からエクスポートした投稿データのみの XML ファイルを配置する。
2. `ruby wp_xml2md.rb` を実行する。
3. ディレクトリを作成し、その中に記事別の md ファイルが作成される。

# 注意
- `li` タグで入れ子になっている部分は非対応。(入れ子部分の `li` かどうかの判別が困難。`li` タグは変換しない方がよかったかも？)
- `table` タグを Markdown 記法に変換するのは煩雑なので非対応。(align の指定等が不明)
- 記事内に埋め込んでいた、Amazon や楽天等の広告、その他独自に埋め込んでいるタグ等は非対応。
- その他、対応できていない部分もあるかと思います。(元となる WordPress でどのような記述をしているかによるので)

