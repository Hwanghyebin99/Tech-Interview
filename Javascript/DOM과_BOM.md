# ๐DOM๊ณผ BOM
## ๋ชฉ์ฐจ
  1. [๋ฌธ์ ๊ฐ์ฒด ๋ชจ๋ธ(DOM)](#DOM-(Document-Object-Model))
  2. [๋ธ๋ผ์ฐ์  ๊ฐ์ฒด ๋ชจ๋ธ(BOM)](#BOM-(Browser-Object-Model))

## DOM (Document Object Model)
### ๋ฌธ์ ๊ฐ์ฒด ๋ชจ๋ธ(DOM)
DOM์ XML, HTML ๋ฌธ์์ ์ ๊ทผํ๊ธฐ ์ํ ์ธํฐํ์ด์ค์ด๋ฉฐ ๊ณ์ธต ๊ตฌ์กฐ๋ก ํํ๋๋ค.  
DOM์ ์น ํ์ด์ง๋ฅผ ๊ฐ์ฒด๋ก ํํํด์ฃผ๋ฉฐ, ์๋ฐ์คํฌ๋ฆฝํธ์ ๊ฐ์ ์คํฌ๋ฆฝํ ์ธ์ด๋ก ์น ํ์ด์ง์ ์ ๊ทผํ  ์ ์๋ ๋ฐฉ๋ฒ์ ์ ๊ณตํ์ฌ ๊ตฌ์กฐ, ์คํ์ผ, ๋ด์ฉ์ ๋ณ๊ฒฝํ  ์ ์๋๋ก ๋์์ค๋ค.

์๋ฅผ ๋ค์ด ์๋ฐ์คํฌ๋ฆฝํธ์์ HTML์ \<h1> element๋ค์ ์ ๊ทผ์ ํ๋ ๋ฐฉ๋ฒ์ ๋ค์๊ณผ ๊ฐ๋ค.
```Javasript
var headElement = document.getElementsByTagName('h1');
```
DOM tree ๊ตฌ์กฐ์์ ์์ฃผ ์ฌ์ฉ๋๋ ๋ธ๋๋ ๋ค์๊ณผ ๊ฐ๋ค
* Document: ํธ๋ฆฌ์ ์ต์๋จ
* Element: TAG
* Attribute: element์ ์์ฑ
* Text: ํธ๋ฆฌ์ ์ต์ข๋จ
## BOM (Browser Object Model)
### ๋ธ๋ผ์ฐ์  ๊ฐ์ฒด ๋ชจ๋ธ(BOM)
BOM์ ์น ๋ธ๋ผ์ฐ์  ์ ์ฒด๋ฅผ ๊ฐ์ฒด๋ก ํํํ๋ฉฐ ์คํฌ๋ฆฝํ ์ธ์ด๋ก ์น ๋ธ๋ผ์ฐ์ ๋ฅผ ์กฐ์ํ  ์ ์๋๋ก ํด์ค๋ค.
๋ค์์ ์๋ฐ์คํฌ๋ฆฝํธ๋ก BOM ๊ฐ์ฒด๋ฅผ ์ด์ฉํด ํ์ฌ ๋ธ๋ผ์ฐ์ ์ URL ์ฃผ์๋ฅผ ์ถ๋ ฅํ๋ ์ฝ๋์ด๋ค.
```Javascript
console.log(location.href);
```
BOM์๋ ๋ค์๊ณผ ๊ฐ์ ๊ฐ์ฒด๊ฐ ์๋ค.
<table>
    <tbody>
        <tr>
            <td>navigator</td>
            <td>๋ธ๋ผ์ฐ์  ๋ช๊ณผ ๋ฒ์  ์ ๋ณด๋ฅผ ์์ฑ์ผ๋ก ๊ฐ์ง๋ค.</td>
        </tr>
        <tr>
            <td>window</td>
            <td>๋ธ๋ผ์ฐ์  ์์๋ค ์ค ์ต์์ ๊ฐ์ฒด์ด๋ค.</td>
        </tr>
        <tr>
            <td>history</td>
            <td>ํ์ฌ ์ฐฝ์์์ ์ฌ์ฉ์ ๋ฐฉ๋ฌธ ๊ธฐ๋ก์ ๊ฐ์ง๋ค.</td>
        </tr>
        <tr>
            <td>location</td>
            <td>ํ์ฌ ํ์ด์ง์ ๋ํ URL ์ ๋ณด๋ฅผ ๋ค๋ฃฌ๋ค.</td>
        </tr>
        <tr>
            <td>navigator</td>
            <td>ํ์ฌ ์ฌ์ฉ์ค์ธ ์น ๋ธ๋ผ์ฐ์  ์ ๋ณด๋ฅผ ๋ค๋ฃฌ๋ค.</td>
        </tr>
        <tr>
            <td>screen</td>
            <td>ํ์ฌ ์ฌ์ฉ์ค์ธ ํ๋ฉด ์ ๋ณด๋ฅผ ๋ค๋ฃฌ๋ค.</td>
        </tr>
    </tbody>
</table>