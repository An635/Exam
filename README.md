# exam
#1/LẤY GIÁ TRỊ CHECKBOX:
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
#2/BẮT SỰ KIỆN CHECKBOX:
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
#3/TẠO CHECKALL:
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
#4/LẤY GIÁ TRỊ RADIO:
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
#5/BẮT SỰ KIỆN ONCHANGE CỦA THẺ SELECT:
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
#6/LẤY GIÁ TRỊ THẺ SELECT MULTIPLE:
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
#7/CHUYỂN ĐỔI PHẦN TỬ CỦA 2 THẺ SELECTE MULTIPLE
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
#8/TRUYỀN MẢNG VÀO HÀM:
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
#9/LẤY ĐỘ DÀI OBJECT:
```JS
             a,   var listObj = new Object();
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
                
 

