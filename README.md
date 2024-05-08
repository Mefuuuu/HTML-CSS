
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
