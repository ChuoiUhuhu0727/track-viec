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

## Về việc lưu dữ liệu

Bản này là static site thuần (không có backend), nên dữ liệu lưu bằng `localStorage` — chỉ nằm trên trình duyệt cậu đang dùng, không đồng bộ giữa các máy/thiết bị khác nhau. Xoá cache trình duyệt hoặc đổi trình duyệt khác sẽ mất dữ liệu.

## Về tính năng AI gợi ý ưu tiên

Nút "Nhờ AI phân loại ưu tiên" gọi thẳng Claude qua một capability chỉ chạy được khi trang mở bên trong Claude Artifact — trên GitHub Pages (static, không backend, không API key) tính năng này không hoạt động và sẽ hiện thông báo giải thích khi bấm vào. Nếu muốn dùng tính năng AI đầy đủ + lưu dữ liệu đồng bộ nhiều máy, dùng bản Claude Artifact.

## Chạy local

Không cần build gì cả, mở thẳng `index.html` bằng trình duyệt là chạy được.

---

Built with [Claude](https://claude.com/claude-code).
