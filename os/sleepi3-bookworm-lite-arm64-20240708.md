# sleepi3-bookworm-lite-arm64-20240708
Raspberry Pi OS (64-bit) Lite July 4th 2024 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[sleepi3-bookworm-lite-arm64-20240708.img.xz](https://mechatrax.com/data/sleepi3/sleepi3-bookworm-lite-arm64-20240708.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
6e0a6d0278632af7c44f2680005e7161623063cbd501eb6dd70cb4b27b35548d
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
  * パッケージを 20240708 時点の最新版に更新

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
