# Javascript-function-regular

Đối với các web-developer thì việc làm việc với Javascript là điều không trành khỏi. Dưới đây là một số thứ sẽ làm tăng tốc độ code JS lên đáng kể

## Array method
1. Spread operator
Sử dụng để tự động điền phần tử của 1 array vào vị trí. Nó cũng có thể được sử dụng cho object.

Lợi ích khi sử dụng:
  Cú pháp ngắn gọn 
  Có thể sử dụng khi pass argument
  Hoạt động với cả array và object 


Example: 

const a = [1,2,3,4,5]

console.log(a)    ->  (3) [1, 2, 3]

console.log(...a) -> 1 2 3


2. filter

Trả về kết quả là array thoả màn điều kiện 

Example:

const arr = [1, 2, 3, 4, 5, 6];

const filter = arr.filter(x => x < 3);

console.log(filter); // output: [1, 2]

console.log(arr); // output: [1, 2]

3. some 

Check xem phần tử thoả mãn điều kiện có tồn tại trong array không

Example:

const arr = [1, 2, 3, 4, 5, 6];

const somed = arr.some((e) => e > 6);       // false


4. Every 

Cũng là một method check phần tử thoả mãn điều kiện, nhưng mà là thoả mãn tất cả điều kiện

const arr = [1, 2, 3, 4, 5, 6]

const everyed = arr.every((e) => e < 7);   // true 


5. concat

Gộp 2 mảng lại với nhau 

const arr = [1, 2, 3, 4, 5, 6]

[].concat(arr)    // [1, 2, 3, 4, 5, 6]


6. reduced

Có 4 tham số 
- accumulator
- currentValue
- currentIndex
- array

Method mình thích nhất và cũng là khó nhớ nhất. Có rất nhiều ứng dụng. Thực hiện các operator cho các phần tử trong array và accumulator sẽ được truyền cho lần tiêp theo
Ứng dụng thương để tính tổng hoặc đếm các phần tử array




Example: Đếm số lần xuất hiện phần tử
var names = ['Alice', 'Bob', 'Tiff', 'Bruce', 'Alice'];

var countedNames = names.reduce(function (allNames, name) { 

  if (name in allNames){
  
    allNames[name]++
    
  } else {
  
    allNames[name] = 1
    
  }
  
  return allNames;
  
}, {});

// countedNames is:

// { 'Alice': 2, 'Bob': 1, 'Tiff': 1, 'Bruce': 1 }






