# Claude Theme for VSCode

Claude のカラーパレットにインスパイアされた、目に優しい VSCode テーマ。

3 バリアント収録:

- **Claude Dark** — 暖色系ダーク。引き締まったコントラスト。
- **Claude Dark Soft** — Dark をさらに低彩度化。長時間作業向け。
- **Claude Light** — Claude.ai のクリーム背景を再現。日中作業向け。

## カラーフィロソフィー

- Claude シグネチャの **コーラルオレンジ (#D97757)** をアクセントに統一。
- 暖色寄りのニュートラル (cream / warm gray) を基調にして、目への刺激を抑える。
- シンタックスは低彩度パレットで揃え、**読みやすさ優先**でハイライトの差分を整理。
- セージグリーン (string)、アンバー (number/function)、テラコッタ (keyword) の組み合わせで色相を分散しつつ、互いに干渉しない明度設計。

## 主要カラーチップ

### Dark
| 用途 | HEX |
|---|---|
| Background | `#1F1E1D` |
| Foreground | `#E8E6DC` |
| Accent | `#D97757` |
| Keyword | `#C9907A` |
| String | `#A8B89A` |
| Function | `#E0B084` |
| Number | `#D4A574` |
| Comment | `#6B6A65` (italic) |

### Light
| 用途 | HEX |
|---|---|
| Background | `#F5F4EE` |
| Foreground | `#2A2826` |
| Accent | `#C15F3C` |
| Keyword | `#B5532E` |
| String | `#5C7A4E` |
| Function | `#8B5A2B` |
| Number | `#8B5A2B` |
| Comment | `#8A887E` (italic) |

## インストール

### ローカルインストール (開発中)

```bash
# このリポジトリを ~/.vscode/extensions/ にシンボリックリンク
ln -s "$(pwd)" ~/.vscode/extensions/claude-theme
```

VSCode を再起動し、`Cmd+K Cmd+T` でテーマピッカーを開いて **Claude Dark** / **Claude Dark Soft** / **Claude Light** を選択。

### VSIX パッケージ作成

```bash
npm install -g @vscode/vsce
vsce package
code --install-extension claude-theme-0.1.0.vsix
```

## カスタマイズ

`settings.json` で個別 token を上書き可能:

```json
{
  "editor.tokenColorCustomizations": {
    "[Claude Dark]": {
      "comments": "#7A7973"
    }
  }
}
```

## ライセンス

MIT
