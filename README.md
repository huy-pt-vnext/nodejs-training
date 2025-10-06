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
