# Bài tập lớn — Nền tảng lập trình cho phân tích và trực quan dữ liệu

Landing page và các trang bài tập lớn con của nhóm.
Đại học Bách Khoa – ĐHQG-HCM · Khoa Khoa học và Kỹ thuật Máy tính
Học kỳ 261, năm học 2026–2027 · Giảng viên: Lê Thành Sách

## Cấu trúc

| Tệp | Nội dung |
|---|---|
| `index.html` | Landing page — thông tin môn học, nhóm, mục lục bài con |
| `tabular.html` | Bài con 1 — dữ liệu bảng (bắt buộc) |
| `text.html` | Bài con 2 — dữ liệu văn bản (bắt buộc) |
| `image.html` | Bài con 3 — dữ liệu ảnh (tự chọn) |
| `styles.css` | Giao diện dùng chung |

Nhóm 3 người làm 3 loại dữ liệu: Tabular + Text bắt buộc, cộng một bài tự chọn
trong Image / Multimodal / Time series. Nếu nhóm đổi bài tự chọn, đổi tên
`image.html` và sửa mục tương ứng trong `index.html`.

## Danh sách cần điền trước khi nộp

### Landing page (`index.html`)

- [ ] Thay `<Tên nhóm>` ở tiêu đề, dòng đầu trang và footer — **phải trùng
      khớp sheet GroupRegistration**
- [ ] Thay MSSV X / Y / Z bằng mã số thật
- [ ] Sửa vai trò từng thành viên cho khớp phân công thực tế
- [ ] Thay link GitHub cá nhân từng người, hoặc **xóa hẳn dòng `.gh`** nếu
      không có — đề bài ghi rõ không tạo link giả
- [ ] Thay link kho mã nguồn ở footer

### Mỗi trang bài con

- [ ] Link notebook Colab (kiểm tra chạy được Run all từ tài khoản khác)
- [ ] Link PDF report của bài đó
- [ ] Link video YouTube, chế độ Public hoặc Unlisted
      (gợi ý tiêu đề: `[Tên nhóm] – [Loại dữ liệu] – Nền tảng lập trình`)
- [ ] Viết đoạn mô tả bài toán và điền bảng thông số tập dữ liệu
- [ ] Kiểm tra tập dữ liệu đạt ngưỡng: bảng ≥ 2000 mẫu và 10 cột;
      văn bản ≥ 2000 mẫu; ảnh ≥ 5000 ảnh và ≥ 3 lớp

### Nộp thêm trên LMS

- [ ] Một thành viên nộp PDF tổng hợp, đặt tên `<groupname>-report.pdf`

## Thang điểm để đối chiếu

| Thành phần | Trọng số |
|---|---|
| Chất lượng notebook `.ipynb` | 50% |
| Báo cáo, giải thích, Markdown | 20% |
| Video demo và trình bày | 15% |
| Sáng tạo, mở rộng, kết luận | 10% |
| Hình thức nộp (trang này) | 5% |

Mục 10 điểm sáng tạo yêu cầu **mỗi loại dữ liệu** có ít nhất một hình trả lời
một câu hỏi cụ thể, caption ghi kết luận, và có số liệu đối chiếu
(trước/sau xử lý, mô hình A so với B, mẫu đúng so với mẫu sai). Đổi màu hay
thêm word cloud mà không nêu được điều gì thì không tính điểm.
