# exam
# 1/LẤY GIÁ TRỊ CHECKBOX:
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
