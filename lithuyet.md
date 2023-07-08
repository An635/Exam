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
### 5,innerHTML 
+ Công dụng giúp lấy nội dung hoặc thiết lập nội dung cho 1 node html
```html
                    <div id='node'> Học js </div>
```
```js
                    let node = document.getElementById('node')
                     //Lấy nội dung
                          let content = node.innerHTML
                     //gán nội dung
                              node.innerHTML = 'hfkj';  
```
### 7,insertAdjacentHTML
+ Chèn các node vào các vị trí xác định
+ Vị trí này được chỉ định bởi tham số hàm
> element.insertAdjacentHTML(position, text);
> text là 1 chuỗi string 
> position là vị trí trèn
```html
                          <!-- Vị trí 1: beforebegin-->       
                            <div id="node">
                                <!-- Vị trí 2:afterbegin --> 
                                <span>Học lập trình miễn phí.</span>
                                <span>Tfdjlkfdet</span>
                                <!-- Vị trí 3:beforeend --> 
                            </div>
                            <!-- Vị trí 4:afterend -->
```
```js
                        let element = document.getElementById('node');
 
                    // Vị trí 1: beforebegin
                    element.insertAdjacentHTML("beforebegin", '<span>Nội dung chèn 1</span>');
                     
                    // Vị trí 2: afterbegin
                    element.insertAdjacentHTML("afterbegin", '<span>Nội dung chèn 2</span>');
                     
                    // Vị trí 3: beforeend
                    element.insertAdjacentHTML("beforeend", '<span>Nội dung chèn 3</span>');
                     
                    // Vị trí 4: afterend 
                    element.insertAdjacentHTML("afterend", '<span>Nội dung chèn 4</span>');
```
### 8,nextSibling
+ là một thuộc tính của node js
+ Công dụng của nó trả về node kế tiếp node hiện tại
>  nextNode = node.nextSibling
> node chính là node được chỉ định
> nextNode là node kế tiếp được trả về từ thuộc tính nextSibling
```html
                     <span id="value1">Value 1</span>
                      <span id="value2">Value 2</span>
```
```js
                       let node = document.getElementById('value1');
                        let nextNode = node.nextSibling;
                        console.log(nextNode); // #text
```
### 9,activeElement
+ Lựa chọn phần tử đang được focus trong tài liệu
+ Nó phụ thuộc vào con trỏ chuột của chúng ta đang focus vào tài liệu html
+ Nếu muốn thiết lập focus tói 1 thẻ html nào đó sử dụng thuộc tính phương thức
> element.focus()
>  document.activeElement
> Để lấy tên của thẻ HTML mà method này trả về thì ta sử dụng thuộc tính tagName.
> document.activeElement.tagName
```html
         <body onclick="myFunction()">
                <h1>Học lập trình </h1>
          <p>Các bạn click vào bất cứ điểm nào trên trang để tìm phần tử đang được focus</p>
                <input type="text" value="Thẻ Input">
                <button>Thẻ Button</button>
                <p id="result"></p>
            </body>
```
```js
         function myFunction() {
            var x = document.activeElement.tagName;
            document.getElementById("result").innerHTML =
                    "bạn đang focus vào thẻ " + x;
        }     
```
### 10,document adoptNode()
+ Sẽ lấy 1 thẻ html từ 1 trang khác
+ Thẻ được lấy và tất cả thẻ con của nó sẽ bị loại bỏ ở trang cũ
+ Nếu muốn sao chép chứ không muốn loại bỏ ở trang cũ sử dụng:
> document.importNode()
+ Nếu muốn sao chép 1 phần tử trong trang chính đó ta sử dụng phương thức
> document.adoptNode(tag là tên thẻ muốn lấy)
```html
                  <iframe src="https://fdklfjsdl.com"></iframe>
                <button onclick="myFunction()">Lấy về thẻ H1</button>
```
```js
                function myFunction() {
                var frame = document.getElementsByTagName("IFRAME")[0];
                var h = frame.contentWindow.document.getElementsByTagName("H1")[0];
                var x = document.adoptNode(h);
                document.body.appendChild(x);
    }
```
### 11,document archors()
+ Giúp ta lấy được tất cả thẻ a trong html
> document.anchors
```html
                <a name="abcd" href="#">HTML</a>
                  <a name="abcd" href="#">PHP</a>
                  <a href="#">CSS</a>
                  <a name="abcd" href="#">C#</a>
                  <a href="#">JAVASCRIPT</a>
                  <a name="abcd" href="#">PYTHON</a>
                  <button onclick="myFunction()">Xem kết quả</button>
                  <p id="result"></p>
```
```js
                function myFunction(){
                var x = document.anchors.length;
                document.getElementById("result").innerHTML = 
                'Số thẻ a được thiết lập thuộc tính name là ' + x;}                    
```
### 11,document baseURL()
+ Trả về giá về giá trị url trang web hiện tại
+ Chỉ lấy url chứ không thiết lập url cho trang được
> let uri = document.baseURI
```html
                <button onclick="myFunction()">Xem kết quả</button>
                  <p id="result"></p>
```
```js
              function myFunction(){
                var x = document.baseURI;
                document.getElementById("result").innerHTML = 
                'URI của trang hiện tại là: ' + x;
            }
```
### 12,document baseURL()
+ Thiết lập nội dung tài liệu html cho thẻ body
> document.body = newContent
```html
               <p>Đây là nội dung của trang...</p> 
                <button onclick="myFunction()">Xem kết quả</button>
                <p id="result"></p>
```
```js
                 function myFunction(){
                document.body.style.backgroundColor = "yellow";
            }
```
### 13,document characterSet()
+ Lấy được bộ mã hóa kí tự đang sử dụng trên web
>   document.characterSet
>   Thuộc tính này tương đương với document.inputEncoding và document.charset.       
```html
             <p id="result"></p>
        <button onclick="myFunction()">Xem kết quả</button>
```
```js
           function myFunction() {
                var x = document.characterSet;
                document.getElementById("result").innerHTML = "characterSet hiện tại là: " + x;
            }
```
### 14,document createAttribute()
+ Là 1 phương thức thuộc đối tượng document
+ createAttribute() tạo ra 1 thuộc tính, xác định tên mà chưa có bất kì giá trị nào 
+ attribute.value() thiết lập giá trị cho thuộc tính
+ element.setAttributeNode() thiết lập thuộc tính đã tạo cho 1 phần tử html
> document.createAttribute(attributename) có thể là tên thuộc tính
+ ví dụ 
- let id = document.createAttribute('id');
- id.value = "result";
### 15,document createComment()
+ Tạo ra 1 đoạn ghi chú với nội dung đã được xác định
> document.createComment(text)
### 16,document.createDocumentFragment()
+ Tạo 1 đối tượng node object ảo với tất cả các thuộc tính và phương thức của 1 đối tượng
> document.createDocumentFragment()
### 17,document.createElement()
+ Tạo 1 node với tên node xác định
> document.createElement(nodename)
```html  
                         <button onclick="myFunction()">Xem kết quả</button>
```
```js
                  function myFunction(){
                var div = document.createElement("div");
                var text = document.createTextNode("Đây là nội dung của thẻ div mới được tạo!");
                div.appendChild(text);
                document.body.appendChild(div);
			}
```
### 18,document.createTextNode()
+ Tạo nội dung văn bản 
>   document.createTextNode(text)
```js
                    <button onclick="myFunction()">Xem kết quả</button>
                var div = document.createElement("div");
                var text = document.createTextNode("Đây là nội dung của thẻ div mới được tạo!");
                div.appendChild(text);
                document.body.appendChild(div);
			}
```
### 19,document.doctype()
+ Trả về loại tài liệu trang HTML dưới dạng 1 documentType object
+ Có thuộc tính name, trả về tên của tài liệu
+ Không xác định loại tại liệu sẽ trả về null
> document.doctype
```css
           div {
                color: black;
                margin: 10px 0px;
                text-align: center;
                background: red;
                width: 400px;
                height: 50px;
            }
```
```js
                  <button onclick="myFunction()">Xem kết quả</button>
                  function myFunction(){
                var div = document.createElement("div");
                var doctype = document.doctype.name;
                var text = document.createTextNode("Loại tài liệu của trang: " + doctype);
                div.appendChild(text);
                document.body.appendChild(div);
			}
```
### 20,document.documentElement()
+ Sẽ trả về documentElement của trang hiện tại dưới dạng một Element Object.
+ documentElement có thể hiểu như là phần tử gốc của một trang
+ Đối với các trang HTML, thuộc tính documentElement sẽ trả về đối tượng là thẻ <html>
+ Thuộc tính này chỉ có quyền đọc
> document.documentElement
```css
                 div {
                color: black;
                margin: 10px 0px;
                text-align: center;
                background: yellow;
                width: 400px;
                height: 50px;
            }
```
```js
                function myFunction(){
                var div = document.createElement("div");
                var doctype = document.documentElement.nodeName;
                var text = document.createTextNode("documentElement của trang: " + doctype);
                div.appendChild(text);
                document.body.appendChild(div);
			}
```
### 21,document.documentMode()
+ Trả về phương thức được trình duyệt sử dụng để hiển thị trang;
+  thuộc tính này chỉ có thể sử dụng với trình duyệt IE, nếu sử dụng ở trình duyệt khác, thuộc tính sẽ trả về undefined.
> document.documentMode

