# Bài tập lớn — Nền tảng lập trình cho phân tích và trực quan dữ liệu

Landing page và các trang bài tập lớn con của nhóm.
Đại học Bách Khoa – ĐHQG-HCM · Khoa Khoa học và Kỹ thuật Máy tính
Học kỳ 261, năm học 2026–2027 · Giảng viên: Lê Thành Sách

## Cấu trúc

| Tệp | Nội dung |
|---|---|
| `index.html` | Landing page — thông tin môn học, 3 bài con, kết quả nổi bật, nhóm |
| `tabular.html` | Bài con 1 — dữ liệu bảng (bắt buộc), nhúng toàn bộ kết quả notebook |
| `text.html` | Bài con 2 — dữ liệu văn bản (bắt buộc) |
| `image.html` | Bài con 3 — dữ liệu ảnh (tự chọn) |
| `styles.css` | Giao diện dùng chung (Be Vietnam Pro / Newsreader / JetBrains Mono, có dark mode) |
| `01_Tabular_Customer_Churn.ipynb` | Notebook bài 1, đã chạy đủ output |
| `assets/tabular/` | 14 hình trích từ output của notebook bài 1 |

Nhóm 3 người làm 3 loại dữ liệu: Tabular + Text bắt buộc, cộng một bài tự chọn
trong Image / Multimodal / Time series. Nếu nhóm đổi bài tự chọn, đổi tên
`image.html` và sửa mục tương ứng trong `index.html`.

### Cập nhật hình khi chạy lại notebook

Số liệu trên `tabular.html` và mục "Kết quả nổi bật" của `index.html` được chép
tay từ output notebook. Sau khi chạy lại notebook, trích lại hình bằng:

```python
import json, base64
nb = json.load(open('01_Tabular_Customer_Churn.ipynb', encoding='utf-8'))
# chỉ số cell -> tên file, giữ đúng thứ tự hình trong cell
names = {9: ['missing'], 11: ['numeric-dist'], 13: ['categorical'], 15: ['target'],
         17: ['correlation'], 21: ['churn-by-category', 'churn-by-numeric'],
         32: ['scaling'], 37: ['class-weight'], 42: ['threshold'], 45: ['test-eval'],
         47: ['improvement-steps'], 50: ['feature-importance'], 53: ['error-by-age']}
for i, ns in names.items():
    imgs = [o for o in nb['cells'][i]['outputs'] if 'image/png' in o.get('data', {})]
    for n, o in zip(ns, imgs):
        open(f'assets/tabular/{n}.png', 'wb').write(base64.b64decode(o['data']['image/png']))
```

rồi đối chiếu lại các con số trong hai trang HTML.

## Danh sách cần điền trước khi nộp

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
