# exam
## 1/LẤY GIÁ TRỊ CHECKBOX:
```HTML
    <input type="checkbox" name="hobby" value="học lập trình"/>
            <label>học lập trình</label> <br/>
    <input type="checkbox" name="hobby" value="Lướt freetuts.net"/>
            <label>Lướt freetuts.net</label>
```
```JS
      document.getElementById('btn').onclick = function(){
           let checkBox = document.getElementsByName('hobby');
           let result = '';
             for(let i=0; i < checkBox.length; i++){
                 if(checkBox[i].checked ===true){
                      result += '['+ checkBox[i].value + ']'  //('Có thể thêm toán tử nối chuỗi')
                 } 
             }
             alert('gia tri can tim: ' + result)
          }
```
## 2/BẮT SỰ KIỆN CHECKBOX:
```HTML
         <input type="checkbox" id="btn" value="Xem kết quả"/> click vao
```
```JS
        document.getElementById('btn').onclick = function(){
               if(this.checked == true){
                    alert('bạn đã click thành công')
               }else{
                    alert('bạn đã bỏ chọn thành công')
               }}
```
## 3/TẠO CHECKALL:
```HTML
         <table cellpadding="8" border="1">
                <tr >
                    <td>
                        <input type="checkbox" name="name" id="checkAll">
                    </td>
                    <td>Nguyen Nam</td>
                </tr>
                <tr>
                    <td>
                        <input type="checkbox" name="name" id="checkAll">
                    </td>
                    <td>Nguyen Doan Gioi</td>
                </tr> </table>
            <input type="button" id="btn1" value="chọn hết"/> 
            <input type="button" id="btn2" value="bỏ chọn"/>
```
```js
            document.getElementById('btn1').onclick = function(){
                    // Có thể dùng byname, tagname;
                    var check = document.getElementsByTagName('input');
                          for(var i=0; i < check.length; i++){
                            check[i].checked = true}}
            document.getElementById('btn2').onclick = function(){
                    var check = document.getElementsByTagName('input');
                          for(var i=0; i < check.length; i++){
                             check[i].checked = false }}
```
## 4/LẤY GIÁ TRỊ RADIO:
```HTML
        <input type="radio" name="gender" id="male" value="nam"/> Nam
        <input type="radio" name="gender" id="female" value="nữ"/> Nữ 
        <input type="button" id="btn1" value="submit"/>
```
```JS
        document.getElementById('btn1').onclick = function(){
            var check = document.getElementsByName('gender);
            for(let i=0; i < check.length; i++){
                if(check[i].checked == true){
                    alert(check[i].value)
                }}};
```
## 5/BẮT SỰ KIỆN ONCHANGE CỦA THẺ SELECT:
```HTML
        <p>chọn giới tính</p>
            <select id="list"  onchange="valueList(this)">
                <option value=" ">----Lựa chọn----</option>
                <option value="male">Nam</option>
                <option value="female">Nữ</option>
            </select>
         <p style="color: blue;" id="text"></p>
```
```JS
        function valueList(obj){
            var value = obj.value;
            var text = document.getElementById('text');
            if(value == ' '){
                text.innerHTML = 'Vui long chon';
            }else if(value == male){
                 text.innerHTML = 'Ban da chon nam';
            }else{
                 text.innerHTML = 'ban da chon nua';}
```
## 6/LẤY GIÁ TRỊ THẺ SELECT MULTIPLE:
```HTML
         <h3>Chọn các mục từ danh sách dưới đây</h3>
                < !--  multiple được bỏ vào giúp chọn nhiều mục -->
             <select name="value" id="list" multiple onchange = "selectBox(this)">
                <option value="con chó">con chó</option>
                <option value="con mèo">con mèo</option>
                <option value="con lợn">con lợn</option>
                <option value="con gà">con gà</option>
                <option value="con bò">con bò</option>
            </select>
            <p id="listText" style="color: red">Các mục được in ra</p>
```
```js
        function selectBox(obj){
            var list = obj.children;
            var result =' ';
            for(var i= 0; i< list.length; i++){
// thuộc tính selected được sử dụng để kiểm tra trạng thái
//của mỗi mục trong danh sách chọn và xác định xem chúng có được chọn hay không.
                if(list[i].selected){
                     result += '<li>' + list[i].value + '</li>'   
                }}
                document.getElementById('listText') = result }
```
## 7/CHUYỂN ĐỔI PHẦN TỬ CỦA 2 THẺ SELECTE MULTIPLE
```HTML
     <h3>Chọn các mục từ danh sách dưới đây</h3>
         <select multiple id="left">
                <option value="tin công nghệ">Tin công nghệ</option>
                <option value="tin thời sự">Tin thời sự</option>
                <option value="tin quốc tế">Tin quốc tế</option>
                <option value="tin thể thao">Tin thể thao</option>
                <option value="tin nông nghiệp">Tin nông nghiệp</option>
        </select>
        <input type="button" id="left-right" value="<<" onclick="leftRight(1)"/>
        <input type="button" id="right-left" value=">>" onclick="leftRight(2)"/>
       <select multiple id="right"></select>
```
```CSS
         select{
            padding: 10px;
            width: 200px;
            height: 200px;}
         select option{
            padding: 5px;}
```
```JS
            function leftRight(type){
                if(type === 1){
                    var left = document.getElementById('right');
                    var right = document.getElementById('left');
                }else{
                    var left = document.getElementById('right');
                    var right = document.getElementById('left');
                    selectCategory(left, right)}}
                function selectCategory(left,right){
                    var option = left.children;
                    var result = [];
                        for(var i =0; i <  optiom.length; i++){
                            if(option[[i].selected){
                                result.push(option[i])}}
                        for(var j=0; j < result.length; i++){
                                rightt.appendChild(result[j])}}
```
## 8/TRUYỀN MẢNG VÀO HÀM:
```JS
//Loại thông thường:
                var arr = [3,4,5,6,7];
                function showArr(element){
                    console.log(element); 
                }
                showArr(arr);
//Loại truyền tham số vô hạn:
                var food = ['chicken','noodle','meat'];
                function showFood(a,b,c){
                        console.log(a,b,c);}
                    //a,Truyền mảng thủ công:
                     showFood(food[0], food[1], food[2]);
                   //b,Truyền mang vào hàm apply:
                     showFood(null(or showFood), food);
                   //c,Cách sử dụng es6:
                      showFood(...food);
//Tìm số lớn nhất trong mảng:
                var numbers1 = [1,2,3,4,5];
                var numbers2 = [3,6,7,8,9];
             console.log(Math.max(...numbers1,...numbers2);
```
## 9/LẤY ĐỘ DÀI OBJECT:
```JS
             a,var listObj = new Object();
                    listObj['name'] = 'Hoang',
                    listObj['id'] = 2;
                    listObj['address'] = 'Ha Noi';
             b, var listObj = {
                    name: 'Hoang',
                    id: 20,
                    address: Ha Noi  
                };
                // Lấy ra object:
                console.log(listObj);
                // Lấy độ dài ob:
                console.log(Object.key(listObj).length);
```
## 10/GỘP 2 OBJECT LẠI VỚI NHAU:
```JS
            var listAni = {
                    name: 'parrot', legs: 2, wings: 2, 
                };
            var listAni1 = {
                    address: 'jungle', bookred: 'no',fly: 'yes'
                };
            //Gộp object có key trùng nhau sẽ bị ghi đè.
                var list = {...listAni, ...listAni1};
            //Ngoài ra còn sử dụng hàm assign() trộn 2 object:
                var list1 = Object.assign(listAni, listAni1);
```
## 11/CÁCH LẤY NGÀY GIỜ TRONG JS:
```html
            <div id=day></div>;
```
```JS
            var total = new Date();
            console.log(total.getFullYear());
            console.log(total.getMonth()+1);
            console.log(total.getHours());
            console.log(total.getSeconds());
            document.getElementById('day').innerHTML = total;
            //Lấy ngày trước đó
                total.setDate(total.getDate() -1);// ngày trước đó
                var yesterday = total.getDate(); // lấy ngày trong đối tượng day
                    console.log(yesterday);
// Ngoài ra có thể sử dụng phương thức setYear(), setMonth(), setHour,Minutes,Seconds().
```
## 12/TẠO SỐ NGẪU NHIÊN TRONG JS:
```JS
            //random 0->9;
                Math.floor(math.random()*10);
            //random 0->100
                Math.floor(math.random()*101);
            //random 1-> 10
                Math.floor(math.random()*10) +1;
            //random 1-> 100
                Math.floor(math.random()*100) +1;
//random min-max
// Random trong phạm vi min và max không bao gồm hai số đó.
              function getRandom (min,max){
                    return Math.floor(Math.random()*(max-min))+1
                }                     
//Tạo số ngẫu nhiên trong phạm vi min - max bao gồm cả hai số đó.
                 function getRandom2(min,max){
                    return Math.floor(Math.random()*(max-min+1))+1
                }
```
## 13/CÁCH ÉP KIỂU DỮ LIỆU:
+ **5 kiểu dữ liệu đơn giản**:  *string, number,boolean, object, function*