### 22,document.documentURL()
+ Thiết lập hoặc trả về đường dẫn hiện tại
+ Sử dụng bất cứ trang nào
> document.documentURI
>  document.documentURI = locationURI
```html
               <div id="result"></div>
        <button onclick="myFunction()">Xem kết quả</button>
```
```js
                  function myFunction(){
                    var location = document.documentURI;
                    document.getElementById("result").innerHTML = location;
			}
```
### 23,document.domain()
+ Trả về tên domain trang hiện tại
> document.domain
```css
                    <div id="result"></div>
                      <button onclick="myFunction()">Xem kết quả</button>
                    div {
                        color: red;
                        font-size: 18px;
                        font-weight: bold;
                        margin: 10px 0px;
                        text-align: center;
                        width: 400px;
                        height: 50px;
                    }
```
```js
                          
              function myFunction(){
                var domain = document.domain;
                document.getElementById("result").innerHTML = "Tên domain hiện tại là: " + domain;
			}
```
### 24,document.embeds()
+  Một bộ chọn có các thuộc tính và phương thức như một object, nó sẽ chọn
+  lấy một tập hợp kết quả
+ Các thẻ trong tập hợp được trả về sẽ được sắp xếp theo đúng thứ tự chúng xuất hiện trên trang
+ Sử dụng thuộc tính length để lấy số phần tử nằm trong collection
> document.embeds
### 25,document.forms()
+ Một bộ chọn có các thuộc tính và phương thức như 1 object
 > document.forms

