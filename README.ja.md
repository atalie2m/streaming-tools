# streaming-tools

OBSで使う配信用ウィジェット集です。

## 時計ウィジェット

`widgets/clock/index.html` をOBSのブラウザソースとして読み込んでください。背景は透過で、ベージュ基調の時計プレートだけが表示されます。推奨サイズは `860 x 545` 前後ですが、ブラウザソースのサイズに合わせて拡大縮小されます。

読み込みURLの例:

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html
```

### URLパラメータ

| パラメータ | 初期値 | 説明 |
| --- | --- | --- |
| `tz` | `Asia/Tokyo` | IANAタイムゾーン。例: `Asia/Tokyo`, `America/Los_Angeles`。 |
| `seconds` | `1` | `seconds=0` にすると秒表示を非表示にします。 |
| `panel` |  | プレートの色を16進カラーで上書きします。`#` は付けても省略しても構いません。 |
| `light` |  | プレートのハイライト色を上書きします。 |
| `shadow` |  | プレート下部の影色を上書きします。 |
| `ink` |  | 文字色を上書きします。 |
| `saturday` |  | 土曜日の曜日表示色を上書きします。 |
| `sunday` |  | 日曜日の曜日表示色を上書きします。 |
| `holiday` |  | 日本の祝日の曜日表示色を上書きします。 |

### 例

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?seconds=0
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?panel=f1dfc4&light=fff2db&shadow=d2ad7a
```

曜日表示は、平日は黒、土曜は青、日曜は赤になります。日本の祝日の場合は祝日色に切り替わり、曜日の後ろに祝日名を表示します。例: `(WED) 昭和の日`。

祝日データは2026年と2027年について内閣府公表の祝日・休日を内蔵しています。それ以外の年は祝日法ベースの計算で判定します。
