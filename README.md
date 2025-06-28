# test-render-image

:ledger: Testing rendering image

## How it works? 🚀

What happen at webserver when I will hide image by:

```css
display: none !important;
visibility: hidden !important;
opacity: 0 !important;
```

and

```
position: absolute;
left: -9999px;
top: -9999px;
```

... in my `nginx` I see 2 requests:

```
127.0.0.1 - - [04/Feb/2016:09:36:22 +0100] "GET /test-render-image/ HTTP/1.1" 200 735 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_3) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/48.0.2564.97 Safari/537.36" "-"
127.0.0.1 - - [04/Feb/2016:09:36:22 +0100] "GET /test-render-image/images/test-image.jpeg HTTP/1.1" 200 17904 "http://localhost/test-render-image/" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_3) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/48.0.2564.97 Safari/537.36" "-"
```
