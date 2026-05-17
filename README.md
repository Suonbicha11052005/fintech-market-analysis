# FinTech Market Analysis & Smart Lending Strategy 📊

Dự án tập trung phân tích thị trường FinTech tại Việt Nam và xây dựng chiến lược cho vay thông minh dành cho nhóm khách hàng chưa được phục vụ hiệu quả bởi hệ thống ngân hàng truyền thống.

Bài toán được thực hiện cho công ty FinTech giả định **FinInnovate** — doanh nghiệp ứng dụng AI, khoa học dữ liệu và tư duy lấy người dùng làm trung tâm để cung cấp các giải pháp tín dụng công bằng, cá nhân hóa và dễ tiếp cận hơn. :contentReference[oaicite:0]{index=0}

Dự án kết hợp:
- Phân tích thị trường
- Phân tích hành vi khách hàng
- Predictive modeling
- Customer segmentation
- Chiến lược phát triển sản phẩm tài chính

Từ bộ dữ liệu gồm 50,000 hồ sơ vay vốn ẩn danh, nhóm xác định được phân khúc thị trường tiềm năng và đề xuất mô hình **FinConnect Smart Group Lending** — nền tảng micro-lending dựa trên AI và social trust. :contentReference[oaicite:1]{index=1}

---

# 🎯 Business Problem

Các ngân hàng truyền thống tại Việt Nam vẫn phụ thuộc mạnh vào:
- Credit score truyền thống
- Quy trình xét duyệt giấy tờ phức tạp
- Yêu cầu tài sản thế chấp
- Lịch sử tín dụng chính thức

Điều này khiến một lượng lớn khách hàng:
- Không tiếp cận được tín dụng chính thống
- Bị từ chối khoản vay
- Dễ rơi vào tín dụng đen hoặc cho vay lãi cao

Theo nghiên cứu thị trường, khoảng **30–40% người trưởng thành tại Việt Nam không có lịch sử tín dụng chính thức**, tạo ra một khoảng trống lớn cho các giải pháp FinTech mới. :contentReference[oaicite:2]{index=2}

Mục tiêu của dự án:
- Xác định phân khúc khách hàng tiềm năng
- Phân tích các yếu tố ảnh hưởng đến default risk
- Xây dựng mô hình dự đoán khả năng vỡ nợ
- Đề xuất chiến lược lending phù hợp cho nhóm underserved customers

---

# 📁 Project Structure

```text
fintech-market-analysis/
│
├── README.md
├── .gitignore
│
├── dataset/
│   ├── FBA_DATA_DICTIONARY.xlsx
│   ├── FBA 2025 - Customer credit data.xlsx
│   └── master_df.csv
│
├── notebooks/
│   ├── FBAR2_Sherpa_EDA.ipynb
│   └── FBAR2_Sherpa_Model.ipynb
│
├── [FBAR2]_Sherpa_Report.pdf
├── FBA Round 2 Question Booklet.pdf
└── FBAR2_Sherpa.pbix
```

---

# 📊 Dataset Overview

Bộ dữ liệu gồm:
- 50,000 hồ sơ vay vốn ẩn danh
- 13 biến chính
- Thông tin nhân khẩu học, tài chính và hành vi tín dụng

Các nhóm dữ liệu bao gồm:
- Age group
- Employment status
- Income level
- Housing status
- Loan amount
- Debt
- Savings
- Credit rating
- Loan repayment status

:contentReference[oaicite:3]{index=3}

---

# 🔍 Key Business Insights

## Customer Base Characteristics

Tệp khách hàng chủ yếu tập trung ở:
- Nhóm thu nhập thấp và trung bình
- Người lao động toàn thời gian
- Người thuê nhà
- Khách hàng có Fair–Good credit score

Phần lớn khách hàng:
- Có dưới 10 năm kinh nghiệm làm việc
- Vay các khoản nhỏ và trung bình
- Vay chủ yếu để debt consolidation

:contentReference[oaicite:4]{index=4}

---

## Default Risk Drivers

Những khách hàng có:
- Thu nhập thấp
- Credit score thấp
- Công việc thiếu ổn định
- Debt-to-savings ratio cao

có xác suất default cao hơn đáng kể.

Trong khi đó:
- Khách hàng thu nhập cao
- Lao động toàn thời gian
- Có savings tốt
- Quản lý tài chính kỷ luật

có rủi ro tín dụng thấp hơn. :contentReference[oaicite:5]{index=5}

---

# 🤖 Predictive Modeling

Dự án xây dựng và so sánh nhiều mô hình classification:
- Logistic Regression
- Random Forest
- LightGBM
- XGBoost

Mô hình cuối cùng được lựa chọn là **LightGBM** nhờ:
- Hiệu suất tốt hơn
- Feature importance rõ ràng
- Khả năng xử lý dữ liệu hiệu quả

:contentReference[oaicite:6]{index=6}

---

# 📈 Feature Engineering

Nhóm xây dựng thêm nhiều financial ratios để cải thiện khả năng dự đoán:

- Loan-to-Income Ratio
- Debt-to-Savings Ratio
- Debt-to-Income Ratio (DTI)

