# Node.js-training
## Day 1
### 1. Xử lý chuỗi `comment sanitizer`

Có một đoạn text do người dùng nhập:
```js
const rawComment = "   I love JAVASCRIPT!!! It's soooo COOL!!!   ";
```

1. Xóa khoảng trắng dư ở đầu và cuối.
2. Viết hoa chữ cái đầu tiên, còn lại viết thường.
3. Giới hạn comment tối đa 30 ký tự, nếu dài hơn thì cắt và nối thêm "...".
4. Nếu comment chứa "cool" (không phân biệt hoa thường), đổi thành "great".
5. In ra kết quả cuối cùng.

### 2. Quản lý giỏ hàng (array + splice + push + pop + shift + unshift)
```js
let cart = ["apple", "banana", "orange"];
```
1. Thêm "mango" vào cuối và "kiwi" vào đầu.
2. Nếu "banana" tồn tại trong giỏ → xóa nó (dùng indexOf + splice).
3. Sau khi xóa, thêm "grape" ngay sau "apple".
4. Nếu giỏ hàng có hơn 4 món → xóa món cuối cùng.
5. In ra danh sách cuối cùng và tổng số món hàng.

### 3. Làm sạch danh sách chuỗi và nối thành chuỗi
Cho danh sách tên thô:
```js
const rawNames = "Alice,, Bob,   Charlie , ,David,";
```

1. Tách thành mảng theo dấu `,`
2. Xóa các phần tử rỗng ("" hoặc chỉ toàn khoảng trắng).
3. Chuẩn hóa từng tên (viết hoa chữ đầu, các chữ sau viết thường).
4. Nối lại thành chuỗi "Alice | Bob | Charlie | David".

### 4. Regex kiểm tra dữ liệu nhập vào

Tạo một hàm validateUserInput(input):

+ Trả về "Valid Email" nếu input là email hợp lệ.
+ Trả về "Valid Phone" nếu là số điện thoại 10 chữ số.
+ Trả về "Invalid" nếu không khớp gì cả.

Ví dụ:
```js
console.log(validateUserInput("test@example.com"));
console.log(validateUserInput("0987654321"));
console.log(validateUserInput("hello world"));
```

### 4. Primitive vs Reference
```js
let user1 = { name: "Huy", skills: ["JS"] };
let user2 = user1;
let user3 = structuredClone(user1); // deep copy

user2.name = "Nam";
user2.skills.push("TS");
user3.skills.push("React");

console.log(user1, user2, user3);
```

Giải thích chi tiết:
+ Vì sao user1 và user2 cùng thay đổi?
+ Vì sao user3 không bị ảnh hưởng?
