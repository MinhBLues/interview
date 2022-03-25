### 1. Cookies, Local Storage, Session Storage
- Cookies: 4KB, vài chục cookies cho 1 domain. Được gửi lên server.
- Local Storage: Kích thước 10MB.
- Session Storage: 5MB, dữ liệu bị xoá khi đóng tab. Dữ liệu không được gửi lên server khi send request.

### 2. CSS 
- Có 3 cách khai báo css: inline, style, link.
- Mức độ ưu tiên trong css: inline > id > class > tag, Ưu tiên css đứng sau.

#### CSS framework: Bootstrap, Foundation, UIkit

#### Doctype
- 1 đoạn định dạng không phải là html tag.
- Làm cho trình duyệt web biết được website đang sử dụng phiên bản nào

#### XHTML - HTML

#### Thuộc tính data html
- Lưu trữ data trực tiếp trên html tag

#### SASS - LESS (prepocessor)
- LESS xây dựng dựa trên javascript, SASS xây dựng dựa trên ruby.
- Minxin: Viết hàm trong sass.

#### Canavas - SVG
- Vẽ đồ hoạ 2D
- Canavas vẽ bằng javascript. SVG vẽ bằng xml
| Canavas  | SVG |
| ------------- | ------------- |
| Độ phân giải phải phụ thuộc.  | Độ phân giải độc lập  |
| Không hỗ trợ xử lý sự kiện  | Hỗ trợ xử lý sự kiện  |
| Khả năng kết xuất văn bản ké | Phù hợp nhất cho các ứng dụng có khu vực kết xuất lớn (Google Maps) |
| Bạn có thể lưu hình ảnh kết quả là .png hoặc .jpg | Kết xuất chậm nếu phức tạp (mọi thứ sử dụng DOM nhiều sẽ chậm) |
| Rất thích hợp cho các game chuyên sâu về đồ họa. | Không phù hợp với các ứng dụng trò chơi |

#### position
- Có 5 giá trị: static, relative, absolute, fixed, sticky
- Static: vị trí mặc định, đúng với văn bản.
- relative: vị trí tương đối so với vị trí ban đầu của nó.
- absolute: vị trí tương đối so với thằng cha.
- fixed: vị trí mặc định với windows, chỉ có tác dụng khi có scroll.

#### BEM (Block - Element - Modifers)
- Quy ước đặt tên trong CSS

#### SEO 
- Tag: title, meta, a, heading content(h1, h2,...), link, img

#### DOM 
- API lập trình cho các tài liệu XML, HTML


#### 3. Async, Defer, Normal <script>
- Async: bất đồng tải <script> trong việc dựng html.
- Defer: chạy song song với quá trình dựng html.

### 4. Scope javascript
- var: function scope (hoisting)
- let, const: block scope ({}) (no hoisting)
- Variable Scope: Global variables - Local variables.
- Global variables: are those declared outside of a block.
- Local variables: are those declared inside of a block.

### 5. "use strict" 
- Chế độ nghiêm ngặt, bắt buộc viết theo chuẩn javascript.

### 6. call, apply, bind
- Gán this cho function
- apply, call gán this cho function và truyền tham số vào function.
```javascript
function.call(Object)
function.apply(Object)
```
- apply truyền tham số vào theo dạng mảng
```javascript
function longerSummary(genre, year) {
  console.log(
    `${this.title} was written by ${this.author}. It is a ${genre} novel written in ${year}.`
  )
}
longerSummary.call(book, 'dystopian', 1932)
longerSummary.apply(book, ['dystopian', 1932])
```
### 7. Cloresure
- JavaScript Closures là tập hợp bao gồm một hàm và môi trường nơi hàm số đó được khai báo.
```javascript
function greeting(message) {
   return function(name){
        return message + ' ' + name;
   }
}
```

## 8. prototype
- Prototype là cơ chế mà các object trong javascript kế thừa các tính năng từ một object khác.
```javascript
function Person(){
}

Person.prototype.name = "Kien" ;
Person.prototype.age = 24;
Person.prototype.sayName = function(){
	console.log(this.name);
}

var person1 = new Person();

console.log(person1.name) // Output" Kien
```
### SSR, CSR, Pre-rendered

### Function Expression vs Function Declaration
```javascript
//Expression
alert(foo()); // ERROR! foo wasn't loaded yet
var foo = function() { return 5; }
// Declaration
alert(foo()); // Alerts 5. Declarations are loaded before any code can run.
function foo() { return 5; }
```

### XSS: tấn công bằng cách chèn script, html độc vào website

### Immediately Invoked Function Expression: 
- Khởi tạo một function và thực thi nó ngay lập tức.
```javascript 
(function(){
 //code here
})();
```