### 26,document.hasFocus()
+ Sẽ kiểm tra xem liệu tràn hoặc bất cứ phần tử trang nào trên trang có được focus không.
> document.hasFocus()
```css
                #result{
                                color: red;
                                font-size: 20px;
                                font-weight: bold;
                            }
```
``` html
                <p>Click vào bất cứ phần tử nào để focus trang</p>    
                <form action="#" method="POST">
                    Username: <input type="text" name="fname" placeholder="Nhập Username"><br>
                    Email: <input type="text" name="lname" placeholder="Nhập Email">
                </form>
 
                <p id="result"></p>
                <button onclick="myFunction()">Xem kết quả</button>
```
```js
                 setInterval("myFunction()", 5);
                    function myFunction(){
                        var x = document.getElementById("result");
                        if (document.hasFocus()) {
                            x.innerHTML = "Trang đã được focus.";
                        } else {
                            x.innerHTML = "Trang chưa được focus.";
                        }}
```
### 27,document.head()
+  Sẽ trả về phần tử head của trang tài liệu
+  Nếu có nhiều thẻ head trong trang, thẻ head đầu tiên sẽ được trả về.
> document.head
``` html
                              <p id="result"></p>
                            <button onclick="myFunction()">Xem kết quả</button
```
```js
                       function myFunction(){
                      var head = document.head;
                      document.getElementById("result").innerHTML = "ID của thẻ head là: " + head.id;
                  }
```
### 27,document.images()
+ Sẽ trả về tập hợp các thẻ img
> document.images
### 28,document.implementation()
+  Sẽ trả về đối tượng DOMimplementation object
+  Một đối tượng cung cấp các phương thức,
+  Thuộc tính mà không phụ thuộc vào bất kì kiểu trang nào.
> document.implementation
``` html
<p>Click để kiểm tra xem trang hiện tại có đặc tính HTML DOM 1.0 hay không</p>
        <p id="result"></p>
        <button onclick="myFunction()">Xem kết quả</button>
```
```js 
		function myFunction() {
	                var imp = document.implementation;
	                var result = imp.hasFeature("HTML", "1.0") ? "Có" : "Không";
	                document.getElementById("result").innerHTML = result;
            }
```
### 29,document.importNode()
+ Sẽ lấy một node từ một trang khác và nhập trang hiện tại
+ Có thể nhập bất cứ loại thẻ nào.
> document.importNode(node, deep)
> node là một node từ một tài liệu khác
> deep bắt buộc, nếu mang giá trị true thì các thẻ con trong node cũng sẽ được nhập.
### 30,document.inputEncoding()
+ Sẽ trả về bộ mã hóa kí tự được sử dụng cho trang.
+ sẽ trả về bộ mã hóa kí tự tại thời điểm phân tích cú pháp.
+ Thuộc tính này có chức năng tương tự với document.characterSet.
> document.inputEncoding
```css
			#result{
		                color: red;
		                font-size: 20px;
		                font-weight: bold;
		            }
<p id="result"></p>
<button onclick="myFunction()">Xem kết quả</button>
```
```js
	 function myFunction(){
                var charset = document.inputEncoding;
                document.getElementById("result").innerHTML = "characterSet hiện tại là: " + charset;
            }
```
### 31,document.lastModified()
+ Sẽ trả về thời gian của lần chỉnh sửa trang gần nhất
+ Thời gian trả về sẽ bao gồm các thông tin giờ, phút, giây và ngày, tháng, năm.
+ Thuộc tính này chỉ có quyền đọc(read-only), tức là người dùng sẽ không thể thiết lập giá trị cho nó.
> document.lastModified
```css
					#result{
			                color: red;
			                font-size: 20px;
			                font-weight: bold;
			            }
			<p id="result"></p>
			        <button onclick="myFunction()">Xem kết quả</button>
```
```js
				function myFunction(){
		                var time = document.lastModified;
		                document.getElementById("result").innerHTML = 
		                "Lần chỉnh sửa gần nhất vào lúc : " + time;
		            }
```
### 32,document.links()
+ sẽ trả về một collection tập hợp tất cả các liên kết xuất hiện trên trang tài liệu.
+ Nếu một phần tử không có thuộc tính href nó sẽ không được chọn vào collection.
+ Các phần tử trong collection sẽ được sắp xếp theo đúng thứ tự chúng xuất hiện trên trang.
> document.links
```css
			#result{
		                color: red;
		                font-size: 20px;
		                font-weight: bold;
            		}

			<map name="planetmap">
			          <area href="#">Arena-1</map>
			          <area href="#">Arena-2</map>
			          <area href="#">Arena-3</map>
			        </map>
			
			        <p>
			          <a>HTML</a><br>
			          <a href="/css/default.asp">CSS</a>
			        </p>
			        <p id="result"></p>
			        <button onclick="myFunction()">Xem kết quả</button>

```
```js
		
				 function myFunction(){
		                var lenght = document.links.length;
		                document.getElementById("result").innerHTML = 
		                "Số liên kết trên trang : " + lenght;
		            }
```
### 33,document.normalize ()
+ Sẽ nối các đoạn text gần kề lại với nhau
> document.normalize()
### 34,document.scripts()
+ Sẽ trả về 1 collection tập hợp các phần tử 
> document.scripts
```html
				<p id="result"></p>
        			<button onclick="myFunction()">Xem kết quả</button>
```
```js
				 function myFunction(){
			                var lenght = document.scripts.length;
			                document.getElementById("result").innerHTML = 
			                "Số thẻ script trong trang là : " + lenght;
			            }
```
### 35,document.querySelctor ()
+ Sẽ trả về phần từ đầu tiên trong tập hợp các kết quả tìm thấy 
> document.querySelector(CSS selectors)
```css
				 #result{
			                color: red;
			                font-size: 20px;
			                font-weight: bold;
			            }
				<ul class="freetut">
			            <h3>Khóa học 1</h3>
			            <h3 class="demo"> Name: PHP</h3>
			            <h3 class="demo">Time: 48 Videos</h3>
			            <h3 class="demo">Author: Nguyễn Văn A</h3>
			        </ul>
			        <p id="result"></p>
			        <button onclick="myFunction()">Xem kết quả</button>
```
```js
				 function myFunction(){
                document.querySelector(".demo").style.color = "red";
            }
```
### 36,document.querySelctorAll()
+ Trả về tất cả các phần trong tập hợp các kết quả được tìm thấy css selector
+ Là NodeList object
>   document.querySelectorAll(CSS selectors)
```css
	
				#result{
			                color: red;
			                font-size: 20px;
			                font-weight: bold;
			            }
				<ul class="fdf">
			            <h3>Khóa học 1</h3>
			            <h3 class="demo"> Name: PHP</h3>
			            <h3 class="demo">Time: 48 Videos</h3>
			            <h3 class="demo">Author: Nguyễn Văn A</h3>
			        </ul>
			        <p id="result"></p>
			        <button onclick="myFunction()">Xem kết quả</button>
```
```js
				function myFunction(){
			                var NodeObject = document.querySelectorAll(".demo");
			                NodeObject.forEach(function(item){
			                    item.style.color = "red";
			                });
			            }	
```	
### 37,document.removeEventListener()
+ Sẽ xóa bỏ một sự kiện đã được gán vào bởi phương thức document.addEventListener().
> document.removeEventListener(event, function, useCapture)
> event là một chuỗi đại diện cho sự kiện và không sử dụng tiền tố on
```css
					#result{
				                color: red;
				                font-size: 20px;
				                font-weight: bold;
				            }
					<p id="result"></p>
					<button onclick="removeHandler()">Remove event</button>
```
```js	
			document.addEventListener("mousemove", myFunction);
			    function myFunction() {
			document.getElementById("result").innerHTML = Math.random();}
			            function removeHandler() {
			document.removeEventListener("mousemove", myFunction);}
```
### 37,document.getElementById()
+ Trả về thuộc tính id 
> document.getElementById(elementID)
```css
			<p id="result">Đây là thẻ có id="result"</p>
        		<button onclick="myFunction()">Xem kết quả</button>
```
```js
			function myFunction(){
	                document.getElementById("result").style.color = "red";
	                document.getElementById("result").style.fontSize = "20px";
	                document.getElementById("result").style.fontWeight = "bold";
	            }
```
### 38,document.getElementsByClassName()
+ Trả về tập hợp các phần tử trong trang có thuộc tính class
+ Kết quả trả về nodeList object
+ Đối tượng nodeList này đại diện cho danh sách node
+ Người dùng có thể truy cập các node bằng chỉ số
> document.getElementsByClassName(classname)
```css
			#result{
		                color: red;
		                font-size: 20px;
		                font-weight: bold;
		            }
			<ul class="freetut">
		            <h3>Khóa học 1</h3>
		            <h3 class="demo"> Name: PHP</h3>
		            <h3 class="demo">Time: 48 Videos</h3>
		            <h3 class="demo">Author: Nguyễn Văn A</h3>
		        </ul>
			<p id="result">Đây là thẻ có id="result"</p>
        		<button onclick="myFunction()">Xem kết quả</button>
```
```js
		function myFunction(){
	                var NodeObject = document.getElementsByClassName("demo");
	                NodeObject[0].style.color = "red";
	                NodeObject[1].style.color = "blue";
	                NodeObject[2].style.color = "yellow";
	            }
```
### 39,document.getElementsByName()
+ Trả về tập hợp các phần tử trong trang có thuộc tính name được cung cấp
+ Trả về duois dạng 1 đối tượng nodelist Object












