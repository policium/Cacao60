# Cacao60%（開発中）
![PCB](https://raw.githubusercontent.com/policium/Cacao60/master/images/Cacao60_back.png)  
　DIYといったら英語配列という風潮（制約？）に一石投じるため、妥協無しで全部盛りの日本語配列モバイルキーボードを目指します。
### ～要件～
- **日本語配列**  
![KLE](https://raw.githubusercontent.com/policium/Cacao60/master/images/Cacao60_kle.jpg)  
　よくある60%の日本語配列キーボードはZ列を0.25U左にずらしてカーソルキーを右下に凸形に配置するスペースを確保しています。しかし慣れはあるもののZ列の微妙なズレがストレスになるのも事実。日本語配列でもカーソルキーを諦めてZ列を普通の配置にしたキーボードが幾つも出ています。硬派な向きには60%キーボードはカーソル無しが基本みたいです。  
　しかし私は軟弱なのでカーソルキーが無くなると日本語変換の為にFnキーやCtrlキーを押す事になり困ってしまいます。カーソルキーを凸ではなくViのHJKL方式で横に並べる事にして右下に何とか入れます。こうすることで人差し指で←、小指で→に最短距離でアクセス出来るため凸配列より日本語変換が捗ることを狙っています。  
　今回はこの配列を日本語キーキャップの数少ない選択肢の一つMajestouch MINILA Air用と108キー用のABSキーキャップを混ぜて利用します。やはり普通の配列はDSA系のフラットプロファイルではなくOEM系のスカルプチャードプロファイルが合うと思います。FILCO様お願いなのでMINILA Air用のキーキャップを暫く販売しておいてください。  
　選択肢としてHyperXもありますが1キー犠牲になるため悩みました。入手性はこちらの方がいいのかもしれません。光りますしおすし。  
　この手が使えなくなると日本語キーキャップの選択肢が少ないこともあり、PBTのブランクキーキャップに昇華印刷かUVプリントすることになります。ただOEMプロファイルでMINILA系の日本語配列にできるブランクキーキャップがどこに売っているのか・・・誰か教えてください。XDAのブランクキーキャップはいい感じにはまります。本命です。

- **GH60互換**  
　ロープロファイル（プレートとケースの端がツライチになるタイプ）のケースならフィットすると思います。
高級路線ではないので、ケースの選びやすさを大事にします。音の良さは犠牲にしますが、何らか対策したいと思います。

- **Kailh Choc V2**  
　[これ](https://www.kailhswitch.com/mechanical-keyboard-switches/key-switches/kailh-low-profile-switch-choc-v2.html)はKailhの薄型スイッチですが、ステムが普通のスイッチと同じ十字のタイプになります。キーキャップの自由度が高い事が日本語配列を実現するにあたって重要になります。一部で同じタイプ（オリジナル）のCherry MX Low Profile RGB Redスイッチも手に入る様になってきていますが、リニアタイプのみの展開になっており、青軸、茶軸、赤軸が選べるのも大きいです。  
　しかし現状では対応スタビライザーが存在しない上に薄型故にキーキャップを選ぶのが問題です。Choc V1用のスタビライザーは存在しますがトラベルが短いのとトッププレート必須なのでそのままでは難しいです。折角なのでストロークを犠牲にしないでスタビライザーを付ける方法を考えてみます。寸法を見ていると普通はプレートに付けるCostarスタビライザーをPCBに付ける事で対応出来そうな気がします。薄型スイッチを利用する場合、キーキャップとプレートが干渉しないようにフローティングタイプというスカート部分が短いキーキャップを使うのが基本です。ただし著しくキーキャップの選択肢を狭めるためプレートは無しの方向です。一部キーキャップでスイッチと干渉があると思うのでスイッチを削って乗り越えたいです。（手元ではXDA、DSAは行けそうでした。MajestouchのABSキーキャップは干渉しました。）

- **Bluetooth（nRF52840）**  
　モバイルしたいので無線は欲しいです。ファームウェアは[QMK](https://qmk.fm/)フォークの何れかを採用しようと思いますが、[ZMK](https://zmkfirmware.dev/)も気になっています。

- **LiPo電池充電機能**  
　HHKB、MINILAと差別化したいため充電機能付きとします。1回の充電で1週間程度は使いたいところ。

- **バックライト、アンダーグロー両対応（RGB）**  
![PCB](https://raw.githubusercontent.com/policium/Cacao60/master/images/Cacao60_front.png)  
　USB接続時はとりあえず全部盛りRGBで光らせたいです。全部光らせるとUSBの電力容量を超えそうなのでSK6812より消費が少ないSK6805を採用します。LEDが小さい為、スイッチのLED窓にギリギリ収まります。QMKのRGB Matrixにも対応したいです。対応ファームはどうするか？
