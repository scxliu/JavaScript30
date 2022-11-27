## Css variables

### 功能
- [x] input value 變化監聽(持續)
- [x] 改變 img style (border , blur)

### 技術點
- HTMLElement: change event
  > The change event is fired for \<input\>, \<select\>, and \<textarea\> elements when the user modifies the element's value. Unlike the input event, the change event is not necessarily fired for each alteration to an element's value
  https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event
- blur function
  > The blur() CSS function applies a Gaussian blur to the input image. Its result is a <filter-function>.
  https://developer.mozilla.org/en-US/docs/Web/CSS/filter-function/blur
- Nullish coalescing (??) operator
  > The nullish coalescing (??) operator is a logical operator that returns its right-hand side operand when its left-hand side operand is null or undefined, and otherwise returns its left-hand side operand.
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing
  當左側 operands 為 null / undefined 則  return 右側
  與 || 不同的是， || 是當 當左側 operands 為 false(type conversion 後也算) 則  return 右側
- HTMLElement.dataset
  > The dataset read-only property of the HTMLElement interface provides read/write access to custom data attributes (data-*) on elements. It exposes a map of strings (DOMStringMap) with an entry for each data-* attribute.
  https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset
- Cannot using Continue in JavaScript forEach()
  Use return or filter unwanted
  https://masteringjs.io/tutorials/fundamentals/foreach-continue
- Object.entries()
  > The Object.entries() method returns an array of a given object's own enumerable string-keyed property key-value pairs.
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries
- Get value of input
  https://stackoverflow.com/questions/11563638/how-do-i-get-the-value-of-text-input-field-using-javascript


### 正解解法
- 更改 CSSStyleDeclaration 的 property value ，比如
  以 --root 定義的 style : 
  ```
  document.documentElement.style.setProperty
  ```
  以 css stylesheet 定義的 style : 
  ```
  const stylesheet = document.styleSheets[1];
  const boxParaRule = [...stylesheet.cssRules].find((r) => r.selectorText === ".box p");
  boxParaRule.style.setProperty()
  ```
  https://developer.mozilla.org/en-US/docs/Web/API/CSSStyleDeclaration/setProperty

