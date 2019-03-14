1.去掉一个数组的重复元素
  //创建一个新数组，遍历要处理的数组，如果元素没有出现过，则添加到新数组中，最后返回新数组
    function unique1(arr) {
      if(arr.length===0) return [];
      var tmparr=[];
      for(var i=0;i<arr.length;i++){
        if(tmparr.indexOf(arr[i])===-1){
          tmparr.push(arr[i]);
        }
      }
      return tmparr;
    }
    
  //如果数组的第i项的初始位置不等于i，则为重复元素，可以忽略
    function  unique2(arr) {
      if(arr.length===0) return [];
      var tmparr=[arr[0]];
      for(var i=1;i<arr.length;i++){
        if(arr.indexOf(arr[i])===i){
          tmparr.push(arr[i]);
        }
      }
      return tmparr;
    }
