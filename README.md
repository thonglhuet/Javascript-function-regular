# Javascript-function-regular

Đối với các web-developer thì việc làm việc với Javascript là điều không trành khỏi. Dưới đây là một số thứ sẽ làm tăng tốc độ code JS lên đáng kể.

Các hàm qúa quen thuộc mình sẽ k liệt kê ở đây

## Array method
1. Spread operator
Sử dụng để tự động điền phần tử của 1 array vào vị trí. Nó cũng có thể được sử dụng cho object.

Lợi ích khi sử dụng:
  Cú pháp ngắn gọn 
  Có thể sử dụng khi pass argument
  Hoạt động với cả array và object 


Example: 

```
const a = [1,2,3,4,5]

console.log(a)    ->  (3) [1, 2, 3]

console.log(...a) -> 1 2 3
```

2. filter

Trả về kết quả là array thoả màn điều kiện 

Example:

```
const arr = [1, 2, 3, 4, 5, 6];

const filter = arr.filter(x => x < 3);

console.log(filter); // output: [1, 2]

console.log(arr); // output: [1, 2]
```

3. some 

Check xem phần tử thoả mãn điều kiện có tồn tại trong array không

Example:
```

const arr = [1, 2, 3, 4, 5, 6];

const somed = arr.some((e) => e > 6);       // false
```

4. Every 

Cũng là một method check phần tử thoả mãn điều kiện, nhưng mà là thoả mãn tất cả điều kiện

```
const arr = [1, 2, 3, 4, 5, 6]

const everyed = arr.every((e) => e < 7);   // true 

```


5. concat

Gộp 2 mảng lại với nhau 

```
const arr = [1, 2, 3, 4, 5, 6]

[].concat(arr)    // [1, 2, 3, 4, 5, 6]

```

6. reduced

Có 4 tham số 
- accumulator
- currentValue
- currentIndex
- array

Method mình thích nhất và cũng là khó nhớ nhất. Có rất nhiều ứng dụng. Thực hiện các operator cho các phần tử trong array và accumulator sẽ được truyền cho lần tiêp theo
Ứng dụng thương để tính tổng hoặc đếm các phần tử array




Example: Đếm số lần xuất hiện phần tử
```
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

```

## String method

1. startsWith(), endsWith()

Kiểm tra xem String có bắt đầu hoặc kết thúc với text

```

var str = 'Welcome to hell';

console.log(str.startsWith('Welcome')); // true
console.log(str.startsWith('Welcome', 5)); // false
console.log(str.endsWith('Welcome')); // false

```

2. includes()

Kiểm tra contain text 

```
var str = 'Welcome to hell';
console.log(str.includes('Welcome')); // true
console.log(str.includes('Welcome'), 5); // false 

```

3. slice()

Tạo một chuỗi mới từ chuỗi ban đầu


```

var str = 'good luck, you are already in hell';
console.log(str.slice()); // good luck, you are already in hell
console.log(str.slice(4)); // luck, you are already in hell
console.log(str.slice(1,6)); // ood l


```

4. split()

Tách chuỗi thành mảng dựa vào separator

```
const monthString = 'Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov,Dec'
monthString.split(",");   // ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]

```
5. repeat()

Nhân chuỗi lên n lần

```
const monthString = "123 "
monthString.repeat(3);   // "123 123 123"
```
