# AI Log - Lab 4 Portfolio CV

## Báo lỗi đã phát hiện

### 1) Meta viewport bị sai cú pháp
- Vị trí: `index.html` trong `<head>`
- Mã hiện tại: `content="width=divice-width, initail-scale=1"`
- Lỗi: từ `divice` viết sai thành `device`, `initail` viết sai thành `initial`, và giá trị `width=device-width` chưa đúng chuẩn.
- Hệ quả: trên thiết bị di động, trình duyệt có thể không hiểu đúng viewport, khiến trang bị phóng to hoặc tràn ngang.

### 2) HTML trong danh sách liên hệ thiếu thẻ đóng `<li>`
- Vị trí: phần `Liên hệ` trong `index.html`
- Mã hiện tại:
  ```html
  <li><strong>Email:</strong>
  <li><strong>GitHub:</strong> <a href="#">github.com/minhan-demo</a></li>
  ```
- Lỗi: dòng đầu tiên không có `</li>` đóng, làm cấu trúc danh sách HTML sai.
- Hệ quả: DOM không hợp lệ, layout và định dạng có thể bị xấu/không đồng nhất.

### 3) Selector CSS `.img` không khớp với phần tử thực tế
- Vị trí: `css/style.css`
- Mã hiện tại:
  ```css
  .img {
    max-width: 100%;
    height: auto;
  }
  ```
- Lỗi: không có phần tử nào có class `img`; ảnh thực tế dùng `class="avatar"` và thẻ `img`.
- Hệ quả: quy tắc này không được áp dụng, dẫn đến hình ảnh có thể không tối ưu hóa kích thước trên màn hình nhỏ.

### 4) Thiếu tính responsive cơ bản ở đầu dự án
- Vị trí: `index.html`, `css/style.css`
- Đánh giá: cấu trúc và CSS hiện tại mới dùng các kiểu desktop-first và có dấu hiệu không tối ưu cho mobile, dù đã có một phần media query.
- Hệ quả: trang có thể đáp ứng tốt trên màn hình lớn nhưng chưa chắc ổn trên 320px mà không tối ưu tiếp tục cho mobile-first.

## Tóm tắt
Các lỗi trên chủ yếu nằm ở thiết lập viewport, cấu trúc HTML và tối ưu ảnh/CSS. Nếu tiếp tục phát triển phần responsive theo Lab 4, cần sửa ngay các vấn đề này trước khi kiểm thử trên mobile.
