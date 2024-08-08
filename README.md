# quasar-boilerplate

- 한국어 설정
- breakpoint 활성화
- prettier 설정
- 구글 폰트 설정 (Noto Sans KR)

quasar.config
```js
framework: {
      ...
      cssAddon: true,
      lang: 'ko-KR',
}
```

.prettierrc
```
{
  "singleQuote": true,
  "semi": true,
  "tabWidth": 2,
  "trailingComma": "all",
  "printWidth": 80,
  "bracketSpacing": true,
  "arrowParens": "avoid"
}
```