+ **6 kiểu dữ liệu object**:   *object, date, array, string, number, boolean*

+ **2 kiểu dữ liệu không chứa dữ liệu nào cả**:  *null, undefined*

+ **NaN** *là Number*

+ **Null** *là 1 object*

+ **Undefined** *Biến chưa gán dữ liệu, biến chưa được khai báo*
***
## 14/TÌM MIN &MAX TRONG MẢNG:
```JS
             var arr = [20, 40, 60,28, 49];
              var arrMax = Math.max.apply(Math, arr);
                console.log(arrMax);
                var arrMin = Math.min.apply(Math, arr);
                console.log(arrMin);
```
## a,Cắt mảng sử dụng thuộc tính length:
```js
              var result = [23,54,6,74,77,25,98,98];
//Giảm độ dài mảng:
                result.length = 4;
//Tăng độ dài mảng:
                result.length = 10;
//Thiết lập mảng rỗng:               
               result.length = 0;
//Hoặc
                result = [];
```
## b,Xóa phần tử mảng
```js
//Trường hợp này dùng xóa phần tử của mảng chứ không xóa tổng độ dài mảng;
//Vị trí xóa undefined
        delete result[3];
//Trường hợp xóa luôn phần tử:
        result.splice(1(start),1(length))
  
```
## 15/SỬ DỤNG DOM TRUY VẤN HTML
## TRUY VẤN THEO ID:

