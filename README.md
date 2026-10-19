## **Phần 1 (Phân tích)**
## 3 quy tắc vàng mà bảng tính hiện tại đang vi phạm:
- Header duy nhất
- Không hàng trống
- Dữ liệu nguyên tử / sạch
# **Phần 2 (Hoàn thiện)**
## Bước 1: Gỡ bỏ Merge Cell ở hàng tiêu đề
- Chọn các ô tiêu đề đang bị gộp.
- Vào Home → Merge & Center → Unmerge Cells.
- Nhập lại tên cho từng cột, mỗi cột một Header riêng, ngắn gọn (ví dụ: Ma_TB, Ten_TB, Vi_Tri, Trang_Thai).
## Bước 2: Xóa hàng trống
- Chọn toàn bộ vùng dữ liệu, nhấn F5 → Special → Blanks (hoặc Ctrl + G → Special → Blanks) để chọn các ô trống.
- Chuột phải → Delete → Entire row.
## Bước 3: Làm sạch cột "Trạng thái" bằng TRIM()
### Giả sử cột Trạng thái là cột D, dữ liệu bắt đầu từ dòng 2, tạo thêm một cột phụ (ví dụ cột E):
- Tại ô E2 nhập: =TRIM(D2)
- Nhấp đúp vào Fill Handle (góc dưới phải ô E2) để điền xuống hết các dòng.
- Chọn toàn bộ cột E → Ctrl + C → chuột phải tại cột D → Paste Special → Values (để dán giá trị, bỏ công thức).
- Xóa cột phụ E.
## Bước 4: Bật lại AutoFilter trên toàn vùng
- Nhấp vào một ô bất kỳ trong bảng (hoặc Ctrl + A chọn vùng liên tục).
- Nhấn Ctrl + Shift + L (nếu Filter đang bật sai vùng thì nhấn 2 lần để tắt rồi bật lại).
- Bấm mũi tên cột "Trạng thái": lúc này chỉ còn một giá trị "hỏng". Tích chọn là lọc đúng toàn bộ thiết bị hỏng.