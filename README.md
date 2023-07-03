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
