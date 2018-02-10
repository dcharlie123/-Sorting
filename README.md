# -Sorting
手写一波各种排序
```javascript
function swap(arr,a,b){
  var temp=arr[a];
  arr[a]=arr[b];
  arr[b]=temp;
}
```
## 冒泡
```javascript
function PSort(arr){
  console.time();
  for(var i=0;i<arr.length;i++){
    for(var j=i+1;j>0;j--){
      if(arr[j]<arr[j-1]){
        swap(arr,j,j-1);
      }
    }
  }
  console.timeEnd();
  console.log(arr)
}
```
## 选择排序
```javascript
function sort2(arr){
  let len = arr.length;
  for(var i=0;i<len;i++){
    var minIndex=i;
    for(var j=i+1;j<len;j++){
      if(arr[j]<arr[minIndex]){
        minIndex=j
      }
    }
    swap(arr,minIndex,i)
  }
  return arr;
}
```
## 插入排序
```javascript
function sort3(arr){
  for(var i=1,len=arr.length;i<len;i++){
    let index=i-1,
        temp=arr[i];
    while(index>=0 && arr[index]>temp){
      arr[index+1]=arr[index];
      index--;
    }
    arr[index+1]=temp;
  }
  return arr;
}
```
