## Hướng dẫn chi tiết về Quy tắc người dùng, Bộ nhớ, Theo dõi lỗi và Tạo quy tắc

 Dựa trên cuộc trò chuyện, đây là hướng dẫn tập trung vào các khía cạnh chính mà bạn quan tâm:

 ### 1. Quản lý tác vụ phức tạp

 * **T = Σ(τ_complex) ⇌ hệ thống tác vụ có cấu trúc**
 * T.plan_path = ".cursor/tasks/"
 * T.backlog_path = ".cursor/tasks/backlog.md"
 * T.sprint_path = ".cursor/tasks/sprint_{n}/"
 * T.structure = (step_n.md ⨁ review.md)
 * T.progress = siêu dữ liệu trong tệp {status, priority, notes}
 * T.backlog = nhóm tác vụ với tính năng tự động ưu tiên
 * T.sprint_review = (
  kích hoạt khi xác thực
  ⨁ chạy M.sync ⨁ Λ.extract ⨁ Φ.snapshot ⨁ Ψ.summarize
 )
 * T.update_task_progress = (
  xác định vị trí bước hiện tại trong sprint hoặc backlog
  ⨁ cập nhật trạng thái = "done"
  ⨁ kiểm tra các mục trong danh sách kiểm tra dựa trên quan sát đã hoàn thành
  ⨁ thêm ghi chú nếu một phần hoặc đã sửa đổi
 )

 ### 2. Theo dõi và cải tiến lỗi

 * **Ξ* = công cụ chẩn đoán & cải tiến**
 * Ξ.error_memory = ".cursor/memory/errors.md"
 * Ξ.track = ghi lại các vấn đề lặp lại, đề xuất sửa lỗi
 * Ξ.cleanup_phase = (
  phát hiện trôi mã: logic chết, nhập bị hỏng, không mạch lạc
  ⨁ đề xuất tái cấu trúc hoặc đơn giản hóa
  ⨁ tùy chọn lưu trữ các khối đã xóa trong Ψ
 )
 * Ξ.recurrence_threshold = 2
 * Ξ.pattern_suggestion = (
  nếu phát hiện các vấn đề có thể sửa chữa lặp lại
  ⨁ tự động tạo bản nháp quy tắc trong Λ.path
  ⨁ đề xuất chiến lược có thể tái sử dụng
 )

 ### 3. Công cụ học tập dựa trên quy tắc

 * **Λ = tự học dựa trên quy tắc**
 * Λ.path = ".cursor/rules/"
 * Λ.naming_convention = {
  "0■■": "Tiêu chuẩn cốt lõi",
  "1■■": "Cấu hình công cụ",
  "3■■": "Quy tắc kiểm tra",
  "1■■■": "Dành riêng cho ngôn ngữ",
  "2■■■": "Quy tắc dành riêng cho khung",
  "8■■": "Quy trình làm việc",
  "9■■": "Mẫu",
  "_name.mdc": "Quy tắc riêng tư"
  }
 * Λ.naming_note = "Mặt nạ danh mục, không phải chữ cố định. Sử dụng ID tăng dần."
 * Λ.pattern_alignment = (
  căn chỉnh mã với các phương pháp hay nhất
  ⨁ đề xuất các mẫu chỉ khi được biện minh
  ⨁ thực thi SRP, tránh trừu tượng hóa sớm
 )
 * Λ.autonomy = (
  tự động phát hiện các lần lặp lại đáng giá quy tắc
  ⨁ tạo _DRAFT.mdc trong ngữ cảnh
 )

 ### 4. Bộ nhớ dựa trên tệp

 * **M = Στ(λ) ⇌ bộ nhớ dựa trên tệp**
 * M.memory_path = ".cursor/memory/"
 * M.retrieval = giải quyết tham chiếu động
 * M.sync = (
  được kích hoạt khi xem xét
  ⨁ lưu trữ ý tưởng, ràng buộc, thông tin chi tiết, ghi chú cạnh
 )

 ### 5. Ví dụ về cách sử dụng

 * "Tạo quy tắc cho…"
 * "Theo dõi các lỗi lặp lại về…"
 * "Hãy nhớ điều này:…"
 * "Sử dụng những gì bạn đã ghi nhớ làm mẫu để tạo quy tắc."
 * "Nhớ lại lỗi về X và tạo quy tắc sửa lỗi."
 * "Lưu trữ heuristic này để sử dụng trong tương lai."

 ### 6. Cấu trúc đầu ra
```
.cursor/
├── tasks/          # Kế hoạch, backlog, các bước sprint
├── rules/          # Các quy tắc thực hành tốt nhất được đề xuất
├── memory/         # Dấu vết lý luận, lịch sử lỗi
```

### 7. Mẹo sử dụng

* Rõ ràng: Bắt đầu lời nhắc bằng các thuật ngữ như **plan**, **refactor**, **test**, **rule**.
* Sử dụng ngôn ngữ có cấu trúc: Agent thích các bước và ý định rõ ràng.
* Bao gồm ngữ cảnh dev: Sử dụng các thuật ngữ Agile/TDD để phù hợp với logic bên trong.
* Nghĩ dài hạn: Các hành vi lặp lại được biến thành các quy tắc có thể tái sử dụng.
* Hãy thoải mái thử nghiệm — và nếu có điều gì đó không ổn, hãy hỏi **why** trực tiếp
