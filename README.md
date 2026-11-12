# KSCL Showroom · VinFast SAMCO Bình Tân

https://kscl.vinfastsamcobinhtan.com · bản **v3.4**

## Kiến trúc
Giao diện (GitHub Pages) → Apps Script (link `/exec` trong `config.js`) → Google Sheet + Drive.
Code Apps Script (`.gs`) **không** để ở repo này; bản lưu nằm ở repo riêng tư `samco-apps-script`.
App một file (`index.html`), không dùng samco-core. Ảnh chụp và báo cáo lưu trong thư mục Drive "Kiểm soát chất lượng".

## Đường dẫn
| Link | Ai dùng | Nội dung |
|---|---|---|
| `/` | Người kiểm, các bộ phận | Kiểm tra 105 tiêu chí VinFast SR_4_026 (Ngày / Tuần / Tháng), báo cáo + PDF, việc cần xử lý |
| `/?trang=khac-phuc` | Bộ phận được giao lỗi | Cập nhật khắc phục |
| `/quanly`, `/khac-phuc` | link cũ | Tự chuyển về đúng trang |

## File
| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ giao diện |
| `config.js` | Link `/exec` của Apps Script |
| `icon.svg`, `icon-180.png`, `favicon.ico` | Biểu tượng |
| `logo.png` | Logo SAMCO trên báo cáo |
| `quanly.html`, `khac-phuc.html` | Trang chuyển hướng |
| `CNAME` | Tên miền |

## Google Sheet
`TieuChi` (105 tiêu chí, cột Lộ trình) · `AnhMau` (64 ảnh mẫu, cột Mã tiêu chí) · `BoPhan` · `Xe` · `BaoCao` · `ChiTiet` · `ViecCanXuLy`

## Cập nhật
1. Sửa Apps Script → Lưu → Triển khai → Quản lý các bản triển khai → bút chì → **Phiên bản mới** → Triển khai. Link `/exec` giữ nguyên.
2. Tải file giao diện lên repo này (nhánh `main`). GitHub Pages cập nhật sau 1–2 phút.
3. Đổi link Apps Script: chỉ sửa `config.js`.

## Phiên bản
- v3.4: ảnh chụp theo từng tiêu chí; tự xóa phiếu nháp cũ hơn 60 ngày; link Apps Script chuyển sang `config.js`.
- v3.2: bộ tiêu chí VinFast SR_4_026, lộ trình 13 khối, 64 ảnh mẫu, điểm VinFast x/105 + PDF.
- v2: giao lỗi, hạn xử lý, khắc phục, xác nhận.
