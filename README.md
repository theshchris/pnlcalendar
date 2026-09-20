# PnL Calendar / 盈亏日历

[English](#english) · [简体中文](#简体中文) · [Español](#español) · [日本語](#日本語)

<p align="center">
  <img src="ios/AppStoreScreenshots/iPhone-6.5/en/01-day-august-2026.png" width="220" alt="English daily calendar">
  <img src="ios/AppStoreScreenshots/iPhone-6.5/zh-Hans/03-year-2026.png" width="220" alt="中文年度视图">
  <img src="ios/AppStoreScreenshots/iPhone-6.5/ja/04-settings.png" width="220" alt="日本語設定画面">
</p>

## Support

Email: [shchris2019@gmail.com](mailto:shchris2019@gmail.com)

- English: For bugs or feature requests, email the address above or open a
  [GitHub Issue](https://github.com/theshchris/pnlcalendar/issues).
- 简体中文：如需报告问题或提出建议，请发送邮件至上述地址或创建
  [GitHub Issue](https://github.com/theshchris/pnlcalendar/issues)。
- Español: Para informar de errores o proponer funciones, escribe al correo
  anterior o abre una [incidencia en GitHub](https://github.com/theshchris/pnlcalendar/issues).
- 日本語：不具合の報告や機能の提案は、上記メールアドレスまたは
  [GitHub Issues](https://github.com/theshchris/pnlcalendar/issues)をご利用ください。

Never include a Flex Token, Query ID, account identifier, balance, position, or
report content in a public issue, screenshot, or log.

请勿在公开问题、截图或日志中提供 Flex Token、Query ID、账户标识、余额、持仓或
报表内容。

## English

### Overview

PnL Calendar is a free, ad-free, read-only, local-first performance calendar for
Interactive Brokers users. It turns account performance into clear daily,
monthly, and yearly views without sending financial data through a
developer-operated server.

The current version synchronizes performance from Interactive Brokers and is
suitable for reviewing U.S. and global stocks, ETFs, options, futures, and other
investments. Results are consolidated in the account's base currency.

### Features

- Daily performance calendar, twelve-month overview, and multi-year summary
- Net P&L, time-weighted return, win rate, and configurable period details
- Display P&L, return, or both together
- Optional mark-to-market and realized P&L, cash flow, dividends, interest,
  commissions, and fees when those fields are available in the report
- Optional automatic synchronization when the app opens, plus manual sync
- Direct, read-only connection to the IBKR Flex Web Service
- Flex credentials protected by the iOS Keychain
- Financial report cache stored only in the app's private local storage
- No developer-operated backend, advertising, analytics SDK, or cross-app tracking
- English, Simplified Chinese, Spanish, and Japanese
- Light and dark themes, configurable gain/loss colors, and configurable week start
- Native layouts for iPhone and iPad
- Built-in demo data for exploring the app without an IBKR account

### Using live Interactive Brokers data

Live synchronization requires your own Activity Flex Query ID and Flex Token.
In IBKR Client Portal:

1. Open **Reporting → Flex Queries**.
2. Create or edit an **Activity Flex Query** with XML output.
3. Enable **Change in NAV** and the fields needed for dates, starting and ending
   value, transfers, deposits and withdrawals, mark-to-market P&L, realized P&L,
   dividends, interest, commissions, fees, and TWR.
4. To display realized P&L while using MTM mode, also enable **Trades** with
   Trade Date, Level of Detail, FIFO P&L Realized, Currency, and FX Rate to Base.
5. Save the query and copy its Query ID.
6. Open **Flex Web Service Configuration**, enable the service, choose an expiry
   period, and create a token. Leave the IP restriction empty for phone use.
7. Enter the Query ID and Flex Token in PnL Calendar, then validate and save.

Only fields included in the query can appear in optional detail rows. PnL
Calendar only reads reports. It cannot place trades, manage funds, or change
account settings.

### Privacy

The app connects directly from the device to Interactive Brokers over HTTPS.
Credentials are stored in the iOS Keychain, and downloaded report data is cached
in the app sandbox. The developer does not receive or collect this data.

Read the complete [Privacy Policy](PRIVACY.md).

### Development

Requirements:

- Xcode 16 or later
- iOS/iPadOS 18.0 or later

Open [`ios/PnLCalendar.xcodeproj`](ios/PnLCalendar.xcodeproj), select an iPhone
or iPad simulator, and run the `PnLCalendar` scheme. Simulator builds must remain
signed for Keychain access.

The deterministic App Store screenshot workflow is documented in
[`ios/AppStoreScreenshots`](ios/AppStoreScreenshots/README.md).

The repository also contains the original self-hosted Node.js web prototype:

```bash
cp .env.example .env
# Add your own IBKR_FLEX_TOKEN and IBKR_FLEX_QUERY_ID to .env
npm start
```

Open <http://127.0.0.1:4187>. Use `npm test` to run the web parser tests. Never
commit `.env` or expose the local server to an untrusted network.

### Repository layout

- `ios/` — native SwiftUI app, tests, branding, and App Store screenshots
- `lib/` — Flex parsing and period logic for the web prototype
- `public/` — web prototype interface
- `server.js` — local web prototype server
- `PRIVACY.md` — public privacy policy for the iOS and iPadOS app

### Disclaimer

PnL Calendar is an independent third-party utility and is not affiliated with,
endorsed by, or sponsored by Interactive Brokers LLC or its affiliates.
Interactive Brokers and IBKR are trademarks of their respective owners.

The app is provided for informational record-keeping only. It does not execute
trades, manage funds, or provide financial, investment, tax, or legal advice.

## 简体中文

### 简介

盈亏日历是一款面向 Interactive Brokers 用户的免费、无广告、只读、本地优先收益
日历。应用将账户表现整理为清晰的每日、每月和年度视图，财务数据不会经过开发者运营
的服务器。

当前版本支持从 Interactive Brokers 同步账户表现，适合复盘美股及其他股票、ETF、
期权、期货等投资。所有结果均以账户基础货币汇总显示。

### 功能

- 每日收益日历、十二个月总览和多年年度汇总
- 净盈亏、时间加权收益率、胜率和可配置的周期明细
- 可显示盈亏金额、收益率，或同时显示两者
- 当报表包含相应字段时，可选显示盯市盈亏、已实现盈亏、资金流、股息、利息、佣金和费用
- 可选择打开应用时自动同步，也可随时手动同步
- 直接、只读连接 IBKR Flex Web Service
- Flex 凭据保存在 iOS 系统钥匙串中
- 财务报表缓存仅保存在应用的本地私有空间
- 不使用开发者后端、广告、分析 SDK 或跨应用追踪
- 支持英语、简体中文、西班牙语和日语
- 支持浅色、深色主题以及自定义涨跌颜色和每周起始日
- 原生适配 iPhone 和 iPad
- 内置演示数据，无需 IBKR 账户也能浏览应用

### 使用 Interactive Brokers 真实数据

实时同步需要你自己的 Activity Flex Query ID 和 Flex Token。请在 IBKR Client Portal
中完成以下设置：

1. 打开 **Reporting → Flex Queries**。
2. 创建或编辑一个输出格式为 XML 的 **Activity Flex Query**。
3. 启用 **Change in NAV**，并加入日期、期初与期末净值、转账、存取款、盯市盈亏、
   已实现盈亏、股息、利息、佣金、费用和 TWR 所需字段。
4. 如果在 MTM 模式下仍需显示已实现盈亏，还要启用 **Trades**，并加入 Trade Date、
   Level of Detail、FIFO P&L Realized、Currency 和 FX Rate to Base。
5. 保存查询并复制 Query ID。
6. 打开 **Flex Web Service Configuration**，启用服务、选择有效期并创建 Token。
   如果用于手机，请将 IP 限制留空。
7. 在盈亏日历中输入 Query ID 和 Flex Token，然后验证并保存。

只有查询中包含的字段才能出现在可选明细中。盈亏日历只读取报表，不能下单、管理资金
或更改账户设置。

### 隐私

应用通过 HTTPS 从设备直接连接 Interactive Brokers。凭据保存在 iOS 钥匙串中，下载
的报表数据缓存在应用沙盒内，开发者不会接收或收集这些数据。

请阅读完整的[隐私政策](PRIVACY.md)。

### 开发

环境要求：

- Xcode 16 或更高版本
- iOS/iPadOS 18.0 或更高版本

打开 [`ios/PnLCalendar.xcodeproj`](ios/PnLCalendar.xcodeproj)，选择 iPhone 或 iPad
模拟器，然后运行 `PnLCalendar` scheme。模拟器构建需要保持签名，才能访问钥匙串。

App Store 固定演示数据截图流程记录在
[`ios/AppStoreScreenshots`](ios/AppStoreScreenshots/README.md) 中。

仓库还包含原始的 Node.js 本地自托管网页原型：

```bash
cp .env.example .env
# 在 .env 中加入你自己的 IBKR_FLEX_TOKEN 和 IBKR_FLEX_QUERY_ID
npm start
```

打开 <http://127.0.0.1:4187>。使用 `npm test` 运行网页解析测试。请勿提交 `.env`，
也不要将本地服务器暴露在不可信网络中。

### 仓库结构

- `ios/` — 原生 SwiftUI 应用、测试、品牌资源和 App Store 截图
- `lib/` — 网页原型的 Flex 解析和周期逻辑
- `public/` — 网页原型界面
- `server.js` — 本地网页原型服务器
- `PRIVACY.md` — iOS 和 iPadOS 应用的公开隐私政策

### 免责声明

盈亏日历是独立的第三方工具，与 Interactive Brokers LLC 及其关联公司不存在隶属、
认可或赞助关系。Interactive Brokers 和 IBKR 是其各自权利人的商标。

本应用仅用于信息整理，不执行交易、管理资金，也不提供金融、投资、税务或法律建议。

## Español

### Descripción general

PnL Calendar es un calendario de rendimiento gratuito, sin publicidad, de solo
lectura y centrado en la privacidad local para usuarios de Interactive Brokers.
Organiza el rendimiento de la cuenta en vistas diarias, mensuales y anuales sin
enviar datos financieros a un servidor operado por el desarrollador.

La versión actual sincroniza el rendimiento desde Interactive Brokers y permite
revisar acciones estadounidenses e internacionales, ETF, opciones, futuros y
otras inversiones. Los resultados se consolidan en la divisa base de la cuenta.

### Funciones

- Calendario diario, resumen de doce meses y vista de varios años
- Ganancias y pérdidas netas, rentabilidad ponderada por tiempo, porcentaje de
  periodos positivos y detalles configurables
- Visualización de ganancias y pérdidas, rentabilidad o ambos datos
- Detalles opcionales de valoración a mercado, ganancias y pérdidas realizadas,
  flujos de caja, dividendos, intereses, comisiones y otros gastos cuando estén
  disponibles en el informe
- Sincronización automática opcional al abrir la app y sincronización manual
- Conexión directa y de solo lectura al IBKR Flex Web Service
- Credenciales Flex protegidas por el llavero de iOS
- Informes almacenados únicamente en el espacio privado de la app
- Sin backend del desarrollador, publicidad, SDK de analítica ni seguimiento entre apps
- Inglés, chino simplificado, español y japonés
- Temas claro y oscuro, colores configurables y primer día de la semana ajustable
- Interfaces nativas para iPhone y iPad
- Datos de demostración para explorar la app sin una cuenta de IBKR

### Uso de datos reales de Interactive Brokers

La sincronización requiere tu propio Activity Flex Query ID y Flex Token. En
IBKR Client Portal:

1. Abre **Reporting → Flex Queries**.
2. Crea o edita una **Activity Flex Query** con salida XML.
3. Activa **Change in NAV** y añade los campos necesarios para fechas, valores
   inicial y final, transferencias, depósitos y retiradas, valoración a mercado,
   ganancias y pérdidas realizadas, dividendos, intereses, comisiones, gastos y TWR.
4. Para mostrar las ganancias y pérdidas realizadas en modo MTM, activa también
   **Trades** con Trade Date, Level of Detail, FIFO P&L Realized, Currency y
   FX Rate to Base.
5. Guarda la consulta y copia su Query ID.
6. Abre **Flex Web Service Configuration**, activa el servicio, elige una fecha
   de caducidad y crea un Token. Deja vacía la restricción de IP para usarlo en
   un teléfono.
7. Introduce el Query ID y el Flex Token en PnL Calendar, valida y guarda.

Solo los campos incluidos en la consulta pueden aparecer en los detalles
opcionales. PnL Calendar solo lee informes: no puede realizar operaciones,
administrar fondos ni modificar la cuenta.

### Privacidad

La app se conecta directamente desde el dispositivo a Interactive Brokers
mediante HTTPS. Las credenciales se guardan en el llavero de iOS y los informes
descargados se almacenan en el entorno privado de la app. El desarrollador no
recibe ni recopila estos datos.

Consulta la [Política de privacidad](PRIVACY.md) completa.

### Desarrollo

Requisitos:

- Xcode 16 o posterior
- iOS/iPadOS 18.0 o posterior

Abre [`ios/PnLCalendar.xcodeproj`](ios/PnLCalendar.xcodeproj), selecciona un
simulador de iPhone o iPad y ejecuta el scheme `PnLCalendar`. Las compilaciones
del simulador deben permanecer firmadas para acceder al llavero.

El flujo de capturas deterministas para App Store está documentado en
[`ios/AppStoreScreenshots`](ios/AppStoreScreenshots/README.md).

El repositorio también contiene el prototipo web Node.js original para uso local:

```bash
cp .env.example .env
# Añade IBKR_FLEX_TOKEN e IBKR_FLEX_QUERY_ID a .env
npm start
```

Abre <http://127.0.0.1:4187>. Usa `npm test` para ejecutar las pruebas. No
publiques `.env` ni expongas el servidor local a una red que no sea de confianza.

### Estructura del repositorio

- `ios/` — app SwiftUI nativa, pruebas, recursos y capturas de App Store
- `lib/` — análisis Flex y lógica de periodos del prototipo web
- `public/` — interfaz del prototipo web
- `server.js` — servidor web local
- `PRIVACY.md` — política de privacidad pública de la app para iOS y iPadOS

### Aviso legal

PnL Calendar es una utilidad independiente de terceros y no está afiliada,
respaldada ni patrocinada por Interactive Brokers LLC ni sus filiales.
Interactive Brokers e IBKR son marcas de sus respectivos propietarios.

La app se ofrece únicamente para el registro informativo. No ejecuta operaciones,
administra fondos ni proporciona asesoramiento financiero, de inversión, fiscal
o jurídico.

## 日本語

### 概要

PnL Calendarは、Interactive Brokersユーザー向けの無料・広告なし・読み取り専用・
ローカルファーストのパフォーマンスカレンダーです。金融データを開発者運営の
サーバーへ送ることなく、口座の成績を日次・月次・年次でわかりやすく表示します。

現在のバージョンはInteractive Brokersからパフォーマンスを同期し、米国株を含む
株式、ETF、オプション、先物などの投資の振り返りに対応しています。結果は口座の
基準通貨で集計されます。

### 機能

- 日次カレンダー、12か月の一覧、複数年の年次サマリー
- 純損益、時間加重収益率、勝率、設定可能な期間別詳細
- 損益、収益率、または両方を表示
- レポートに項目が含まれる場合、時価評価損益、実現損益、資金フロー、配当、利息、
  手数料、その他の費用を表示
- App起動時の自動同期を任意で設定でき、手動同期にも対応
- IBKR Flex Web Serviceへの直接・読み取り専用接続
- Flex認証情報をiOSキーチェーンで保護
- 金融レポートのキャッシュをAppのプライベート領域にのみ保存
- 開発者運営のバックエンド、広告、解析SDK、App間トラッキングなし
- 英語、簡体字中国語、スペイン語、日本語に対応
- ライト／ダークテーマ、騰落色、週の開始日を設定可能
- iPhoneとiPad向けのネイティブレイアウト
- IBKR口座を接続せずに試せるデモデータを内蔵

### Interactive Brokersの実データを使用する

同期には、ご自身のActivity Flex Query IDとFlex Tokenが必要です。IBKR Client
Portalで次の設定を行います。

1. **Reporting → Flex Queries**を開きます。
2. XML出力の**Activity Flex Query**を作成または編集します。
3. **Change in NAV**を有効にし、日付、期首・期末価値、振替、入出金、時価評価損益、
   実現損益、配当、利息、手数料、費用、TWRに必要な項目を追加します。
4. MTMモードで実現損益も表示する場合は、**Trades**を有効にし、Trade Date、
   Level of Detail、FIFO P&L Realized、Currency、FX Rate to Baseを追加します。
5. Queryを保存し、Query IDをコピーします。
6. **Flex Web Service Configuration**を開き、サービスを有効にして有効期限を選び、
   Tokenを作成します。スマートフォンで使用する場合はIP制限を空欄にします。
7. PnL CalendarにQuery IDとFlex Tokenを入力し、検証して保存します。

Queryに含まれる項目だけが追加詳細に表示されます。PnL Calendarはレポートの読み取り
のみを行い、取引の発注、資金管理、口座設定の変更はできません。

### プライバシー

AppはデバイスからInteractive BrokersへHTTPSで直接接続します。認証情報はiOS
キーチェーンに保存され、ダウンロードしたレポートはAppのサンドボックスに保存され
ます。開発者がこれらのデータを受信または収集することはありません。

完全な[プライバシーポリシー](PRIVACY.md)をご覧ください。

### 開発

必要環境：

- Xcode 16以降
- iOS/iPadOS 18.0以降

[`ios/PnLCalendar.xcodeproj`](ios/PnLCalendar.xcodeproj)を開き、iPhoneまたはiPad
シミュレータを選択して`PnLCalendar` schemeを実行します。キーチェーンへアクセス
するため、シミュレータビルドも署名を維持する必要があります。

App Store用の固定データによるスクリーンショット手順は
[`ios/AppStoreScreenshots`](ios/AppStoreScreenshots/README.md)に記載しています。

リポジトリには、ローカルでセルフホストする元のNode.js Webプロトタイプも含まれます。

```bash
cp .env.example .env
# .envにIBKR_FLEX_TOKENとIBKR_FLEX_QUERY_IDを追加
npm start
```

<http://127.0.0.1:4187>を開きます。`npm test`でWebパーサーのテストを実行できます。
`.env`をコミットしたり、信頼できないネットワークへローカルサーバーを公開したり
しないでください。

### リポジトリ構成

- `ios/` — SwiftUIネイティブApp、テスト、ブランド素材、App Storeスクリーンショット
- `lib/` — WebプロトタイプのFlex解析と期間ロジック
- `public/` — Webプロトタイプのインターフェース
- `server.js` — ローカルWebプロトタイプサーバー
- `PRIVACY.md` — iOS／iPadOS Appの公開プライバシーポリシー

### 免責事項

PnL Calendarは独立したサードパーティ製Appであり、Interactive Brokers LLCおよび
その関連会社との提携、承認、スポンサー関係はありません。Interactive Brokersおよび
IBKRは、それぞれの権利者の商標です。

本Appは情報整理のみを目的としており、取引の実行、資金管理、金融・投資・税務・法務
に関する助言は行いません。
