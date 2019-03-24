# hw1

## 作業規格

1. 每一個方格的寬度為 300 px，高度不限，但每個方格的高度必須一樣
2. 上面為遊戲瀏覽畫面，圖片可以用[這張](https://static-cdn.jtvnw.net/previews-ttv/live_user_wayne75525-320x180.jpg)
3. 下面左邊是實況主的大頭貼，可以先用[這張](https://static-cdn.jtvnw.net/jtv_user_pictures/fate_twisted_na-profile_image-f51be41c0c37cf65-300x300.jpeg)代替
4. 一排有三個方格
5. 不需做 RWD，可以直接假設螢幕寬度會在 1000 px 以上
6. 背景圖片可以用[這張](http://cdn.leagueoflegends.com/lolkit/1.1.6/resources/images/bg-default.jpg)
7. 因為背景圖片太亮，所以背景圖片上面必須疊一層透明度為 50% 的黑色
8. 背景圖片必須保持不動（`background-attachment: fixed`）
9. 作業成品需要有九個方格，你可以做完一個之後複製九遍即可
10. 必須可以滾動

## 自我練習

1. 請問 CSS 的屬性`position`有哪幾種值？
static、 relative、fixed、absolute、sticky

2. 承上，請問那幾種值有哪些區別？請講出適合應用的地方。
* static: 不會被特別指定頁面上的位置，依照瀏覽器預設配置自動排版在頁面上。
* relaive: 將元素內top、right、bottom、left屬性的元素，相對調整位置
* fixed: 固定在瀏覽器視窗的某個位置，可以使用top、right、left、bottom，設定它的位置。
* absolute: 浮動位置定位在上層容器的相對位置，如果上層沒有可以定位的元素，則以body當作定位容器。
* sticky: 當滾輪滾到設定sticky區塊時，會將該元素固定位置。

3. `display`的三個值`inline`, `block`, `inline-block`有什麼異同？可以試著舉出幾個例子嗎？
* inline 不會獨佔一行，多個相鄰inline屬性會排列同一行，任何固定區塊大小屬性無法使用(width、height)
* block 代表元素會以區塊方式呈現，可以設定高寬度。
* inline-block 同時具備inline和block屬性，可以將區塊水平顯示。

4. 有哪些 HTML 元素是 `inline`, 哪些是 `block`？
* inline a、span、b、i、img、ifamed
* block div、p、h1、ul、li

5. 當我設定一個元素的`width`為`300px`，並且`padding`設成`10px`之後，這個元素的寬度應該會是多少？
300+10(左)+10(右) = 320

6. 這次實作的畫面當頻道名稱字太多的時候，會超出一格的大小或者會直接被卡掉，有沒有辦法讓字太多的時候在尾巴顯示`...`？例如原本名稱叫做：「1234567」，顯示的時候變成：「12345...」？
p {
    white-space: nowrap; /* no newline */
    overflow: hidden; /* crop text */
    text-overflow: ellipsis; /* ... */
}

## 進階閱讀

1. [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
2. [學習 CSS 版面配置: flexbox](http://zh-tw.learnlayout.com/flexbox.html)
3. [深入解析 CSS Flexbox](http://www.oxxostudio.tw/articles/201501/css-flexbox.html)