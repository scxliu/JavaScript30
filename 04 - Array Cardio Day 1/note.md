## Array Cardio day

### 功能
- [x] reduce 用法
- [x] filter 用法
- [x] includes 用法

### 技術點
- Array.prototype.sort()
  > The sort() method sorts the elements of an array in place and returns the reference to the same array, now sorted. 
  
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort

  sort 可以接收 compareFn 並有兩個參數，first , second 
  當此 fn return > 0 ; 將 first 放 second 前 ; 
    此 fn return < 0 ; 將 first 放 second 後 ;
    此 fn return === 0 ; 將 first 放 second 不動 ;
  
  https://realdennis.medium.com/javascript-%E5%BE%9Earray%E7%9A%84sort%E6%96%B9%E6%B3%95-%E8%81%8A%E5%88%B0%E5%90%84%E5%AE%B6%E7%80%8F%E8%A6%BD%E5%99%A8%E7%9A%84%E5%AF%A6%E4%BD%9C%E7%AE%97%E6%B3%95-c23a335b1b80
- Array.propotype.reduce()
  > The reduce() method executes a user-supplied "reducer" callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element. The final result of running the reducer across all elements of the array is a single value.

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

  reduce 的概念就是將 reducer fn 遍歷每個 array element，並將將結果計入 accumulator

- Array.prototype.includes()
  > The includes() method determines whether an array includes a certain value among its entries, returning true or false as appropriate.