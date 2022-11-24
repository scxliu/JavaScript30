## JS DRUM KIT

### 功能
- [x] 鍵盤按鈕點擊間聽
- [x] 聲音播放
- [x] 光暈特效
- [x] 放大特效

### 技術點
- Keydown event : 
    > KeyboardEvent.key : Returns a string representing the key value of the key represented by the event.
    https://developer.mozilla.org/en-US/docs/Web/API/Element/keydown_event
- Transitionend event :
    > TransitionEvent.propertyName : A string containing the name CSS property associated with the transition.
    
    https://developer.mozilla.org/en-US/docs/Web/API/Element/transitionend_event
- Array.from() Method : 
    > The Array.from() static method creates a new, shallow-copied Array instance from an iterable or array-like object.
    
    https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from

- HTMLAudioElement : 
    > The HTMLAudioElement interface provides access to the properties of \<audio\> elements, as well as methods to manipulate them.
    > Some of the more commonly used properties of the audio element include **src**, **currentTime**, **duration**, **paused**, **play**,  **muted**, and **volume**. This snippet copies the audio file's duration to a variable:
    
    https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement
