# Array.From 🔥
Phương thức `Array.from()` trả về `Array` từ bất kỳ đối tượng nào có **thuộc tính length** hoặc bất kỳ đối tượng nào **có tính lập** (`iterable object`).

*Ngoài ra nó cũng cung cấp chức năng như là `Array.Map()` *🤟😍  

> Array và String cũng được xem như là một iterable object. 

## Cách dùng 🎉
```js
// Cú pháp cơ bản
Array.from(iterable object);

// Tạo một Array từ String
Array.from("PUMDEPTRAI") // Returns [P,U,M,D,E,P,T,R,A,I]

// Tạo một Array từ một Array (cái này nó vô nghĩa v~ 🤮🥴)
Array.from([1,2,3,4]) // Returns [1,2,3,4] <- 😵

// Sử dụng chức năng như một Array.Map() (cái này mới có nghĩa đây!😎)
Array.from([1, 2, 3], x => x + x) // Returns [2,4,6]
// Cú pháp nó là:
Array.from(array, (element) => { /* ... */ })
```
## Tạo một Array từ một Object?
Nope! We can't. ❌❌❌
`Object` không phải là `iterable object` trừ khi chúng ta biến đổi nó.
Các bạn có thể tìm cách chuyển đổi từ đây [Making Objects Iterable in JavaScript](https://medium.com/swlh/making-objects-iterable-in-javascript-252d9e270be6%29https://medium.com/swlh/making-objects-iterable-in-javascript-252d9e270be6%29)

# Set 🔥
**Set trong Javascript** là một loại **object** cho phép bạn lưu trữ dữ liệu một cách duy nhất, **không trùng lặp**.

`Set` sử dụng thuật toán [SameValueZero](https://tc39.github.io/ecma262/#sec-samevaluezero) để so sánh giá trị của các phần tử.

>   Tương tự như việc sử dụng toán tử so sánh bằng  `===` để so sánh giá trị. Chỉ khác ở chỗ thuật toán này coi `NaN` là giống nhau (mặc dù `NaN !== NaN` là `true`). 

```js
const set2 = new Set([NaN, undefined, NaN]);
console.log(set2);
// Set(2) {NaN, undefined}
```
Vì vậy, ở trên chỉ đúng với `number` và `string`, còn đối với `object` thì khác. Bởi 2 object nhìn giống nhau nhưng rõ ràng chúng không bằng nhau.

```js
const obj1 = { x: 1, y: 2 };
const obj2 = { x: 1, y: 2 };

console.log(obj1 === obj2);
// false

const set1 = new Set([obj1, obj2]);
console.log(set1.size);
// 2
```

## Cách dùng 🎉
### Khởi tạo Set
```js
let set = new Set([iterable]);
```
### Khởi tạo Set rỗng
```js
let set = new Set(); // Set(0) {}
```
### Khởi tạo Set từ Array 
```js
const set = new Set(["P", "U", "M", "M", 1]);
console.log(set); // Set(4) {"P", "U", "M", "1"}
```
### Khởi tạo Set từ String
```js
const set = new Set("PUMM");
console.log(set); // Set(3) {"P", "U", "M"}
```
### Một số phương thức của Set
#### Lấy số lượng phần tử
```js
const set1 = new Set(["P", "U", "M","M"]);
console.log(set1.size); // 3 - vì set chỉ có hai phần tử ["P", "U", "M"]
```
#### Thêm phần tử
```js
// khởi tạo set rỗng
const set1 = new Set();

// thêm phần tử 1
set1.add(1);
console.log(set1);
// Set(1) {1}

// thêm phần tử 2 (khác 1)
set1.add(2);
console.log(set1);
// Set(2) {1, 2}

// thêm phần tử 3 (khác 1 và 2)
set1.add(1).add(2).add(3);
console.log(set1);
// Set(3) {1, 2, 3}
```
#### Kiểm tra phần tử tồn tại trong Set
```js
const set1 = new Set([1, "a", [1, 2]]);

console.log(set1.has(1)); // true
console.log(set1.has("1")); // false
console.log(set1.has("a")); // true
console.log(set1.has("b")); // false
console.log(set1.has([1, 2])); // false - vì [1, 2] !== [1, 2]
```
#### Xóa phần tử
```js
const set1 = new Set("PUMM1");
console.log(set1); // Set(4) {P, U, M, 1}

set1.delete(1);
console.log(set1); // Set(3) {P, U, M}
```
#### Xóa tất cả phần 
```js
const set1 = new Set([1, 2, 3]);
console.log(set1); // Set(3) {1, 2, 3}

set1.clear();
console.log(set1); // Set(0) {}
```


#### Kết hợp From và Set
```js
// khởi tạo set
const set1 = new Set([1, 2, 3, 4, 5, 5]);

// chuyển set thành array sử dụng Array.from
const arr1 = Array.from(set1);
console.log(arr1); // [1, 2, 3, 4, 5]

// Trick 🔥🔥🔥
// chuyển set thành array sử dụng cú pháp spread (...)
const arr2 = [...set1];
console.log(arr2);
// [1, 2, 3, 4, 5]

// Dùng để xóa các phần tử trùng nhau trong mảng!! 😍😍😍
```

# 🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚🔚
