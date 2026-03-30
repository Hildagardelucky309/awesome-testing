# Các Câu Lệnh Kiểm Thử Chức Năng (Functional Testing Prompts)

---

## 1. Tạo kịch bản kiểm thử dựa trên tính năng (Feature-Based)

```text
Tôi cần tạo các kịch bản kiểm thử chức năng toàn diện cho [TÊN_TÍNH_NĂNG].

Mô tả tính năng: [MÔ_TẢ_TÍNH_NĂNG]
User Story: [CÂU_CHUYỆN_NGƯỜI_DÙNG]
Tiêu chí chấp nhận (Acceptance Criteria): [TIÊU_CHÍ]

Vui lòng tạo các kịch bản kiểm thử bao gồm:
- Luồng chạy chuẩn (Happy path)
- Các luồng thay thế (Alternative flows)
- Kiểm tra dữ liệu đầu vào (Input validation)
- Kết quả đầu ra mong đợi
- Điều kiện tiên quyết và điều kiện sau khi thực hiện

Định dạng mỗi kịch bản gồm: ID, Tiêu đề, Điều kiện tiên quyết, Các bước thực hiện, Kết quả mong đợi, Độ ưu tiên.
```

## 2. Kiểm thử luồng người dùng (User Flow Testing)

```text
Tạo các kịch bản kiểm thử cho luồng người dùng sau đây:
[MÔ_TẢ_HÀNH_TRÌNH_NGƯỜI_DÙNG]

Bao gồm các kịch bản cho:
- Từng bước trong luồng
- Chuyển hướng giữa các bước
- Khả năng lưu trữ dữ liệu xuyên suốt các bước
- Xử lý lỗi tại mỗi giai đoạn
- Các điểm thoát và kịch bản hủy bỏ
```

## 3. Kiểm thử các thao tác CRUD (Thêm, Đọc, Sửa, Xóa)

```text
Tạo các kịch bản kiểm thử chức năng cho các thao tác CRUD trên [TÊN_ĐỐI_TƯỢNG]:

Các trường thông tin: [DANH_SÁCH_TRƯỜNG_VÀ_KIỂU_DỮ_LIỆU]
Quy tắc nghiệp vụ: [MÔ_TẢ_QUY_TẮC]

Tạo kịch bản cho:
- Create (Tạo): Dữ liệu hợp lệ/không hợp lệ, các trường bắt buộc, giá trị mặc định.
- Read (Đọc): Xem một bản ghi, nhiều bản ghi, lọc (filtering), sắp xếp (sorting).
- Update (Cập nhật): Cập nhật một phần, cập nhật toàn bộ, cập nhật đồng thời.
- Delete (Xóa): Xóa đơn lẻ, xóa hàng loạt, xóa tạm thời (soft delete), hiệu ứng xóa bắc cầu (cascade).
```

## 4. Kiểm thử kiểm tra tính hợp lệ của Form (Form Validation)

```text
Tạo các kịch bản kiểm thử cho việc kiểm tra tính hợp lệ của biểu mẫu:

Tên biểu mẫu: [TÊN_FORM]
Các trường: [DANH_SÁCH_TRƯỜNG_KÈM_QUY_TẮC_VALIDATION]

Tạo kịch bản cho:
- Kiểm tra trường bắt buộc
- Kiểm tra kiểu dữ liệu
- Kiểm tra định dạng (email, số điện thoại, ngày tháng, v.v.)
- Giới hạn độ dài ký tự
- Xử lý ký tự đặc biệt
- Kiểm tra tính hợp lệ chéo giữa các trường (cross-field)
- Trạng thái của nút Submit
```

## 5. Kiểm thử chức năng tìm kiếm (Search Functionality)

```text
Tạo các kịch bản kiểm thử cho chức năng tìm kiếm:

Loại tìm kiếm: [CƠ_BẢN/NÂNG_CAO/PHÂN_LOẠI-FACETED]
Các trường có thể tìm kiếm: [DANH_SÁCH_TRƯỜNG]
Các bộ lọc hiện có: [DANH_SÁCH_BỘ_LỌC]

Bao gồm các kịch bản cho:
- Tìm kiếm khớp hoàn toàn
- Tìm kiếm khớp một phần
- Phân biệt chữ hoa chữ thường
- Ký tự đặc biệt trong tìm kiếm
- Kết quả tìm kiếm trống
- Sắp xếp và phân trang kết quả tìm kiếm
- Kết hợp nhiều bộ lọc
```

## 6. Kiểm thử điểm tích hợp (Integration Point)

```text
Tạo các kịch bản kiểm thử chức năng cho việc tích hợp giữa [HỆ_THỐNG_A] và [HỆ_THỐNG_B]:

Loại tích hợp: [API/CHUYỂN_FILE/DATABASE/MESSAGE_QUEUE]
Luồng dữ liệu: [MÔ_TẢ_LUỒNG_DỮ_LIỆU]
Hành vi mong đợi: [MÔ_TẢ_HÀNH_VI_MONG_ĐỢI]

Bao gồm:
- Trao đổi dữ liệu thành công
- Độ chính xác khi chuyển đổi dữ liệu
- Xử lý lỗi và cơ chế thử lại (retry logic)
- Kịch bản quá hạn thời gian (timeout)
- Kiểm tra dữ liệu tại các điểm biên (boundaries)
```

## 7. Kiểm thử quyền hạn và kiểm soát truy cập (Permission & Access Control)

```text
Tạo các kịch bản kiểm thử cho kiểm soát truy cập dựa trên vai trò (RBAC):

Vai trò: [DANH_SÁCH_VAI_TRÒ]
Tính năng/Module: [DANH_SÁCH_TÍNH_NĂNG]
Ma trận phân quyền: [MÔ_TẢ_AI_CÓ_QUYỀN_LÀM_GÌ]

Tạo kịch bản cho:
- Các hành động được phép của từng vai trò
- Các hành động bị từ chối của từng vai trò
- Kịch bản chuyển đổi vai trò
- Các nỗ lực truy cập trái phép
- Hiển thị tính năng dựa trên quyền hạn
```

## 8. Kiểm thử chuyển đổi trạng thái quy trình (Workflow State Transition)

```text
Tạo các kịch bản kiểm thử cho việc chuyển đổi trạng thái quy trình:

Đối tượng: [TÊN_ĐỐI_TƯỢNG]
Các trạng thái: [DANH_SÁCH_TRẠNG_THÁI]
Các chuyển đổi được phép: [MÔ_TẢ_SƠ_ĐỒ_TRẠNG_THÁI]
Quy tắc nghiệp vụ: [MÔ_TẢ_QUY_TẮC]

Tạo kịch bản cho:
- Các chuyển đổi trạng thái hợp lệ
- Các nỗ lực chuyển đổi không hợp lệ
- Các hành động đặc thù tại từng trạng thái
- Chuyển đổi có điều kiện
- Các kịch bản hoàn tác (rollback)
```

## 9. Kiểm thử thông báo và cảnh báo (Notification & Alert)

```text
Tạo các kịch bản kiểm thử chức năng cho thông báo:

Loại thông báo: [EMAIL/SMS/PUSH/IN-APP]
Sự kiện kích hoạt: [DANH_SÁCH_SỰ_KIỆN]
Cài đặt người dùng: [MÔ_TẢ_CÀI_ĐẶT]

Bao gồm các kịch bản cho:
- Kích hoạt thông báo thành công
- Độ chính xác của nội dung
- Thời gian gửi thông báo
- Tuân thủ cấu hình ưu tiên của người dùng
- Lịch sử thông báo
- Chức năng từ chối nhận thông báo (opt-out)
```

## 10. Kiểm thử chức năng báo cáo (Reporting Functionality)

```text
Tạo các kịch bản kiểm thử cho tính năng báo cáo:

Tên báo cáo: [TÊN_BÁO_CÁO]
Nguồn dữ liệu: [MÔ_TẢ_NGUỒN]
Bộ lọc/Tham số: [DANH_SÁCH_THAM_SỐ]
Định dạng đầu ra: [PDF/EXCEL/CSV/v.v.]

Bao gồm:
- Tạo báo cáo với các bộ lọc khác nhau
- Xác minh độ chính xác của dữ liệu
- Xử lý khoảng thời gian (date range)
- Chức năng xuất dữ liệu (export)
- Xử lý khi kết quả trống
- Hiệu suất với tập dữ liệu lớn
- Tạo báo cáo tự động theo lịch trình
```

---

## Mẹo khi sử dụng các câu lệnh này

1.  **Càng cụ thể càng tốt**: Thay thế các phần trong ngoặc `[...]` bằng chi tiết thực tế của tính năng.
2.  **Cung cấp ngữ cảnh**: Đưa thêm các quy tắc nghiệp vụ và ràng buộc thực tế của dự án.
3.  **Lặp lại và cải thiện**: Tinh chỉnh kết quả của AI dựa trên nhu cầu đặc thù của bạn.
4.  **Kiểm tra lại**: Luôn rà soát các kịch bản do AI tạo ra để đảm bảo tính đầy đủ và chính xác.
5.  **Tùy chỉnh**: Điều chỉnh định dạng sao cho phù hợp với tiêu chuẩn của tổ chức bạn.