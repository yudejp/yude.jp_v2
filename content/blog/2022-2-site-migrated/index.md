+++
title="サイトを移行しました。"
description="yude.jp を構成するフレームワークを変更しました。"
date=2022-02-12

[taxonomies]
tags = ["zola"]
categories = ["technology"]
+++

2021年3月頃から yude.jp では Next.js + Tailwind CSS でサイトを構成してきましたが、機能を縮小するにあたりこの構成は過剰だったことと、Node.js のエコシステムに疲れてしまったことから、今回 Rust 製の SSG フレームワークである Zola に移行しました。\
現在の構成は以下のとおりです。

* Zola のテーマ: [zerm](https://github.com/ejmg/zerm)
* ~~Zola のビルド: GitHub Actions~~
* Zola のビルド, デプロイ: [Cloudflare Pages](https://pages.cloudflare.com/)

~~当初、Zola のビルドとデプロイを両方とも Cloudflare Pages で行おうとしていましたが、zerm のテーマを使用した状態ではどうしてもビルドが通らず (`styles.css` が見つからない 等の前代未聞のエラーが発生...)、仕方なく GitHub Actions で gh-pages ブランチにビルドしたものを Cloudflare Pages にアップロードしています。ええ...~~
➝ [修正しました。](https://github.com/yudejp/yude.jp_v2/commit/3d45db22f91276112bca2ed1eeab27c4c16d7de1)

よろしゅう。