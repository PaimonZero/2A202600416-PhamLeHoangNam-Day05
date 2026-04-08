# PHÂN TÍCH UX SẢN PHẨM AI: TRỢ THỦ MONI (MOMO)

**Người thực hiện:** Phạm Lê Hoàng Nam
**Sản phẩm:** MoMo — Trợ thủ AI Moni

---

## PHẦN 1 — KHÁM PHÁ (EXPLORATION)

### 1. Marketing

- **Kênh tiếp cận:** Website MoMo, thông báo đẩy (push notifications), và mục "Quản lý chi tiêu" trong app.
- **Lời hứa:** MoMo quảng bá Moni là một "Trợ thủ tài chính" có khả năng:
  - Tự động hóa việc phân loại giao dịch.
  - Nhắc nhở thanh toán hóa đơn thông minh.
  - Trò chuyện và giải đáp thắc mắc dịch vụ bằng ngôn ngữ tự nhiên như người thật.
- **Kỳ vọng tạo ra:** Người dùng mong đợi một hệ thống "set and forget" (thiết lập rồi quên đi), không cần phải nhập tay từng ly cà phê hay ổ bánh mì.

### 2. Trải nghiệm thực tế (Hands-on)

- **UI Entry Point:** Moni xuất hiện ở tab "Lịch sử giao dịch" và một widget lớn ở màn hình chính. Biểu tượng là một chú robot nhỏ thân thiện.
- **Phản ứng của AI:** \* Khi có giao dịch mới (ví dụ: thanh toán tại Highlands Coffee), Moni ngay lập tức đẩy vào nhóm "Ăn uống".
  - Khi chat: "Tháng này tôi tiêu bao nhiêu?", AI mất khoảng 2-3 giây để xử lý và xuất ra biểu đồ tròn.
- **Thay đổi UI:** Khi vào luồng chat, bàn phím thông thường được thay bằng các "Quick Replies" (Gợi ý nhanh) như: _Hạn mức còn lại?_, _Tiền điện tháng này?_, giúp giảm thao tác gõ.

---

## PHẦN 2 — PHÂN TÍCH 4 PATHS (FRAMEWORK)

| Path                     | Trạng thái     | Phân tích chi tiết trải nghiệm                                                                                                                                                                                        |
| :----------------------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Khi AI đúng**       | **Thành công** | Hệ thống tự động gán nhãn chính xác (ví dụ: Grab -> Di chuyển). User nhận được thông báo "Moni đã phân loại giúp bạn". Cảm giác hài lòng cao vì tiết kiệm thời gian.                                                  |
| **2. Khi AI không chắc** | **Phân vân**   | Moni đưa giao dịch vào mục "Chưa phân loại" hoặc "Khác". Tuy nhiên, hệ thống **ít khi chủ động hỏi lại** ngay lúc đó mà đợi user tự vào kiểm tra, dẫn đến biểu đồ chi tiêu bị sai lệch nếu user quên.                 |
| **3. Khi AI sai**        | **Thất bại**   | **Ví dụ:** Chuyển tiền trả nợ cho bạn nhưng AI lại tính vào "Mua sắm". **Cách sửa:** User phải nhấn vào giao dịch -> Chọn "Sửa loại chi tiêu" -> Tìm trong danh sách 20+ danh mục. Quá trình này tốn 4-5 bước chạm.   |
| **4. Khi user mất tin**  | **Lối thoát**  | User có thể tắt tính năng Moni trong cài đặt hoặc xóa hoàn toàn lịch sử chat. Có fallback là nút "Liên hệ tổng đài", nhưng Moni thường cố giữ user ở lại bằng các câu trả lời mẫu thay vì kết nối ngay với nhân viên. |

### Nhận xét:

- **Path xử lý tốt nhất:** **Path 1.** Tốc độ xử lý realtime và khả năng nhận diện các merchant lớn (Grab, Shopee, Highland) rất ấn tượng.
- **Path yếu nhất:** **Path 3.** Đây là "điểm gãy" lớn nhất. AI sai là chuyện bình thường, nhưng cách MoMo bắt người dùng đi "dọn rác" cho AI bằng quy trình thủ công phức tạp làm giảm giá trị của từ "Trợ thủ".
- **Gap Marketing vs. Thực tế:** Marketing nói là Tự động, nhưng thực tế user vẫn phải đóng vai trò "kiểm soát viên" thường xuyên để chỉnh sửa các danh mục bị gán sai.
