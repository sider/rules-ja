# rules-ja
こちらは、Goodcheck, Querly, Phinder, TyScanのカスタムルールのサンプル集を配置します。

# ディレクトリ

- languages/ 以下に、言語別にカスタムルールを定義した goodcheck.ymlを配置しています

```
# 参考

languages
├── java
│   └── goodcheck.yml
├── terraform
│   ├── goodcheck.yml
│   └── sample.tf
├── python
    └── goodcheck.yml


3 directories, 3 files
```

# 利用方法

[Sider](https://sider.review) を使ってコードのチェックを実施することを前提にしております。

### goodcheck.yml

- 基本は、リポジトリ直下に、リポジトリの内容（主な言語）に対応した goodcheck.yml を配置します
- Siderの解析に利用したいToolから、Goodcheckを有効にします
- Siderに連携したリポジトリにプルリクエストが作成された段階で、この定義に応じたチェックが実施されます

### phinder.yml (PHP用)

- 基本は、リポジトリ直下に、phinder.yml を配置します
- Siderの解析に利用したいToolから、Phinderを有効にします
- Siderに連携したリポジトリにプルリクエストが作成された段階で、この定義に応じたチェックが実施されます

