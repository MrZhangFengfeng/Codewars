数组**末尾**添加元素，返回新数组：

    arr.concat(item);单个
    
    arr.concat(item1,item2);两个元素
    
    arr.concat(arr2,arr3);两个数组
    
数组**头部**添加元素，返回新数组：

    [item].concat(arr);
    
    function prepend(arr, item) {
         var a = arr.slice(0);
         a.unshift(item);
         return a;
     }

arr.push() 返回的是新数组的**长度**,并且是改变原数组。
