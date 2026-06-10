# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600564
**Name:** Lương Quốc Đoàn
**Date:** 10/06/2026

---

## 1. Kết quả thí nghiệm

Chạy `agent_simulation.py` với hai bộ dữ liệu và ghi lại kết quả:

| Scenario                          | Agent Response                                                                                                        | Accuracy (1-10) | Notes                                                                                  |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------- | -------------------------------------------------------------------------------------- |
| Clean Data (`processed_data.csv`) | Agent trả lời chính xác thông tin sản phẩm, giá và danh mục sản phẩm. Kết quả nhất quán và không phát sinh lỗi xử lý. | 9/10            | Dữ liệu đã được làm sạch, chuẩn hóa và không có bản ghi lỗi.                           |
| Garbage Data (`garbage_data.csv`) | Agent trả lời thiếu chính xác, một số thông tin bị sai lệch hoặc không thể xử lý được.                                | 4/10            | Dữ liệu chứa nhiều lỗi như trùng lặp, giá trị bất thường và định dạng không nhất quán. |

---

## 2. Phân tích & nhận xét

### Tại sao Agent trả lời sai khi dùng Garbage Data?

Kết quả thí nghiệm cho thấy chất lượng dữ liệu có ảnh hưởng trực tiếp đến hiệu suất của AI Agent. Khi sử dụng bộ dữ liệu sạch (`processed_data.csv`), Agent có thể truy xuất và xử lý thông tin một cách chính xác vì dữ liệu đã được chuẩn hóa, loại bỏ dữ liệu trùng lặp và xử lý các giá trị bất thường.

Ngược lại, khi sử dụng bộ dữ liệu lỗi (`garbage_data.csv`), Agent gặp nhiều vấn đề trong quá trình suy luận. Các bản ghi bị trùng lặp (Duplicate IDs) có thể khiến Agent lấy nhầm thông tin hoặc đưa ra kết quả không nhất quán. Những giá trị ngoại lai (Outliers), chẳng hạn như mức giá quá cao hoặc quá thấp so với thực tế, làm sai lệch kết quả phân tích. Ngoài ra, các kiểu dữ liệu không đúng (Wrong Data Types) như lưu giá dưới dạng chuỗi thay vì số có thể khiến các phép tính thất bại hoặc tạo ra kết quả sai. Các giá trị rỗng (Null Values) cũng làm mất thông tin cần thiết, khiến Agent không đủ dữ liệu để đưa ra câu trả lời chính xác.

Qua đó có thể thấy rằng chất lượng dữ liệu đầu vào đóng vai trò rất quan trọng đối với độ chính xác của hệ thống AI. Một mô hình tốt hoặc một prompt tốt vẫn có thể cho kết quả không chính xác nếu dữ liệu đầu vào chứa nhiều lỗi hoặc không được làm sạch trước khi xử lý.

---

## 3. Kết luận

### Quality Data > Quality Prompt?

Tôi đồng ý với nhận định này.

Mặc dù prompt đóng vai trò quan trọng trong việc hướng dẫn AI thực hiện nhiệm vụ, nhưng dữ liệu chất lượng cao vẫn là yếu tố nền tảng quyết định độ chính xác của kết quả. Nếu dữ liệu đầu vào bị sai lệch, thiếu nhất quán hoặc chứa nhiều lỗi thì AI Agent sẽ khó có thể đưa ra câu trả lời chính xác dù prompt được thiết kế rất tốt.

Do đó, trong các hệ thống AI thực tế, việc xây dựng quy trình Data Cleaning, Data Validation và Data Quality Monitoring là vô cùng cần thiết. Chất lượng dữ liệu tốt sẽ giúp Agent hoạt động hiệu quả hơn, giảm lỗi và nâng cao độ tin cậy của toàn bộ hệ thống.
