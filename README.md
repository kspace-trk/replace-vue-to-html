# Vue to html
プロジェクトの中にある`.vue`という拡張子がつく全てのファイルのなかから、<template>タグで囲われている中身のみを取り出して、同様のファイル名にした.htmlファイルに書き出します。

```
find . -type f -name "*.vue" -exec sh -c 'sed -n "/<template>/,/<\/template>/p" "{}" > "html/$(basename "{}" .vue).html"' \;
```

## なににつかうの？
Webサイトのコンテンツを翻訳業者様に入稿するときなどに役に立ちます。
