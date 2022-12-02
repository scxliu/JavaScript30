## Type Ahead

### 功能
- [x] 監聽輸入
- [x] 篩選資料
- [x] Highlight 搜尋詞
- [x] 從外部取得資料

### 技術點
- fetch
  https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch

- Number.prototype.toLocaleString
  > The toLocaleString() method returns a string with a language-sensitive representation of this number. 
  將數字 10000 變為字串 10,000
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString

- 判斷字串中是否有特定字串 (substr) 的方法
  - indexOf (case sensitive)
  - includes (case sensitive)
  - regex test

  速度比較
  https://stackoverflow.com/questions/5296268/fastest-way-to-check-a-string-contain-another-substring-in-javascript

- 清空 element of DOM
  - innerHTML = ''
  - textContent = ''
  - element.replaceChildren()

  https://dev.to/javascript_jeep/how-to-empty-the-dom-element-in-javascript-nf8

- Regex.test 的檢測結果問題
  > The test() method executes a search for a match between a regular expression and a specified string. Returns true or false.
  JavaScript RegExp objects are stateful when they have the global or sticky flags set (e.g., /foo/g or /foo/y). They store a lastIndex from the previous match. Using this internally, test() can be used to iterate over multiple matches in a string of text (with capture groups).

  若使用 global flag, 則 regex 會儲存當前的匹配字串的 的下一個 index 於 regex.lastIndex, 當你再呼叫一次 regex 匹配，則會從 lastIndex 開始的剩下字串開始匹配

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/lastIndex
  https://uu9924079.medium.com/%E7%82%BA%E4%BB%80%E9%BA%BC-regexp-test-%E8%BC%B8%E5%87%BA%E7%9A%84%E7%B5%90%E6%9E%9C%E6%9C%83%E4%B8%8D%E5%90%8C-%E4%BA%86%E8%A7%A3-js-regex-%E4%B8%AD%E7%9A%84-test-%E6%96%B9%E6%B3%95-5d7ea2d3e261

- String.prototype.replaceAll()
  > The replaceAll() method returns a new string with all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. The original string is left unchanged.

  replaceAll 必須使用 global regex

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replaceAll
  
- Element.insertAdjacentHTML()
  插入 HTML
  https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML

- HTMLElement: input event
  > The input event fires when the value of an <input>, <select>, or <textarea> element has been changed.
  https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event