# Privacy Policy — PnL Calendar

**Effective date: September 9, 2026**

[English](#english) · [简体中文](#简体中文) · [Español](#español) · [日本語](#日本語)

This policy applies to the PnL Calendar app for iOS and iPadOS. PnL Calendar is
an independent third-party utility and is not affiliated with or endorsed by
Interactive Brokers LLC or its affiliates.

## English

### 1. Data handled by the app

PnL Calendar handles the following data only to provide its features:

- The IBKR Flex Token and Query ID that you enter.
- Flex report content returned by Interactive Brokers, including report dates,
  net asset value changes, profit and loss, returns, and related values used to
  calculate the performance calendar.
- On-device preferences such as language, theme, gain/loss colors, and local
  synchronization/cache state.

The developer does not receive or collect this data. You can use the built-in
demo mode without providing IBKR credentials.

If you contact support through the App Store or GitHub, the developer receives
only the information you choose to provide. It is used to respond to your
request and is retained by the communication service you use. Do not send
credentials or financial report data in a support request.

### 2. How data is used and transferred

When you validate credentials or synchronize a report, the app sends the Flex
Token, Query ID, and requested date range directly from your device to the
Interactive Brokers Flex Web Service over HTTPS. The response is processed on
your device to display and calculate performance information.

The app is read-only. It does not place trades, manage funds, change account
settings, or provide financial or investment advice.

### 3. Storage and retention

- Flex credentials are stored in the iOS Keychain using device-only protection.
- Downloaded report data is cached in the app's private Application Support
  directory.
- App preferences are stored locally using iOS preferences storage.

The app does not upload this stored data to a developer-operated server. Data
remains on the device until you delete it. Use **Settings → Delete All Local
Data** to remove credentials, cached financial data, and app preferences. App
cache and preferences are normally removed when the app is uninstalled. Because
Keychain retention can be controlled by iOS, use the in-app deletion control
before uninstalling if you want to ensure that credentials are removed.

### 4. Sharing, selling, analytics, and tracking

PnL Calendar has no developer-operated backend, advertising, analytics SDK, or
cross-app tracking. The developer does not sell, rent, or share your personal or
financial data. Data is sent only to Interactive Brokers when you request the
IBKR-powered features described above.

Interactive Brokers and Apple may process information under their own terms and
privacy policies when you use their services. Their practices are outside the
developer's control.

### 5. Security

PnL Calendar uses HTTPS for IBKR requests, the iOS Keychain for credentials, and
the app sandbox for cached data. No method of electronic storage or transmission
can be guaranteed to be completely secure. You are responsible for protecting
access to your device and IBKR credentials.

### 6. Your choices

You may:

- Use demo mode without connecting an IBKR account.
- Disconnect IBKR and delete all local data from Settings.
- Revoke or regenerate the Flex Token in IBKR Client Portal.
- Uninstall the app to remove its sandboxed cache and preferences.

Because the developer does not receive your app data, the developer cannot view,
export, correct, or delete it on your behalf.

### 7. Changes to this policy

Material changes will be published in this file with an updated effective date.

### 8. Contact

For privacy questions, use the support link on the App Store product page or
open a [GitHub Issue](../../issues). Do not include Flex Tokens, Query IDs,
account identifiers, balances, positions, or report data in a public issue.

## 简体中文

### 1. 应用处理的数据

盈亏日历仅为提供应用功能而处理以下数据：

- 你输入的 IBKR Flex Token 和 Query ID；
- Interactive Brokers 返回的 Flex 报表内容，包括报表日期、净资产变化、盈亏、
  收益率及生成收益日历所需的相关数值；
- 保存在设备上的语言、主题、涨跌颜色以及本地同步和缓存状态等偏好设置。

开发者不会接收或收集这些数据。你也可以不提供 IBKR 凭据，直接使用内置演示模式。

如果你通过 App Store 或 GitHub 联系支持，开发者只会收到你主动提供的信息。这些信息
仅用于回复你的请求，并由你所使用的通信服务保存。请勿在支持请求中发送凭据或财务
报表数据。

### 2. 数据的用途和传输

当你验证凭据或同步报表时，应用会通过 HTTPS 将 Flex Token、Query ID 和请求的日期
范围从设备直接发送至 Interactive Brokers Flex Web Service。返回内容在设备本地处理，
用于展示和计算收益信息。

本应用为只读工具，不会下单、管理资金、更改账户设置，也不提供金融或投资建议。

### 3. 存储与保留

- Flex 凭据使用仅限本设备的保护方式保存在 iOS 钥匙串中；
- 下载的报表数据缓存在应用的私有 Application Support 目录中；
- 应用偏好通过 iOS 的本地偏好存储保存在设备上。

应用不会将这些本地数据上传至开发者运营的服务器。数据会保留在设备上，直到你主动
删除。使用 **设置 → 删除全部本地数据** 可以删除凭据、财务缓存和应用偏好。卸载应用
通常会删除应用沙盒中的缓存和偏好；由于钥匙串的保留行为由 iOS 控制，如果希望确保
凭据被删除，请在卸载前使用应用内的删除功能。

### 4. 共享、出售、分析与追踪

盈亏日历不使用开发者运营的后端、广告、分析 SDK 或跨应用追踪。开发者不会出售、
出租或共享你的个人或财务数据。只有在你使用上述 IBKR 功能时，相关数据才会发送给
Interactive Brokers。

在使用 Interactive Brokers 和 Apple 服务时，这些公司可能依据其各自的条款与隐私
政策处理信息，其行为不受本应用开发者控制。

### 5. 安全

盈亏日历使用 HTTPS 发送 IBKR 请求，使用 iOS 钥匙串保存凭据，并使用应用沙盒保存
缓存。任何电子存储或传输方式都无法保证绝对安全。你有责任保护设备访问权限和 IBKR
凭据。

### 6. 你的选择

你可以：

- 不连接 IBKR 账户，直接使用演示模式；
- 在设置中断开 IBKR 并删除全部本地数据；
- 在 IBKR Client Portal 中撤销或重新生成 Flex Token；
- 卸载应用以删除其沙盒缓存和偏好。

由于开发者不会收到应用数据，因此无法代你查看、导出、更正或删除这些数据。

### 7. 政策变更

如有重大变更，我们会在本文件中发布新版本并更新生效日期。

### 8. 联系方式

如有隐私问题，请使用 App Store 产品页面中的支持链接，或创建
[GitHub Issue](../../issues)。请勿在公开问题中提供 Flex Token、Query ID、账户标识、
余额、持仓或报表数据。

## Español

### 1. Datos tratados por la app

PnL Calendar trata los siguientes datos únicamente para ofrecer sus funciones:

- El Flex Token y el Query ID de IBKR que introduces.
- El contenido de los informes Flex devueltos por Interactive Brokers, incluidas
  las fechas, los cambios del valor liquidativo, las ganancias y pérdidas, las
  rentabilidades y los valores relacionados utilizados para crear el calendario.
- Preferencias guardadas en el dispositivo, como idioma, tema, colores de
  ganancias/pérdidas y estado local de sincronización y caché.

El desarrollador no recibe ni recopila estos datos. Puedes usar el modo de
demostración sin proporcionar credenciales de IBKR.

Si contactas con soporte mediante App Store o GitHub, el desarrollador solo
recibirá la información que decidas proporcionar. Se utilizará para responder a
tu solicitud y será conservada por el servicio de comunicación utilizado. No
envíes credenciales ni informes financieros en una solicitud de soporte.

### 2. Uso y transferencia de los datos

Al validar las credenciales o sincronizar un informe, la app envía el Flex Token,
el Query ID y el intervalo de fechas solicitado directamente desde tu dispositivo
al Flex Web Service de Interactive Brokers mediante HTTPS. La respuesta se
procesa en tu dispositivo para mostrar y calcular la información de rendimiento.

La app es de solo lectura. No realiza operaciones, administra fondos, modifica la
cuenta ni ofrece asesoramiento financiero o de inversión.

### 3. Almacenamiento y conservación

- Las credenciales Flex se guardan en el llavero de iOS con protección exclusiva
  para el dispositivo.
- Los informes descargados se almacenan en la caché privada de la app.
- Las preferencias se guardan localmente mediante el sistema de preferencias de
  iOS.

La app no sube estos datos a ningún servidor operado por el desarrollador. Los
datos permanecen en el dispositivo hasta que los eliminas. Usa **Ajustes →
Eliminar todos los datos locales** para borrar credenciales, datos financieros en
caché y preferencias. Al desinstalar se suelen eliminar la caché y las
preferencias. Como iOS controla la conservación del llavero, utiliza primero la
opción de borrado de la app si quieres asegurarte de eliminar las credenciales.

### 4. Cesión, venta, analítica y seguimiento

PnL Calendar no tiene un backend operado por el desarrollador ni utiliza
publicidad, SDK de analítica o seguimiento entre apps. El desarrollador no vende,
alquila ni comparte tus datos personales o financieros. Los datos solo se envían
a Interactive Brokers cuando solicitas las funciones de IBKR descritas arriba.

Interactive Brokers y Apple pueden tratar información conforme a sus propias
condiciones y políticas de privacidad. Sus prácticas quedan fuera del control del
desarrollador.

### 5. Seguridad

PnL Calendar utiliza HTTPS para las solicitudes a IBKR, el llavero de iOS para
las credenciales y el entorno aislado de la app para la caché. Ningún método de
almacenamiento o transmisión electrónica puede garantizar una seguridad total.
Eres responsable de proteger el acceso a tu dispositivo y tus credenciales.

### 6. Tus opciones

Puedes usar el modo de demostración, eliminar todos los datos locales desde
Ajustes, revocar o regenerar el Flex Token en IBKR Client Portal y desinstalar la
app para eliminar su caché y preferencias. Como el desarrollador no recibe los
datos de la app, no puede consultarlos, exportarlos, corregirlos ni eliminarlos en
tu nombre.

### 7. Cambios en esta política

Los cambios importantes se publicarán en este archivo con una fecha de entrada
en vigor actualizada.

### 8. Contacto

Para cuestiones de privacidad, utiliza el enlace de soporte de la página del
producto en App Store o abre una [incidencia en GitHub](../../issues). No incluyas
Flex Tokens, Query IDs, identificadores de cuenta, saldos, posiciones ni datos de
informes en una incidencia pública.

## 日本語

### 1. Appが取り扱うデータ

PnL Calendarは、機能を提供する目的に限り、次のデータを取り扱います。

- ユーザーが入力したIBKR Flex TokenおよびQuery ID
- Interactive Brokersから返されるFlexレポート（レポート日、純資産価値の変動、
  損益、収益率、およびパフォーマンスカレンダーの計算に必要な関連数値）
- 言語、テーマ、騰落色、ローカルの同期・キャッシュ状態など、デバイス上の設定

開発者がこれらのデータを受信または収集することはありません。IBKRの認証情報を
入力せずに、内蔵のデモモードを利用することもできます。

App StoreまたはGitHubを通じてサポートへ連絡した場合、開発者はユーザーが任意で
提供した情報のみを受け取ります。その情報は問い合わせへの回答にのみ使用され、
利用した通信サービス上に保持されます。認証情報や金融レポートデータをサポート
依頼に含めないでください。

### 2. データの利用と送信

認証情報の検証またはレポートの同期を行うと、AppはFlex Token、Query ID、指定した
日付範囲を、HTTPS経由でデバイスからInteractive Brokers Flex Web Serviceへ直接送信
します。応答はデバイス上で処理され、パフォーマンス情報の表示と計算に使用されます。

本Appは読み取り専用です。取引の発注、資金の管理、口座設定の変更、金融・投資助言
は行いません。

### 3. 保存と保持

- Flex認証情報は、デバイス専用の保護を使用してiOSキーチェーンに保存されます。
- ダウンロードしたレポートは、Appのプライベート領域にキャッシュされます。
- Appの設定は、iOSの設定ストレージを使用してデバイス上に保存されます。

これらのデータが開発者運営のサーバーへアップロードされることはありません。
データは削除するまでデバイスに保持されます。**設定 → ローカルデータをすべて削除**
を使用すると、認証情報、キャッシュ済み金融データ、App設定を削除できます。Appを
アンインストールすると通常、キャッシュと設定は削除されます。キーチェーンの保持は
iOSによって管理されるため、認証情報を確実に削除するには、アンインストール前に
App内の削除機能を使用してください。

### 4. 共有、販売、解析、トラッキング

PnL Calendarには、開発者運営のバックエンド、広告、解析SDK、App間トラッキングは
ありません。開発者が個人データや金融データを販売、貸与、共有することはありません。
上記のIBKR機能をユーザーが利用した場合にのみ、データがInteractive Brokersへ送信
されます。

Interactive BrokersおよびAppleは、それぞれの規約とプライバシーポリシーに基づいて
情報を処理する場合があります。それらの取り扱いは開発者の管理外です。

### 5. セキュリティ

PnL Calendarは、IBKRへのリクエストにHTTPS、認証情報の保存にiOSキーチェーン、
キャッシュの保存にAppサンドボックスを使用します。ただし、電子的な保存や送信の
完全な安全性を保証することはできません。デバイスへのアクセスとIBKR認証情報は、
ユーザー自身で保護してください。

### 6. ユーザーの選択肢

デモモードの利用、設定からのローカルデータ削除、IBKR Client PortalでのFlex Token
の失効・再生成、Appのアンインストールが可能です。開発者はAppデータを受信しない
ため、ユーザーに代わってデータを閲覧、書き出し、訂正、削除することはできません。

### 7. 本ポリシーの変更

重要な変更は、更新後の発効日とともに本ファイルで公開します。

### 8. お問い合わせ

プライバシーに関するお問い合わせは、App Store製品ページのサポートリンク、または
[GitHub Issues](../../issues)をご利用ください。公開Issueには、Flex Token、Query ID、
口座識別子、残高、ポジション、レポートデータを記載しないでください。