*var element = document.getElementById('id')*

*Kết quả trả về 1 object html*

## TRUY VẤN THEO CLASS NAME, TAG NAME, NAME:

*var element1 = document.getElementsByClassName('class')*

*var element2 = document.getElementsByTagName('tag')*

*var element3 = document.getElementsByName('name')*

*Đều trả về 1 mảng object*

>Khi truy vấn mà trả về 1 mảng phải sử dụng vòng lặp để xử lí phần tử

## SỬ DỤNG QUERRYSELECTOR

*document.querySelector('selector) *
## 16/TẠO THÔNG BÁO CONSOLE:
```JS
            console.log('%cTEXT', 'PROPERTY: VALUE';
//EXP:
            console.log('%cStop', "color: green; font-size: 20px; font-family: san-serif;")   
```
## 17/TRY CATCH 

>Là 1 khối lệnh dùng để bắt lỗi chương trình trong js.
>Sử dụng khi không muốn chương trình bị dừng.
>Lỗi do người dùng nhập sai dữ liệu or người dùng thao tác bị sai.
>Tham số e trong catch chính là error object.
>Trường hợp này ta sẽ sử dụng lệnh throw để quăng lỗi.
>throw new Error('Nội dung thông báo lỗi');
```js
                try{
                    // Quăng lỗi vào
                    throw('Noi dung loi');
                }catch (e){
                    //Đón nhận lỗi và in ra
                    // Vị trí này chỉ chạy ở try có quăng lỗi hoặc ở try
                    // Sử dụng sai cú pháp
                    console.log(e.message);
                }finally{
                    // Cuối cùng chạy cái này
                    // Luôn chạy sau cùng
                    console.log('End');
                }
```
## 18/GLOBAL FUNCTION:
## a,isFinite: 
+ Có chức năng kiểm tra 1 giá trị có phải là 1 số hữu hạn hay 1 số hợp lệ hay không.
+ Giá trị truyền vào dương, âm, giá trị NaN phương thức trả về false, true.
> isFinite(value), value(4:true, 'hello': false);
## b,isNaN:
+ Kiểm tra điều kiện giá trị truyền vào có phải hợp lệ hay k
+ Trả về True nếu giá trị NaN
+ Sẽ chuyển đổi tham số truyền vào thành kiểu số sau đó kiểm tra nó.
> isNaN(value);
## c,Number()
+ Chức năng chuyển đối đối tượng thành 1 số
+ Số này đại diện cho giá trị đối tượng được cung cấp
+ Đối tượng truyền vào không chuyển thành 1 số thì NaN sẽ được trả về.
> Number(obj); obj đối tượng cần chuyển đổi
+ exp:  obj: 12heje: NaN, Date(): 1497781501126
## d,parseFloat()
+ Sẽ phân tích 1 chuỗi được cung cấp và trả về 1 giá trị số
+ Chuỗi bắt đầu bằng nguyên, số thập phân trả về số đó
+ Chuỗi bắt đầu khoảng trắng, phương thức sẽ loại bỏ khoảng trắng đó.
+ Chuỗi bắt đầu bằng 1 dấu chấm và theo sau 1 số tự động coi là số thập phân.
+ Nếu kí tự đầu tiên của chuỗi tryền vào không thể chuyển thành 1 số, trả về NaN.
> parseFloat(string); string là chuỗi cần phân tích
> 12gdh: 12, 344-334: 344, .443: 0.443, frew: NaN, ...444: NaN;
## e,parseInt():
+ Sẽ phân tích 1 chuỗi và trả về 1 số nguyên nếu có.
+ Chỉ trả về 1 số nguyên kể cả chuỗi bắt đầu bằng 1 số thập phân
+ Nếu chuỗi được bắt đầu bằng 1 dấu chấm trả về NaN
+ Các khoảng trắng ở đầu và cuối chuỗi không ảnh hưởng đến kết quả
+ Kí tự đầu tiên chuỗi không chuyển number phương thức trả về NaN.
> parseInt(string, radix(tham số không bắt buộc))
> 12fjh: 12, .4444: NaN, ffdsdsh: NaN, 1234 ge fdjh: 1234.
 ## f,String();
+ Sẽ chuyển đổi giá trị của đối tượng được cung cấp thành 1 chuỗi.
+ Trả về 1 chuỗi đại diện cho giá trị đối tượng
+ Trả về kết quả tương tự như khi gọi phương thức toString();
> String(obj) obj là đối tượng cần chuyển đổi
> ex:12dfsd: 12, 123: 123, boolean(0): false,...

## 19/NUMBER FUNCTION:
## a,ISFINITE:
+ Có chức năng kiểm tra một giá trị có phải số hữu hạn hay không
+ Các số thực có giá trị hữu hạn
+ Trả về true thuộc kiểu Number và tương đương với 1 sồ hữu hạn
+ Kiểm tra luôn giá trị không chuyển giá trị như isFinite
> Number.isFinite(value)

## b,ISINTEGER:
+ Kiểm tra 1 giá trị có thuộc kiểu số nguyên không
+ Trả về true nếu thuộc kiểu số nguyên
> Number.isInteger(value)
> ex: -2,'10/3', 'fdhjs', true: false

 ## c,NUMBER.ISNAN()
 + Sẽ kiểm tra giá trị truyền vào có phải là 1 giá trị NaN(0 phải số) hay không.
 + 1 tạo NaN:
- Lấy 0/0
- infinity/infinity
- infinity.0
- Bất kì phép toán nào đó NaN là một toán hạng
- Chuyển đổi 1 xâu non-numeric hoặc undefined về dạng number
+ NaN thuộc kiểu number
+ Trả về false bất kì giá trị nào thuộc kiểu number
> Number.isNaN(value)
> ex: 123, 10/2, -4, 1/6/2017: false

## d,NUMBER.TOFIXED()
+ Chuyển đổi 1 số thành kiểu chuỗi, giữ lại số chữ số thập phân do người dùng xác định
+ Số thập phân lớn hơn số truyền vào trả về null
> number.toFixed(x); x: số thập phân mong muốn
> 144,34234 cho fixed(2): 144,34

## e,NUMBER.TOSTRING()
+ Sẽ chuyển đổi 1 số thành 1 chuỗi, ép kiểu cho giá trị truyền vào thành 1 giá trị 
thuộc kiểu string;
> number.toString(radix)
> là tham số không bắt buộc 2-36 

## e,NUMBER.VALUEOF()
+ Sẽ trả về giá trị gốc của số truyền vào
+ Phương thức không có giá trị truyền vào
