#lithuyet
## I/STRING FUNCTION
### 1/stringendwith
+ Có chức năng xác định liệu 1 chuỗi có kết thúc 1 kí tự hoặc
1 chuỗi được người dùng cung cấp.
+ Chuỗi kết thúc bằng kí tự trả về true
> string.endsWith(searchvalue, length)
### 2/string.fromCharCode()
+ Có chức năng chuyển đối giá trị Unicode thành kí tự
### 3/string.includes()
+ Sẽ kiểm tra xem 1 chuỗi con có nằm trong chuỗi hay không
> string.include(searchvalue, stort)
### 4/string.indexOf()
+ Kiểm tra và tra về vị trí xuất hiện đầu tiên trong chuỗi gốc
> string.indexOf(searchvalue, start)
> var str = "hoc lap trinh";
> -> str.indexOf("lap trinh") // 4 
+ Để tìm vị trí xuất hiện cuối chuỗi dùng lastIndexOf()
> var str = "hoc lap trinh mien phi tai";
>  str.lastIndexOf("i"); // 25
### 5,string.localeCompare()
+ Chức năng so sánh 2 chuỗi với nhau
+ string là chuỗi thứ nhất, compare là chuỗi thứ 2
### 6,string.match()
+ Tìm kiếm các chuỗi con phù hợp với biểu thức chính quy
+ Phương thức trả về các chuỗi dưới dạng 1 mảng
> string.match(regexp(biểu thức chính quy))
>  var str = "hoc lap trinh MIEN PHI tai";
> str.match(/i./ig) // in, IE, I, i
### 7,string.repeat()
+ Sẽ lặp lại chuỗi string với số lần nhất định
+ Trả về 1 chuỗi là n chuỗi string nối nhau
> string.repeat(count)
### 7,string.replace()
+ Tìm kiếm 1 chuỗi sau đó thay thế nó bằng 1 giá trị cung cấp người dùng.
> string.replace(searchvalue, newvalue)
> var str = 'hello this id';
> string.replace('id','tuan');
### 8,string.search()
+ Tìm kiếm chuỗi con trong chuỗi gốc
+ Trả về vị trí xuất hiện của chuỗi con đó.
> string.search(searchvalue);
### 9,string.slice()
+ Trích xuất 1 phần của chuỗi
+ Phương thức trả về 1 chuỗi mới là phần được trích dẫn từ chuỗi ban đầu
> string.slice(start, end)
### 10,string.splite()
+ Phân tách 1 chuỗi thành 1 mảng dữ liệu
+ Dựa vào kí tự phân cách chuối
+ Phương thức trả về mảng mới
>  string.split(separator, limit)
>  separator là kí tự phân cách chuỗi 
>  limit là tham số quy định phần tử tối đa mảng trả về
### 11,string.startsWith()
+ Sẽ kiểm tra xem chuỗi có được bắt đầu bằng 1 chuỗi con được cung cấp hay không
+ Trả về true
> string.startsWith(searchvalue, start)
> searchvalue là chuỗi con, start là vị trí trong chuỗi mà phương thức bắt đầu kiểm tra.
### 12,string.substr()
+ Chức năng xuất 1 chuỗi, chuỗi này xác định tham số
+ Trả về chuỗi
> string.substr(start, length)
> var str = 'hi anh em'
> str.substr(0, 7) //hi anh
### 13,string.substring()
+ Trích xuất nội dung 1 chuối
+ Trả về nội dung được trích xuất từ chuỗi gốc
> string.substring(start, end)
> var str = 'hello world';
> str.substring(0, 11) //hello world
### 14,string.toLocaleLowerCase(), string.toLocaleUpperCase():
+ Chuyển đối all kí tự thành kí tự thường 
> string.toLocaleLowerCase()
+ Chuyển đối all thành in hoa 
> string.toLocaleUpperCase()
### 15,string.toLowerCase(), string.toUpperCase()
+ Chuyển đổi kí tự in hoa thành thường
>  string.toLowerCase()
+ Chuyển đổi kí tự thường thành in hoa
>  string.toUpperCase()
### 16,string.toString()
+ Trả về 1 đối tượng kiểu chuỗi
+ Chuyển 1 mảng thành 1 chuỗi
> string.toString()
### 17,string.trim()
+ Sẽ loại bỏ khoảng trắng ở đầu và cuối chuỗi
+ Trả về chuỗi loại bỏ khoảng trắng
+ Không làm thay đổi chuỗi ban đầu
> string.trim() không tham số truyền vào
### 18,string.concat()
+ Nối hai hay nhiều chuỗi lại với nhau
+ Không làm thay đổi chuỗi truyền vào
> string.concat(string1, string2, ..., stringX)
### 19,string.charAt()
+ Tìm kiếm kí tự ở 1 vị trí nào đó trong chuỗi
>  string.charAt(index)
>  var str = "Frfdsj.net";
>   str.charAt(0) //F
### 20,string.charCodeAt()
+ Trả về mã Unicode của kí tự tại vị trí đó
> string.charCodeAt(index) i
> index là vị trí xuất hiện của kí tự cần tìm kiếm trong chuỗi.
> var str = "Fres.not.com";
> str.charCodeAt(0)  // 70
## II/DOM
### 1, appendChild 
+ Thêm một node vào vị trí cuối cùng
+ Ví dụ có 1 thẻ div trong có 10 thẻ p nếu muốn bổ sung thêm thẻ 11 dùng thuộc tính này.
+ Hàm này có 1 tham số truyền vào là 1 dom node
> **node.appendChild(node_append)**
```html
                        <div id="wrapper">
                              <p> hello everyone </p>
                         </div>
                        <input type ="button" value ='click' onclick ='add'>
```
```js
                        function add(){
                              var node = document.getElementById('wrapper');
                              var p = document.createElement('p')
                                      p.innerHTML = 'chao lan nua';
                              node.appendChild(p);
                        }
// Ngoài ra, muốn bổ sung 1 đoạn text thì có thể sử dụng hàm createTextNode để tạo một text
// text node bản chất là dom node, nó là 1 đoạn text chứ không phải thẻ html
                        function add(){
                              var node = document.getElementById('wrapper');
                                var textNode = document.createTextNode('hiho')
                              node.appendChild(textNode);
                        }

```

