
# HTML
    1. h1 - h6 - heading
    2. p - paragraph
    3. img - image
    4. a - anchor
    5. ul, li - unordered list, list item
    6. table
    7. input
    8. button
    9. div  

# CSS

Gồm 3 cách: 

    1. Internal: sử dụng cặp thẻ Style đặt trực tiếp trong file HTML và viết CSS trong cặp thẻ đó
    2. External: tạo 1 file .CSS bên ngoài và liên kết lại bằng thẻ Link
    3. Inline: Đưa thẳng Attribute vào trong thẻ muốn chỉnh sửa trong file HTML

- CSS celectors: là các cách chúng ta sử dụng để chọn ra các phần tử (elements) mà chúng ta muốn "style" cho chúng. Có 2 CSS selectors thân thuộc với chúng ta nhất là id và class.
  + ID & Class: ID thì dùng #, class thì dùng .
  + ![image](https://github.com/Mefuuuu/HTML-CSS/assets/133778142/6a688877-16ba-4a08-be54-3f681c579109)
 
- Priority? (sự ưu tiên)
  + Internal vs External: Ai gọi trước sau thì lấy
  + !Important: ghi đè lên mọi thứ
  + Inline - 1000
  + #id - 100
  + .class - 10
  + tag -1
  + Equal specificity: Nếu trong thẻ không có Inline thì khi gọi trùng thì thay đổi nào gọi sau sẽ được lấy
  + Universal selector and inherited: cả 2 đều 0đ, đều có thể được ghi đè lên

- Variable

  Biến trong CSS tạo ra để dễ thay đổi thuộc tính với số lượng lớn
  
```c
:root{
    --text-color: violet;
} // Đặt biến

.second-heading {
    color: var(--text-color);
    font-size: 20px;
} // sử dụng biến
```
- CSS UNIT
  + Absolute units:
    
    .px
    
    .pt
    
    .cm
    
    .mm
    
    .inch ...
    
  + Relative units:
    
    .%
    
    .rem
    
    .em
    
    .vw
    
    .vh
      
- Reset margin được đặt mặc định:
```c
* {
    margin: 0; /* Loại bỏ margin mặc định */
    padding: 0; /* Loại bỏ padding mặc định */
}
```
- CSS Functions
  + var()
  + linear-gradient()
  + rgba()
  + rgb()
  + calc()
  + attr()

- CSS pseudo-classes
  + :root
  + :hover : kích hoạt khi di chuột vào
  + :active : kích hoạt khi bấm vào
    ```c
    .box:active{
            background-color: aquamarine;
        }
    ```
  + :first-child
  + :last-child
    
- Pseudo-elements
  + ::before
  + ::after
    ```c
    .box::after{
            content: "";
            display: block;
            width: 50px;
            height: 50px;
            background-color: bisque;
        }
    ```
  + ::first-letter
  + ::first-line
  + ::selection
- CSS Padding: Phần đệm, có làm tăng kích thước của Element
  
  ![image](https://github.com/Mefuuuu/HTML-CSS/assets/133778142/4ca492d0-9ecd-4c89-881f-b5a66bfdc2fd)
- CSS Border: đường viền
  + Mặc định border-width là medium, thông thường sẽ tương ứng với 3px
  + border-style: solid; //nét thẳng
  + border-style: dashed; //nét đứt
  + border: 10px solid #333; // cách viết ngắn gọn
- CSS Margin (khoảng cách lề): Không làm tăng kích thước như 2 cái trên, có thể rút gọn như Padding
- CSS Box-sizing: Có tác dụng giữ nguyên tổng kích thước khi sử dụng Padding và Border
  + box-sizing: border-box; // giữ kích thước
  + box-sizing: unset; //Thiết lập lại
  + box-sizing: content-box; //trở về khi ko set boxsizing
- CSS Background-image 
  +  background-image: linear-gradient(180deg, rgba(255, 255, 0, 0.4), rgba(0, 255, 255, 0.4)); //Tạo background với dãy màu chuyển, Nếu bỏ trống chỗ xoay thì mặc định 180 độ
  +  background-size: 100%; //size
  +  background-size: contain; //Thay đổi kích thước hình nền để đảm bảo hình ảnh hiển thị đầy đủ
  +  background-size: cover; // Thay đổi kích thước hình nền để bao phủ toàn bộ vùng chứa, ngay cả khi phải kéo dài hình ảnh hoặc cắt bớt một chút ở một trong các cạnh . demo: https://www.w3schools.com/cssref/playdemo.php?filename=playcss_background-size&preval=cover
  +  background-repeat: no-repeat; //tránh sự lặp lại của ảnh, nếu dùng repeat có thể tạo background với ảnh lặp lại

![image](https://github.com/Mefuuuu/HTML-CSS/assets/133778142/87fbeccb-b618-4e6c-be94-4954850e5525)

- CSS Background-origin: Tương tự như Background-clip khi học color. Sẽ đổ Background lên các phần như content, border, padding
  + background-origin: content-box;
  + background-origin: border-box;
  + background-origin: padding-box;
- CSS Background-position: Vị trí, Khi không ghi gì thì sẽ là center
- CSS Background shorthand: Rút gọn code
  + background: url(...) no-repeat center / contain; //trước background-size phải có dấu /
- CSS Positon: Relative : là vị trí tương đối không phụ thuộc vào ai cả
```c
        h1{
            position: relative;
            top: 100px;
            left: 100px;
        }
```
- CSS Position: Absolute: vị trí tuyệt đối dùng khi có 1 đối tượng là con của 1 đối tượng khác và cần di chuyển vị trí đối tượng con xung quanh đối tượng cha (khi 1 đối tượng phụ thuộc vào đối tượng khác)
  + Thẻ con chỉ cần biết thẻ cha gần nhất có sử dụng position
  + Thường được dùng để làm mờ như ảnh:
    
    ![image](https://github.com/Mefuuuu/HTML-CSS/assets/133778142/95550614-e645-48fc-86f4-2c66c54a12f7)
- CSS Position: Fixed: (khi 1 đối tượng phụ thuộc vào trình duyệt) thường dùng khi đính Header lên đầu
  + ```c
    .header{
            width: 100vw;
            height: 120px;
            background-color: black;
            position: fixed;
            top: 0;
        }
    ```
- CSS Position: Sticky: (hạn chế dùng, tại nhiều trình duyệt không hỗ trợ)

- More:
  + letter-spacing: 4px; // tăng khoảng cách các chữ
  + text-align: center; // căn giữa 
  + text-align: justify; // căn giữa đoạn văn 2 bên
  + Sau khi padding dùng 
    margin-left: auto;
    margin-right: auto; // để căn content ra giữa map
  + font-weight: 500; // giới hạn đến 700 chỉnh độ đậm nhạt của chữ
  + cursor: pointer; chỉnh hình con trỏ chuột
  + text-transform: uppercase; // In hoa chữ
  + font-family: Arial, Helvetica, sans-serif; // chỉnh font chữ
  + font-style: italic; // in nghiêng
  + opacity: 0.6; // chỉnh độ trong suốt
  + line-height: 1.4; // tăng khoảng cách dòng trong đoạn văn 
  + text-decoration: none; // bỏ gạch chân
  + display: flex;
    align-items: center;    // giữa chiều cao
    justify-content: center;    // giữa chiều rộng
