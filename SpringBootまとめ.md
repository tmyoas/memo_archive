SpringBootまとめ
===

# アノテーション

- @SpringBootApplication
    - = @Configuration + @EnableAutoConfiguration + @ComponentScan
    - @Configuration
    	- Springの設定がJavaで行えるようになる（とは？）
    	- このクラスがBean設定を行うクラスであることを示す
    	-　必ずクラス宣言の前につける
    - @EnableAutoConfiguration
    	- Springの設定自動化、依存関係の追加でライブラリが設定書かなくても使える
    - @ComponentScan
    	- DIコンテナにBeanを自動登録する、これが書かれたclassを起点にして配下をスキャン、@ComponentがついたclassをBeanとして登録

- @Component
	- このclassをbean登録するよー <- なんか違う?
	- コンポーネント = 強いクラス = Beanを利用する
	- 必ずクラス宣言の手前につける

- @Bean
	- 初期値（init的な？）だよー

- @EnableAsync
    - 非同期処理有効にするよー
- @Async("hoge")
	- 非同期処理したいclassにつける、パラメータで定義した名前のTaskExecutor(Springの非同期処理を行うクラス)を使う

- @Actuator

- @Builder

- @RequiredArgsConstructor
	- Lombok(@getter, @setter, @Dataとかもこれ)
	- finalな変数に値をセットするための引数付きコンストラクタを生成する
	- delombok

- @Autowired
	- 型を使ってDIコンテナの中のbeanと変数を紐づけ、初期値セットまでやる
		- このときbeanの登録されていない or 定義が複数ある型の場合はエラーになる
	- @Componentの中で使われる


# 他の用語

- Bean
	- Springが自動生成したインスタンス、DIコンテナのおかげでnewとか初期値登録とかしなくてよい
- DIコンテナ
	- この中にBeanが登録される、インスタンスのnew消去とか初期値設定を勝手にやってくれるようになる、初期値はコードの外に出せる
- 

# gradle
- Spring Boot Gradle plugin
	- その名の通り、GradleでSpringBootのビルドやら実行やらをするためのプラグイン
- bootRun
	- build + Run (+ ホットデプロイ？)