# Track Việc

Todo list cá nhân có chia việc thành subtask, ghi input cần chuẩn bị cho từng subtask, log thời gian thực tế đã làm, và thanh tiến độ theo %.

## Xem trực tiếp

https://chuoiuhuhu0727.github.io/track-viec/

## Tính năng

- Chia mỗi việc thành các việc con (subtask).
- Mỗi việc con có ô "input cần chuẩn bị" — ghi rõ cần tài liệu/thông tin gì trước khi bắt đầu.
- Ghi nhận thời gian đã làm cho từng việc con (cộng dồn theo từng lần log, xem lại lịch sử được).
- Thanh tiến độ % theo số việc con đã xong, cả ở từng việc lẫn tổng toàn bộ danh sách.
- Gắn nhãn ưu tiên thủ công: must-have / nice-to-have, bấm vào badge để đổi.

- Việc mới tạo tự lên đầu; mỗi việc có ngày tạo, ngày hạn, nút lên/xuống.
- Thanh "tiến bộ hôm nay so với hôm qua": điểm = việc con xong + phút làm / 30 + điểm các ý đã học (Nhớ 1đ / Hiểu 2đ / Tư duy 3đ).
- Nhật ký ngắn: ghi chú có nhãn (vd `internship`), lọc theo nhãn, ghi chú loại "Ghi chú" không tính điểm.
- Đồng bộ qua repo GitHub + xuất/nhập file JSON.

## Về việc lưu dữ liệu

Dữ liệu luôn lưu ở `localStorage` của trình duyệt (xoá cache là mất), nên có hai cách giữ an toàn:

1. **Xuất/nhập JSON** — mục "Đồng bộ GitHub & sao lưu" ở cuối trang.
2. **Đồng bộ GitHub** — app ghi file `data.json` vào một repo dữ liệu (nên là repo riêng, **không phải repo này**). Cần fine-grained token chỉ cấp cho repo đó, quyền *Contents: read & write*. Token nằm trong trình duyệt, không commit lên đâu cả. Khi cả hai bên cùng thay đổi, app hỏi lấy bản nào.

## Về tính năng AI gợi ý ưu tiên

Nút "Nhờ AI phân loại ưu tiên" gọi thẳng Claude qua một capability chỉ chạy được khi trang mở bên trong Claude Artifact — trên GitHub Pages (static, không backend, không API key) tính năng này không hoạt động và sẽ hiện thông báo giải thích khi bấm vào. Nếu muốn dùng tính năng AI đầy đủ + lưu dữ liệu đồng bộ nhiều máy, dùng bản Claude Artifact.

## Chạy local

Không cần build gì cả, mở thẳng `index.html` bằng trình duyệt là chạy được.

---

Built with [Claude](https://claude.com/claude-code).
