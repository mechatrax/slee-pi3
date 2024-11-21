# sleepi3-bookworm-lite-arm64-20241121
Raspberry Pi OS (64-bit) Lite November 19th 2024 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[sleepi3-bookworm-lite-arm64-20241121.img.xz](https://mechatrax.com/data/slee-pi3/sleepi3-bookworm-lite-arm64-20241121.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
cff734fdb6fde0c9f1ec6000f96beb78679e5c1e278a48c4594f6da13871301a
```

## 変更内容
Raspberry Pi OS からの変更内容は次のとおりです。
  * slee-Pi3 用パッケージをインストール
  * I2C を有効化
  * slee-Pi3 の誤動作を防ぐために core_freq=250 を設定
  * シリアルコンソールを有効化
  * rootfs で ext4 の 64bit オプションを有効化
  * ハードウェアウォッチドッグタイマの監視に systemd を使用
  * APT::Periodic の無効化
  * WiFi の地域設定を日本（JP）に設定
  * パッケージを 20241121 時点の最新版に更新

## インストールパッケージ
  * 独自パッケージ  
    sleepi3-utils  
    sleepi3-monitor  
    sleepi3-firmware  
    python-sleepi  
    mechatrax-archive-keyring

## 削除パッケージ  
  * 常駐プロセス削減のため削除  
    triggerhappy  
    udisks2  

  * 独自パッケージと競合のため削除  
    fake-hwclock