### 2, parentElement
+ Giúp lấy được thẻ html cha của thẻ html hiện tại
+ Trả về thẻ html đang chứa thẻ hiện tại hoặc trả về null o có thẻ nào.
+ Chỉ là thuộc tính đọc, trả về 1 dom object
> parentElement = node.parentElement;
> node là 1 dom object, ta sử dụng hàm sau để truy vấn:
- document.(getElementById(), tagName, className())
```js
// Thay đổi css color cho thẻ div
                        let node = document.getElementById('comy');
                           if(node.parentElement){
                              node.parentElement.style.color ='red'
                            }   
```
### 3, parentNode
+ Giúp lấy được thẻ html cha của thẻ html được chỉ định
+ Là 1 thuộc tính dom node object, nó sẽ trả về node cha của node chỉ định
> parentNode = node.parentNode
```html
                    <div> <p id ='text'>fđhksjhkfd</p>
```
```js
                let p = document.getElemntById('text')
                    // lấy div trong p
                  let div = p.parentNode; 
```
### 4, insertAfter(), insertBefore()
+ Hàm giúp chèn thêm các thẻ html vào sau 1 thẻ html nào đó
```html
              <ul> <li id='menu'>css</li> </ul> 
              <input type = 'button' value='add' onclick = 'insertAfterMenu()'>
```
```js
                    function insertAfter(newNode, existingNode) {
                        existingNode.parentNode.insertBefore(newNode, existingNode.nextSibling)
                        }
                     function insertAfterMenu(){
                          let menu = document.getElementById('menu')
                          let li = document.createElement('li')
                            li.textContent = 'php';
                              insertAfter(li, menu);
                      }
```
+ Hàm dùng để chèn 1 node html vào đằng trước 1 node khác
+ Phương thức được tích hợp sẵn js
> let insertedNode = parentNode.insertBefore(newNode, referenceNode(nốt được chèn))
```html
                   <div id="parentElement">
                           <span id="childElement">foo bar</span>
                    </div>
```
```js
                    // Xác định parentNode
                   let parentNode = document.getElementById('parentElement');
                  // Xác định referenceNode
                   let referenceNode = document.getElementById('referenceNode');
                  // Xác định newNode
                      let newNode = document.createElement('span');
                        newNode.textContent = "Bla fret";
  // Thực hiện chèn
let insertedNode = parentNode.insertBefore(newNode, referenceNode);
```



