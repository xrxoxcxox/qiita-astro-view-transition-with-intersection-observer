---
title: "unicorn.studioで作ったものをサイトに載せる"
coverImage: "https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-user-contents.imgix.net%2Fhttps%253A%252F%252Fcdn.qiita.com%252Fassets%252Fpublic%252Fadvent-calendar-ogp-background-7940cd1c8db80a7ec40711d90f43539e.jpg%3Fixlib%3Drb-4.0.0%26w%3D1200%26blend64%3DaHR0cHM6Ly9xaWl0YS11c2VyLXByb2ZpbGUtaW1hZ2VzLmltZ2l4Lm5ldC9odHRwcyUzQSUyRiUyRnFpaXRhLWltYWdlLXN0b3JlLnMzLmFwLW5vcnRoZWFzdC0xLmFtYXpvbmF3cy5jb20lMkYwJTJGMjE0Njc3JTJGcHJvZmlsZS1pbWFnZXMlMkYxNjk0NTkyNDA1P2l4bGliPXJiLTQuMC4wJmFyPTElM0ExJmZpdD1jcm9wJm1hc2s9ZWxsaXBzZSZmbT1wbmczMiZzPWUyZWUzYzU5YWI3YmU2YTNhNzdhN2RhNTg1YWJlN2Jk%26blend-x%3D120%26blend-y%3D462%26blend-w%3D90%26blend-h%3D90%26blend-mode%3Dnormal%26mark64%3DaHR0cHM6Ly9xaWl0YS1vcmdhbml6YXRpb24taW1hZ2VzLmltZ2l4Lm5ldC9odHRwcyUzQSUyRiUyRnMzLWFwLW5vcnRoZWFzdC0xLmFtYXpvbmF3cy5jb20lMkZxaWl0YS1vcmdhbml6YXRpb24taW1hZ2UlMkY4YTMwMDIzOGRmNzg0YzlmYzRlMDY4M2JjMjE0MWIzYzhjNWI3YjU4JTJGb3JpZ2luYWwuanBnJTNGMTYzODI4NjQ3Mz9peGxpYj1yYi00LjAuMCZ3PTQ0Jmg9NDQmZml0PWNyb3AmbWFzaz1jb3JuZXJzJmNvcm5lci1yYWRpdXM9OCZib3JkZXI9MiUyQ0ZGRkZGRiZmbT1wbmczMiZzPWEyMDY4NDQ1YTUxOGRmZmQzM2U4MzQ1ZTFkYzkwMzc1%26mark-x%3D186%26mark-y%3D515%26mark-w%3D40%26mark-h%3D40%26s%3D098c4c89f3864df165807eaa75f5a2cc?ixlib=rb-4.0.0&w=1200&fm=jpg&mark64=aHR0cHM6Ly9xaWl0YS11c2VyLWNvbnRlbnRzLmltZ2l4Lm5ldC9-dGV4dD9peGxpYj1yYi00LjAuMCZ3PTk2MCZoPTMyNCZ0eHQ9dW5pY29ybi5zdHVkaW8lRTMlODElQTclRTQlQkQlOUMlRTMlODElQTMlRTMlODElOUYlRTMlODIlODIlRTMlODElQUUlRTMlODIlOTIlRTMlODIlQjUlRTMlODIlQTQlRTMlODMlODglRTMlODElQUIlRTglQkMlODklRTMlODElOUIlRTMlODIlOEImdHh0LWFsaWduPWxlZnQlMkN0b3AmdHh0LWNvbG9yPSUyMzNBM0MzQyZ0eHQtZm9udD1IaXJhZ2lubyUyMFNhbnMlMjBXNiZ0eHQtc2l6ZT01NiZ0eHQtcGFkPTAmcz01NDk5YTExZGJkOGM5YWExN2Y2NDQ0ZmE5MzkwY2NkZg&mark-x=120&mark-y=112&blend64=aHR0cHM6Ly9xaWl0YS11c2VyLWNvbnRlbnRzLmltZ2l4Lm5ldC9-dGV4dD9peGxpYj1yYi00LjAuMCZ3PTgzOCZoPTU4JnR4dD0lNDB4cnhveGN4b3gmdHh0LWNvbG9yPSUyMzNBM0MzQyZ0eHQtZm9udD1IaXJhZ2lubyUyMFNhbnMlMjBXNiZ0eHQtc2l6ZT0zNiZ0eHQtcGFkPTAmcz1mMzhlMDNlODEyZjRjNjYxNjRhMzFmYmU5MmIwYWZmYw&blend-x=242&blend-y=454&blend-w=838&blend-h=46&blend-fit=crop&blend-crop=left%2Cbottom&blend-mode=normal&txt64=UWlpdGHmoKrlvI_kvJrnpL4&txt-x=242&txt-y=539&txt-width=838&txt-clip=end%2Cellipsis&txt-color=%233A3C3C&txt-font=Hiragino%20Sans%20W6&txt-size=28&s=2d64b961ee3b12e9014988e2edbe41f6"
---

## この記事の概要

