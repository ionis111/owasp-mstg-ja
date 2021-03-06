## ユーザー連携のテスト

### ユーザー啓発のテスト (MSTG-STORAGE-12)

開発者がユーザーに知っておくべきことを教えなければならない責任の面で、最近多くのことが起こっています。
これは特にヨーロッパの [一般データ保護規則 (GDPR)](https://gdpr-info.eu/ "GDPR") の導入に伴ってシフトしています。そのときから、プライベートなデータで何が起こっているのか、またその理由をユーザーに教えるのがベストです。
さらに、アプリケーションを適切に使用する方法についてユーザーに通知することをお勧めします。これによりユーザー情報のセキュアな処理および操作を保証します。
次に、PII であるかどうかにかかわらず、アプリがアクセスするデバイスデータの種類についてユーザーに通知すべきです。
最後に、OSS 関連情報をユーザーと共有する必要があります。
全四項目をここではカバーします。

> これは MSTG プロジェクトであり、法的な手引書ではないことをご了承ください。したがって、ここでは GDPR および他の関連する法律については扱いません。

#### ユーザーに個人情報を通知する

ビジネスプロセスのためにユーザーから個人情報が必要となる場合には、データで何をするのか、なぜ必要なのかをユーザーに知らせる必要があります。データの実際の処理を行う第三者がいる場合には、それについてもユーザーに知らせる必要があります。最後に、サポートする必要がある三つのプロセスがあります。

- **忘れられる権利**: ユーザーは自分のデータの削除を要求することが可能であり、その方法を説明されている必要があります。
- **データを修正する権利**: ユーザーはいつでも自分の個人情報を修正することが可能であり、その方法を説明されている必要があります。
- **ユーザーデータにアクセスする権利**: ユーザーはアプリケーションが持つ自分のすべての情報を要求することが可能であり、ユーザーはこの情報を要求する方法を説明されている必要があります。

これらのほとんどはプライバシーポリシーでカバーできますが、ユーザーが理解できるようにしてください。

追加のデータを処理する必要がある場合には、ユーザーに再度同意を求める必要があります。この同意要求の中で、ユーザーが追加データの共有を元に戻す方法を明確にする必要があります。同様に、ユーザーの既存のデータセットをリンクする必要がある場合には、それについてユーザーの同意を求める必要があります。

#### ユーザーにベストなセキュリティプラクティスを通知する

ユーザーに通知できるベストプラクティスのリストは以下の通りです。

- **指紋の使用**: アプリが認証に指紋を使用し、高いリスクの取引や情報へのアクセスを提供する場合には、デバイスに複数の他人の指紋を登録した際に生じる問題についてユーザーに知らせます。
- **ルート化および脱獄**: アプリがルート化もしくは脱獄済みデバイスを検出する場合には、そのデバイスの脱獄やルート化の状態のために特定の高いリスクのアクションがさらにリスクを抱えることをユーザーに知らせます。
- **特定の資格情報**: ユーザーがリカバリーコード、パスワード、ピンをアプリケーションから取得 (あるいはいずれかを設定) する場合には、これを他人と決して共有してはならず、アプリだけがそれを要求することを教えます。
- **アプリケーションの配布**: 高いリスクのアプリケーションの場合には、アプリを配布する公式な方法を伝えることを推奨します。そうしなければ、ユーザーは他のチャネルを使用して危険なバージョンのアプリケーションをダウンロードする可能性があります。

#### デバイスデータへのアクセス

Google Play ストアと Apple App Store で部分的にカバーされていますが、あなたのアプリが使用するサービスとその理由をユーザーに説明する必要があります。以下に例を示します。

- あなたのアプリは連絡先リストへのアクセスを必要としますか？
- あなたのアプリはデバイスの位置情報サービスにアクセスする必要がありますか？
- あなたのアプリはデバイスを識別するためにデバイス識別子を使用しますか？

あなたのアプリがこのようなことをする必要がある理由をユーザーに説明します。この話題の詳細については [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/requesting-permission/ "Apple Human Interface Guidelines") および [Android App permissions best practices](https://developer.android.com/training/permissions/requesting.html#explain "Android App permissions best practices") にあります。

#### 共有する必要があるその他の情報 (OSS 情報)

著作権法では、アプリで使用されているサードパーティライブラリについてユーザーに知らせる必要があります。各サードパーティライブラリについて、特定の情報 (著作権、改変、オリジナルの作者など) をユーザーに提示する必要があるかどうかを確認するために、ライセンスを参照する必要があります。これには、専門家に法的助言を求めるのがベストです。例として [Big Nerd Ranch のブログ投稿](https://www.bignerdranch.com/blog/open-source-licenses-and-android/ "Example on license overview") があります。さらに、ウェブサイト [TL;DR - Legal](https://tldrlegal.com/ "TL;DR - Legal") は各ライセンスに必要なものを把握するのに役立ちます。

### 参考情報

#### OWASP MASVS

- MSTG-STORAGE-12: "アプリは処理される個人識別情報の種類をユーザーに通知しており、同様にユーザーがアプリを使用する際に従うべきセキュリティのベストプラクティスについて通知している。"

#### オープンソースライセンス言及の例

- <https://www.bignerdranch.com/blog/open-source-licenses-and-android/>

#### ライセンスの理解に役立つウェブサイト

- <https://tldrlegal.com/>

#### パーミッションリクエストに関するガイダンス

- Apple Human Interface Guidelines - <https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/requesting-permission/>
- Android App permissions best practices - <https://developer.android.com/training/permissions/requesting.html#explain>
