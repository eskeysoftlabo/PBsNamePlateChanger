# Store listing copy

Text for the Bethesda.net / ZOS Console AddOn Uploader entry. Plain text, no markdown —
paste as-is. The **name** field is what the in-game add-on browser shows, so it must read
`PB's NamePlateChanger` there; `## Title` in the manifest does not reach that screen.

---

## Overview (JP)

キャラクターの頭上に表示される名前の文字サイズを変更します。小さすぎて読めない、大きすぎて
視界を塞ぐ、どちらも設定パネルのスライダーひとつで調整できます。書体と縁取りも変更可能です。

## Overview (EN)

Changes the size of the names displayed above characters' heads. Too small to read, or big
enough to block your view — either way it is one slider in the settings panel. The typeface
and outline can be changed too.

---

## Description (JP)

キャラクターの頭上に出る名前（ネームプレート）のフォントを調整するアドオンです。

■ できること

・文字サイズの変更（10〜72）
　これが中核機能です。ロード画面を跨いでも維持されます。
・書体の変更
　ゲームが持っている書体から5種類。
・縁取りの変更
　影・縁取りなど、背景から文字を浮き立たせる方法。

■ 設定

設定 → アドオン設定 → PB's NamePlateChanger（LibHarvensAddonSettings が必要です）

チャットコマンドでも操作できます。
　/pbfont            コマンド一覧
　/pbfont size 32    文字サイズを指定
　/pbfont safe       サイズだけ残し、書体と縁取りをゲーム既定に戻す
　/pbfont off        ゲーム本来のフォントに戻す
　/pbfont status     現在の状態を表示

■ できないこと（重要）

頭上の名前はゲーム本体が描画しているため、アドオンからは以下を変更できません。

・称号、キャラクター名、＜ギルド名＞の並び順
・行の分け方、センタリング
・文字の色

称号行とギルド行を表示するかどうかは、ゲーム本体の設定（設定 → ネームプレート →
「称号を表示」「ギルドを表示」）で切り替えられます。

■ コンソールでの注意

コンソールのアドオンは 100MB のメモリを全アドオンで共有しています。まだ読み込まれていない
書体を設定するとクライアントがそのフォントを構築し、その負荷がこのメモリに計上されるため、
アドオンが停止することがあります。

そのため、

・選択できる書体は、UIが既に読み込んでいる5種類のみにしてあります
・書体と縁取りはログイン時に一度だけ適用されます。ロード画面を挟むとゲーム既定の書体に
　戻りますが、指定した文字サイズは維持されます
・設定パネルの「ロード後も書体を維持する」をオンにすると毎回適用しますが、
　コンソールでは動作が不安定になります（PCでは問題ありません）

文字サイズの変更にはこの負荷がかからないため、常に安全です。

■ 元に戻す

アドオンが初めてフォントを書き換える前に、ゲーム本来の値を保存します。
「ネームタグのフォントを変更」をオフにするか /pbfont off で、いつでも完全に元へ戻せます。

---

## Description (EN)

Adjusts the font of the names displayed above characters' heads.

■ What it does

- Text size, 10 to 72. This is the core feature, and it survives loading screens.
- Typeface: five of the game's own faces.
- Outline: shadow, outline and so on, for readability against bright scenery.

■ Settings

Settings → Add-On Settings → PB's NamePlateChanger (requires LibHarvensAddonSettings)

Chat commands are available too:
  /pbfont            list the commands
  /pbfont size 32    set the text size
  /pbfont safe       keep the size, put typeface and outline back to the game's own
  /pbfont off        restore the game's own font
  /pbfont status     show the current state

■ What it cannot do

The game engine draws the overhead name itself, so an add-on cannot change:

- the order of the title, character name and <guild> lines
- how they are split across lines, or their centring
- the text colour

Whether the title line and the guild line appear at all is the game's own setting:
Settings → Nameplates → Show Title / Show Guild.

■ Note for console

Console add-ons share a 100 MB memory pool. Setting a typeface the client has not loaded
makes it build that font, and the cost is billed to that pool — which can take add-ons down.

So:

- Only the five faces the UI already has loaded are offered.
- The typeface and outline are applied once per session. After a loading screen the game's
  own face comes back, with your text size still applied.
- "Keep typeface after loading screens" re-applies everything every time. It is unstable on
  console; on PC it is fine.

Changing the text size does not carry this cost and is always safe.

■ Restoring

The game's own font is saved before the add-on ever writes one. Turn "Custom nametag font"
off, or use /pbfont off, to put it back exactly as it was.

---

## Disclaimer (both)

This Add-On is not created by, affiliated with or sponsored by ZeniMax Media Inc. or its
affiliates. The Elder Scrolls and related logos are registered trademarks or trademarks of
ZeniMax Media Inc. in the United States and/or other countries. All rights reserved.