[unicorn.studio](https://www.unicorn.studio/)というツールがあります。

ノーコードでWebGLを扱えて、インタラクティブなエフェクトやモーションを簡単に作ることができます。

適当に触っていても面白い表現が作れて、非常に魅力的なツールです。

ただ、作ったものを実際にサイト上に載せるのにはやや苦労しました（特にReactでは）。
というわけでコピー＆ペーストにて動かせるように記事にします。

## unicorn.studioの特徴

いきなり実装の仕方から入るのも不親切なので、少しだけunicorn.studioの特徴を記載します。

### エフェクトが豊富

- 標準エフェクト
  - ディストーション、ブラー、ライトなど、様々な種類のエフェクトが搭載されている
  - 公式サイトでは「35+ effects」という表記ながら、実際に数えたら50あった
    - 徐々に増えているのかもしれない
- 自分で書くカスタムエフェクト
  - シェーダーが書ける場合、自分で書くことも可能

### モーションやインタラクションをつけるのが簡単

- 登場、スクロール、マウスオーバーをトリガーにしたモーション
- マウスの動きに追従した変化

### この手のライブラリの中では軽い

- gzipped時で36kB
- 役割や機能の豊富さが違うので単純比較すべきではないものの、参考程度にthree.jsは167.9kB、p5.jsは244.6kB

### FramerとWebflowなどでの利用が簡単

- ノーコードな技術スタック（？）に焦点を当てていそう
- それもあってか自前で実装するサイトへのサポートはやや手薄な印象

### 画像や動画としての書き出しも可能

- サイズや拡張子、フレームレートなどが選択できる
- インタラクティブ性はなくなってしまうものの、手軽に使えるという意味では嬉しい機能

## 下準備

エディタ画面右上の`Export`から`Embed`を開くと`Project ID`があります。
コードの中でこれを使うのでコピーしておきます。

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/364bdcd7-dbee-4717-9bcb-5d4a0cc74cfc.png)


## 実装

素のHTML上で使用する場合と、Reactで使用する場合の両方を記載します。

### HTML

最低限ならこの3ファイルで良いです。
（`main.js`の中身も1行しかないので直接HTMLに書いても良いですが、さすがにそうはしないだろう、ということで3ファイル用意しています。）

```sh:ファイル構成
.
├── index.html
├── main.js
└── style.css
```

HTMLは以下

```html:index.html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
    <script
      src="https://cdn.unicorn.studio/v1.3.2/unicornStudio.umd.js"
      defer
    ></script>
    <script src="main.js" defer></script>
  </head>
  <body>
    <div
      data-us-project="YOUR_PROJECT_ID"
      style="width: 100%; height: 100%"
    ></div>
    <!-- お好きな内容 -->
  </body>
</html>
```

```javascript:main.js
UnicornStudio.init();
```

CSSはお好きに書いてもらえれば大丈夫です。

重要なのは以下の3点です。

1. CDNにあるunicron.studioのコードを使う
1. `data-us-project`にProject IDを記載する
1. `init()`する

### React

Viteの`create-vite`でReactプロジェクトを作ったという前提での記載です。

```sh:ファイル構成
.
├── README.md
├── index.html
├── package-lock.json
├── package.json
├── public
├── src
│   ├── App.css
│   ├── App.tsx
│   ├── components
│   │   └── UnicornEmbed.tsx
│   ├── hooks
│   │   └── useUnicornStudio.ts
│   ├── index.css
│   ├── main.tsx
│   └── vite-env.d.ts
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

`projectId`を渡して描画できるコンポーネントを作成します。

```tsx:src/components/UnicornEmbed.tsx
import { useRef } from "react";

interface UnicornEmbedProps {
  projectId: string;
}

export const UnicornEmbed: React.FC<UnicornEmbedProps> = ({ projectId }) => {
  const containerRef = useRef<HTMLDivElement>(null);


  return (
    <div
      ref={containerRef}
      data-us-project={projectId}
      style={{ width: "100%", height: "100%" }}
    />
  );
};
```

1ページで複数回`UnicornEmbed`を使うかもしれないと考えて、hookを作成します。

```tsx:src/hooks/useUnicornStudio.ts
import { useEffect } from "react";

declare global {
  interface Window {
    UnicornStudio: {
      init(): Promise<void>;
      destroy(): void;
    };
  }
}

let isInitialized = false;

export const useUnicornStudio = () => {
  useEffect(() => {
    if (isInitialized) return;

    if (!window.UnicornStudio) {
      window.UnicornStudio = {
        init: () => Promise.resolve(),
        destroy: () => {},
      };

      const script = document.createElement("script");
      script.src = "https://cdn.unicorn.studio/v1.3.2/unicornStudio.umd.js";
      script.onload = () => {
        window.UnicornStudio.init();
        isInitialized = true;
      };
      document.head.appendChild(script);
    }

    return () => {
      if (isInitialized) {
        window.UnicornStudio.destroy();
        isInitialized = false;
      }
    };
  }, []);
};
```

あとは、今作った2つの機構を使えば大丈夫です。

```tsx:src/App.tsx
import "./App.css";
import { UnicornEmbed } from "./components/UnicornEmbed";
import { useUnicornStudio } from "./hooks/useUnicornStudio";

function App() {
  useUnicornStudio();
  return (
    <>
      <UnicornEmbed projectId="YOUR_PROJECT_ID" />
      {/* お好きな内容 */}
    </>
  );
}

export default App;
```
