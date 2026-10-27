# K26CNTT2_IT108_Session08_Ex06.no1
Bài tập số 6
# Bài tập 6: Phân tích sự cố tài liệu dự án trên GitHub

## Phần 1. Phân tích các sai lầm và ưu thế của Markdown

### 1. hai sai lầm trong tư duy của Nam khi dùng file Rich Text (.docx)
- **Không hỗ trợ xem trực tiếp trên GitHub:** File Word (`.docx`) là file định dạng nhị phân (Binary file/Rich Text). GitHub không thể dịch và hiển thị nội dung file `.docx` trực tiếp trên giao diện trình duyệt, buộc người dùng phải tải về máy mới đọc được.
- **Gây lỗi xung đột (Conflict) toàn bộ file khi dùng Git:** Vì `.docx` lưu trữ cấu trúc dưới dạng gói nhị phân phức tạp, Git không thể theo dõi sự thay đổi theo từng dòng chữ (line-by-line). Do đó, chỉ cần Nam chỉnh sửa một dấu phẩy, Git sẽ hiểu là toàn bộ file bị thay đổi và báo xung đột trên toàn bộ tập tin.

### 2. Tại sao Markdown an toàn và nhẹ hơn?
- **Dung lượng siêu nhẹ & Chống hư hại file:** Markdown là dạng văn bản thô (Plain Text) chỉ chứa các ký tự mã ASCII/Unicode cơ bản nên dung lượng rất nhỏ (vài KB). Nếu bị mất 1 byte dữ liệu do lỗi mạng, file `.md` vẫn mở ra đọc bình thường các phần còn lại, trong khi file `.docx` sẽ hỏng hoàn toàn cấu trúc zip/xml và không thể mở được.
- **Hỗ trợ Git Diff hoàn hảo:** Git dễ dàng so sánh từng dòng code/chữ trong file Markdown, giúp nhóm làm việc chung phát hiện chính xác ai đã sửa dòng nào, tránh tối đa xung đột.

---

## Phần 2. Hoàn thiện nội dung giới thiệu dự án GreenTech (Chuyển đổi sang Markdown)

# Dự Án GreenTech - Giải Pháp Nông Nghiệp Thông Minh

Chào mừng bạn đến với dự án **GreenTech**! Đây là hệ thống giám sát và tự động hóa công việc chăm sóc cây trồng dựa trên công nghệ IoT.

## I. Mục tiêu dự án
- Tự động hóa quy trình tưới nước và điều hòa nhiệt độ môi trường.
- Tối ưu hóa chi phí vận hành và tiết kiệm nước cho trang trại.
- Giám sát thông số môi trường thời gian thực thông qua ứng dụng di động.

## II. Bảng so sánh các giải pháp kỹ thuật

| Tiêu chí | Giải pháp truyền thống | Giải pháp GreenTech (IoT) |
| :--- | :--- | :--- |
| **Cách thức vận hành** | Bật/tắt thủ công bằng tay | Tự động hóa theo cảm biến |
| **Độ chính xác** | Phụ thuộc vào cảm tính người làm | Chính xác theo thông số thời gian thực |
| **Tiết kiệm tài nguyên** | Dễ gây lãng phí nước/điện | Tối ưu hóa 30% - 50% chi phí |

## III. Danh sách công việc triển khai (Task List)
- [x] Thiết kế sơ đồ nguyên lý phần cứng
- [x] Lập trình tập lệnh đọc dữ liệu cảm biến
- [ ] Kết nối hệ thống với máy chủ đám mây (Cloud)
- [ ] Chạy thử nghiệm thực tế tại nhà kính
