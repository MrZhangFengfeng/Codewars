数组**末尾**添加元素，返回新数组：

    arr.concat(item);
    
    arr.concat(item1,item2);
  
    arr.concat(arr2,arr3);
    
 - - -
 
数组**头部**添加元素，返回新数组：

    [item].concat(arr);
    
    function prepend(arr, item) {
         var a = arr.slice(0);
         a.unshift(item);
         return a;
     }
     
- - -

arr.push() 返回的是新数组的**长度**,并且是改变原数组。

- - -

统计数组 arr 中值等于 item 的元素出现的次数:

    function count(arr, item) {
        var count = 0;
        arr.map(function(a) {
            if(a === item) {
                count++;
            }
        });
        return count;
    }
    

    function count(arr, item) {
        return arr.filter(function(a){
            return (a==item);
        }).length
    }
  
  - - - 
  
在数组 arr 中，查找值与 item 相等的元素出现的所有位置(巧用或运算)

    function findAllOccurrences(arr, target) { 

      var temp = []; 
          arr.forEach(function(val,index){ 
              val !== target ||  temp.push(index); 
          }); 
          return temp; 
      }
      
- - -

