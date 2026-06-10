[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112875&assignment_repo_type=AssignmentRepo)

# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** luongdoan305@gmail.com
**Name:** Luong Quoc Doan

---

## Mo ta

Trong bài lab này, tôi thực hành xây dựng một Data Pipeline đơn giản theo mô hình ETL (Extract - Transform - Load) kết hợp với các kỹ thuật Data Quality cơ bản.

Các công việc đã thực hiện bao gồm:

- Đọc dữ liệu từ file JSON (Extract).
- Thực hiện làm sạch dữ liệu (Transform) như:
  - Loại bỏ dữ liệu trùng lặp (Deduplication).
  - Loại bỏ các giá trị bất thường (Outlier Detection).
  - Kiểm tra tính hợp lệ của dữ liệu (Sanity Check).
  - Ẩn thông tin cá nhân (PII Masking) bằng cách xóa trường tên và che email.
- Xuất dữ liệu đã làm sạch ra file mới (Load).
- Thực hiện thí nghiệm so sánh chất lượng dữ liệu sạch và dữ liệu lỗi để đánh giá ảnh hưởng của Data Quality đến độ chính xác của AI Agent.
- Tìm hiểu vai trò của Data Validation, Data Cleaning và Observability trong quá trình xây dựng Data Pipeline.

---

## Cach chay (How to Run)

### Prerequisites

```bash
pip install pandas
```

### Chay ETL Pipeline

```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)

```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
