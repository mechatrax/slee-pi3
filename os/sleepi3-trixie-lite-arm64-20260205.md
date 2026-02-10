# sleepi3-trixie-lite-arm64-20260205
Raspberry Pi OS (64-bit) Lite December 4th 2025 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[sleepi3-trixie-lite-arm64-20260205.img.xz](https://mechatrax.com/data/slee-pi3/sleepi3-trixie-lite-arm64-20260205.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
4abf20b097eb6375c69d8d7873f36ade33adeba3836de1d63f835cc81e01e711
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
  * パッケージを 20260205 時点の最新版に更新

## インストールパッケージ
  * 独自パッケージ  
    sleepi3-utils  
    sleepi3-monitor  
    sleepi3-firmware  
    sleepi3-dkms  
    python-sleepi  
    mechatrax-archive-keyring

## 削除パッケージ  
  * 常駐プロセス削減のため削除  
    udisks2  

  * 独自パッケージと競合のため削除  
    fake-hwclock
