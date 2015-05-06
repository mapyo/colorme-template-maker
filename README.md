colorme-template-maker
------

[こちら](http://shop-pro.jp/)のテンプレ作成をしやすくするやつです。


## Requirements

```
brew install node
```


## Installation

```
git clone git@github.com:mapyo/colorme-template-maker.git
cd colorme-template-maker
npm install coffee-script -g
mkdir -p assets/css
mkdir -p assets/templates
```

※css,templatesフォルダはテンプレを管理しているフォルダとシンボリックを貼るとよいです。

## Setting of yml file

```
cp config/local.yml.sample config/local.yml
```

#### PHPSESSID

1. [管理画面](https://admin.shop-pro.jp/)にログイン
2. Chrome Developer Toolsを開いてResources→Cookies→admin.shop-pro.jpのPHPSESSID(Domainがadmin.shop-pro.jp)をコピー
3. local.ymlのPHPSESSIDの部分を変更

#### tmpl_uid

1. [デザイン設定画面](http://admin.shop-pro.jp/?mode=design_tmpl_lst)を開く
2. 編集したいテンプレを利用中のテンプレートにする
3. 利用中のテンプレートのデザイン編集ボタンをクリック
4. `http://admin.shop-pro.jp/?mode=design_tmpl_sel&tmpl_uid=xx`の、`xx`の部分の番号をコピー
5. local.ymlのtmpl_uidの部分を変更


## Usage

#### テンプレをサイトから取ってきたい時

```
./pull-template
```
assets以下に各種cssやフォルダが作成されます

#### ローカルの内容をサイトに反映させたい時

```
./push-template
```

## その他

自己責任で使って下さい。