Các biến này trở thành những yếu tố quan trọng nhất trong predictive model. :contentReference[oaicite:7]{index=7}

---

# 📊 Model Performance

## LightGBM Metrics

| Metric | Score |
|---|---|
| Accuracy | 0.6395 |
| Precision | 0.4230 |
| Recall | 0.4490 |

Kết quả cho thấy:
- Income level
- Savings behavior
- Employment stability

là những yếu tố ảnh hưởng mạnh nhất đến khả năng trả nợ của khách hàng. :contentReference[oaicite:8]{index=8}

---

# 👥 Customer Segmentation

Nhóm sử dụng:
- K-Means Clustering
- Elbow Method

để phân chia khách hàng thành 4 nhóm archetypes khác nhau. :contentReference[oaicite:9]{index=9}

Các phân khúc bao gồm:

| Segment | Đặc điểm |
|---|---|
| Unemployment Risk | Nhóm rủi ro cao do thất nghiệp |
| Financially Strained | Thu nhập thấp, áp lực tài chính cao |
| Middle Class | Nhóm khách hàng ổn định phổ biến |
| Wealthy, High Leverage | Thu nhập cao nhưng vay lớn |

---

# 🎯 Target Segment

Nhóm tập trung vào phân khúc:

## Financially Strained

Đặc điểm:
- Chiếm 30.3% tập dữ liệu
- 91.8% là low-income borrowers
- Debt-to-savings ratio cao
- Financial pressure lớn
- Default rate lên tới 40.5%

Tuy nhiên đây cũng là:
- Nhóm underserved lớn nhất
- Có nhu cầu vay thực tế
- Có tiềm năng phát triển nếu áp dụng alternative scoring

:contentReference[oaicite:10]{index=10}

---

# 💡 Proposed Solution — FinConnect

Nhóm đề xuất nền tảng:

## FinConnect Smart Group Lending

Mô hình micro-lending dựa trên:
- Group responsibility
- AI trust scoring
- Smart peer matching
- Dynamic credit history

Thay vì chỉ dùng traditional credit score, hệ thống đánh giá:
- Savings behavior
- Financial discipline
- Social trust
- Group repayment dynamics

:contentReference[oaicite:11]{index=11}

---

# 🚀 Go-To-Market Strategy

## Phase 1 — Pre-Launch
- Xây dựng cộng đồng
- Referral campaign
- Financial education content
- Hợp tác với industrial zones

## Phase 2 — Launch
- Beta rollout
- Zero-fee campaigns
- User acquisition bằng referral

## Phase 3 — Scale
- Tối ưu smart matching
- Loyalty & gamification
- Retail partnership ecosystem

:contentReference[oaicite:12]{index=12}

---

# 🛠️ Technical Stack

## Programming & Analytics
- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- XGBoost

## Visualization
- Matplotlib
- Seaborn
- Power BI

## Analytical Techniques
- Classification Modeling
- Feature Engineering
- K-Means Clustering
- Customer Segmentation
- Credit Risk Analysis

---

# 📊 Dashboard

Dự án bao gồm Power BI dashboard:

```text
FBAR2_Sherpa.pbix
```

Dashboard hỗ trợ:
- Customer demographics analysis
- Credit risk analysis
- Segment visualization
- Default trend analysis
- Market opportunity insights

---

# 🧠 Analytical Workflow

## 1. Data Cleaning
- Xử lý missing values
- Chuẩn hóa dữ liệu
- Encode categorical variables
- Standardize numerical features

---

## 2. Exploratory Data Analysis (EDA)
Phân tích:
- Customer demographics
- Loan behavior
- Default patterns
- Income distribution
- Credit risk indicators

---

## 3. Predictive Modeling
Xây dựng và đánh giá:
- Logistic Regression
- Random Forest
- LightGBM
- XGBoost

---

## 4. Customer Segmentation
Ứng dụng:
- K-Means clustering
- Elbow Method
- Segment profiling

---

## 5. Strategic Recommendation
Đề xuất:
- FinConnect Smart Group Lending
- Trust scoring framework
- Go-to-market strategy
- Product roadmap

---

# 🚀 How to Run

## Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/fintech-market-analysis.git
```

---

## Open Jupyter Notebook

```bash
jupyter notebook
```

---

## Open Power BI Dashboard

Mở file:

```text
FBAR2_Sherpa.pbix
```

bằng Power BI Desktop.

---

# 📌 Repository Contents

| File | Description |
|---|---|
| `FBAR2_Sherpa_EDA.ipynb` | Notebook phân tích dữ liệu khám phá |
| `FBAR2_Sherpa_Model.ipynb` | Notebook xây dựng predictive model |
| `master_df.csv` | Dữ liệu đã xử lý |
| `FBAR2_Sherpa.pbix` | Power BI dashboard |
| `[FBAR2]_Sherpa_Report.pdf` | Báo cáo chiến lược cuối cùng |
| `FBA Round 2 Question Booklet.pdf` | Đề bài case study |

---

# 📄 Disclaimer

Dự án được thực hiện cho mục đích học thuật và nghiên cứu.

Toàn bộ dữ liệu trong dự án đã được ẩn danh và chỉ phục vụ cho mục đích phân tích.
