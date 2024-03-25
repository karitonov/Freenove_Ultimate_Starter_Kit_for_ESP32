# Prepare

ESP32は、エスプレシフが発売したWi-Fi内蔵マイクロコントロールユニットで、強力な特性と豊富な周辺機能を備えています。通常のSingle Chip Micyoco(SCM)チップとして設計・研究することも、インターネットに接続してInternet of Thingsデバイスとして使用することもできます。

ESP32はC/C++言語でもmicropython言語でも開発できる。このチュートリアルでは、micropythonを使用します。micropythonはPythonと同じくらい簡単に学ぶことができ、コードも少ないので初心者に最適です。さらに、ESP32のコードは完全にオープンソースなので、初心者はスマートカーテン、扇風機、ランプ、時計などのIoTスマート家庭用製品の開発・設計方法をすぐに学ぶことができます。

各プロジェクトは、コンポーネントリスト、コンポーネント知識、回路、コードの4つのパートに分かれています。コンポーネントリストは、実験のための材料をより迅速に準備するのに役立ちます。コンポーネント知識は新しい電子モジュールやコンポーネントを素早く理解するのに役立ち、回路は回路の動作原理を理解するのに役立ちます。また、Codeを使えば、ESP32とそのアクセサリキットの使い方を簡単にマスターできます。このチュートリアルのすべてのプロジェクトを終了した後、これらのコンポーネントやモジュールを使用して、スマートハウス、スマートカー、ロボットなどの製品を作り、あなたの創造的なアイデアをプロトタイプや新しく革新的な製品に変えることもできます。

## ESP32-WROVER

ESP32-WROVERは、PCBオンボードアンテナとIPEXアンテナの2種類のアンテナパッケージを発売しました。PCBオンボードアンテナはチップモジュール自体に内蔵されたアンテナで、持ち運びや設計に便利です。IPEXアンテナは、チップモジュール自体の内蔵アンテナから派生した金属アンテナで、モジュールの信号を増強するために使用されます。

このチュートリアルでは、PCBオンボードアンテナパッケージをベースにESP32-WROVERを設計します。

ESP32-WROVERのハードウェア・インターフェースは以下のように分布している：

左右の画像を見比べてください。ESP32-WROVERを理解しやすくするために、ESP32-WROVER上のリソースを異なる色で囲みました。

## Extension board of the ESP32-WROVER

また、提供された回路図に従って、ESP32をより簡単に使用できるように、拡張ボードも設計しています。以下はその写真です。このチュートリアルのすべてのプロジェクトは、このESP32-WROVERを使用しています。

ESP32-WROVERのハードウェアインターフェイスは以下の通りです：

ESP32-WROVERのリソースを理解しやすくするために、ESP32-WROVERのリソースを色分けしています。

ESP32において、GPIOは周辺回路を制御するためのインターフェースです。初心者は各GPIOの機能を覚える必要がある。以下では、ESP32-WROVER開発ボードのGPIOリソースを紹介する。

この後、ESP32-WROVERへの電源供給には、デフォルトではUSBケーブルしか使いません。

チュートリアル全体では、ESP32-WROVERへの給電にT拡張は使いません。そのため、拡張ボードの5Vと3.3V（EXT 3.3Vを含む）はESP32-WROVERから供給されます。拡張ボードのDCジャックをESP32-WROVERの電源に使うこともできる。その場合、拡張ボードの5VとEXT 3.3Vは外部電源から供給されます。

詳しくはこちらをご覧ください：

[https://www.espressif.com/sites/default/files/documentation/esp32-wrover_datasheet_en.pdf](https://www.espressif.com/sites/default/files/documentation/esp32-wrover_datasheet_en.pdf)

# Chapter 0 Ready (Important)

プロジェクトの構築を開始する前に、飛ばしてはならないほど重要ないくつかの準備をする必要があります。

## 0.1 Installing Thonny (Important)

Thonnyはフリーのオープンソースソフトウェアプラットフォームで、コンパクトなサイズ、シンプルなインターフェース、シンプルな操作、豊富な機能を備えており、初心者向けのPython IDEです。このチュートリアルでは、このIDEを使ってESP32を開発します。

ThonnyはWindows、Mac OS、Linuxなど様々なOSをサポートしています。

### Downloading Thonny

* [https://thonny.org/](https://thonny.org/)
* [https://github.com/thonny/thonny/releases/](https://github.com/thonny/thonny/releases/)

## 0.2 Basic Configuration of Thonny

## 0.3 Installing CH340 (Important)

ESP32はCH340を使ってコードをダウンロードする。そのため、使用する前にCH340ドライバをコンピュータにインストールする必要がある。

## 0.4 Burning Micropython Firmware (Important)
