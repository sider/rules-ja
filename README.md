# rules-ja
こちらでは、Siderで利用できる、[Goodcheck](https://github.com/sider/goodcheck), [Querly](https://github.com/soutaro/querly), [Phinder](https://github.com/sider/phinder), [TyScan](https://github.com/sider/TyScan)のカスタムルールのサンプル集を配置します。

各言語、普段コードレビューなどでよく指摘される内容や、ベストプラクティス的なルールをまとめて公開しています。


# ディレクトリ

- languages/ 以下に、言語別にカスタムルールを定義した goodcheck.ymlを配置しています

```
# 参考

% tree -L 2 languages

languages
├── java
│   ├── goodcheck.apache-commons.yml
│   ├── goodcheck.junit.yml
│   ├── goodcheck.spring.yml
│   └── goodcheck.yml
├── php
│   ├── goodcheck.yml
│   └── phinder.yml
├── python
│   └── goodcheck.yml
├── ruby
│   ├── goodcheck.yml
│   └── querly.yml
├── scala
│   └── goodcheck.yml
├── terraform
│   └── goodcheck.yml
└── unity
    └── goodcheck.yml

7 directories, 12 files
```

# ご利用方法

[Sider](https://sider.review) を使ってコードのチェックを実施することを前提にしております。
このリポジトリから、皆様のリポジトリの言語にあった設定を選びリポジトリ直下に配置して、ご利用下さい。

また、その上で皆様のお手元で独自ルールを追加して、ご活用下さい。

### goodcheck.yml

- 基本は、リポジトリ直下に、リポジトリの内容（主な言語）に対応した goodcheck.yml を配置します
- Siderの解析に利用したいToolから、Goodcheckを有効にします
- Siderに連携したリポジトリにプルリクエストが作成された段階で、この定義に応じたチェックが実施されます

### phinder.yml (PHP用)

- 基本は、リポジトリ直下に、phinder.yml を配置します
- Siderの解析に利用したいToolから、Phinderを有効にします
- Siderに連携したリポジトリにプルリクエストが作成された段階で、この定義に応じたチェックが実施されます

### querly.yml (Ruby用)

- 基本は、リポジトリ直下に、querly.yml を配置します
- Siderの解析に利用したいToolから、Querlyを有効にします
- Siderに連携したリポジトリにプルリクエストが作成された段階で、この定義に応じたチェックが実施されます
