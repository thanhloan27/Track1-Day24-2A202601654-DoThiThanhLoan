# Track 1 — Day 24 · AI Product Financial Model & Unit Economics Lab

## Thông tin cá nhân

| | |
|---|---|
| **Họ và tên** | Đỗ Thị Thanh Loan |
| **Mã học viên** | 2A202601654 |
| **Track** | Track 1 — AI Product Management |
| **Bài** | Day 24 — AI Product Financial Model: từ Giả định đến Stress-test 3 Kịch bản |

## Dự án

**AttendAI — Nền tảng chấm công AI cho doanh nghiệp SME Việt Nam**

Kế thừa module **Chấm công** trong hệ thống HRM nội bộ tôi phân tích ở Day 23, nhưng đóng vai **bán ra thị trường** thay vì dùng nội bộ.

| | |
|---|---|
| **Lõi AI** | Nhận diện khuôn mặt khi mở/đóng ca (chống chấm công hộ) · Phát hiện ca bất thường · Trợ lý giải thích bảng công bằng ngôn ngữ tự nhiên |
| **Người trả tiền** | Giám đốc / Trưởng phòng HR của SME **20–200 lao động** — sản xuất nhỏ, chuỗi bán lẻ, F&B, khách sạn, logistics |
| **Người dùng hằng ngày** | Nhân viên toàn thời gian, làm tại chỗ **theo ca cố định** |
| **Mô hình thu tiền** | **Hybrid** — 590.000đ phí nền tảng/tháng + 18.000đ/nhân viên/tháng |
| **TAM** | **27.000 doanh nghiệp** (phễu top-down 5 bước, xem mục Nguồn tham khảo) |

**Vì sao Hybrid:** chi phí AI biến đổi theo số lượt nhận diện, mà số lượt = số nhân viên × số ca. Gói phí cố định thuần sẽ lỗ trên "power user" — doanh nghiệp 200 lao động 3 ca/ngày đốt gấp 10 lần doanh nghiệp 25 lao động 1 ca nhưng trả cùng giá. Phần phí nền tảng vẫn giữ được MRR dự đoán được.

## Bài nộp

| Sản phẩm | File |
|---|---|
| **Mô hình tài chính 3 Tab** | [`2A202601654_DoThiThanhLoan_Day24.xlsx`](2A202601654_DoThiThanhLoan_Day24.xlsx) |
| **Decision Note** | Ô `B39` Tab 1 của file Excel, và mục ngay dưới đây |

---

## Decision Note

AttendAI đặt ARPU 1.600.000 VNĐ/khách/tháng theo mô hình Hybrid: 590.000 phí nền tảng cộng 18.000/nhân viên. Với khách trung bình 55 lao động, mức này cao hơn ~15% so với ACheckin gói Starter (25.000 VNĐ/nhân viên/tháng) — phần chênh đổi lấy lớp AI nhận diện khuôn mặt chống chấm công hộ mà gói phổ thông không có. CAC 6.000.000 VNĐ tương đương 3,75 tháng doanh thu, đã tính đủ lương inside-sales, quảng cáo, demo và onboarding, không chỉ riêng tiền ads.

Về AI Hidden Costs, chúng tôi dự trù 190.000 VNĐ/khách/tháng, bằng 59% chi phí API (320.000): data labeling cho ~5% lượt nhận diện bị nghi ngờ (55.000), retrain model 20%/năm phân bổ đầu khách (45.000), Human-in-the-loop QA duyệt ca bất thường ~1,2 giờ/khách/tháng (65.000), và compliance dữ liệu sinh trắc học theo Nghị định 13/2023 (25.000). Vì vậy Gross Margin chỉ 60% — đúng khoảng 40-60% của sản phẩm AI, không phải 80% kiểu SaaS truyền thống.

Kết quả Base: LTV/CAC 5,33 và CAC Payback 6,25 tháng, vượt tiêu chuẩn VC. Tỷ số này không đến từ việc bóp CAC xuống thấp mà từ vòng đời khách 33 tháng — hệ quả của switching cost cao: đổi phần mềm chấm công đồng nghĩa di chuyển toàn bộ dữ liệu công và làm lại tích hợp bảng lương. NPV 927 triệu, IRR 43,6%, hoàn vốn dự án tháng 21.

Rủi ro lớn nhất là tiền mặt chạm đáy 529 triệu ở tháng 9, chỉ bằng 3 tháng chi phí cố định. Trong kịch bản Pessimistic với Churn 4,5% và CAC 9 triệu (đều gấp 1,5 lần Base), Runway vẫn đạt 14 tháng nhờ ba hành động đã định lượng: dừng acquisition trả phí (81 xuống 16 khách mới/tháng), đóng băng tuyển dụng, cắt ngân sách brand.

---

## Kết quả 3 kịch bản

### Tab 1 — Giả định đầu vào

| Chỉ số | Optimistic | **Base** | Pessimistic |
|---|---:|---:|---:|
| ARPU (đ/tháng) | 1.900.000 | **1.600.000** | 1.300.000 |
| Adoption rate | 0,35% | **0,30%** | 0,08% |
| TAM (doanh nghiệp) | 35.000 | **27.000** | 20.000 |
| API cost / khách | 290.000 | **320.000** | 380.000 |
| **AI Hidden Costs / khách** | 150.000 | **190.000** | 240.000 |
| Infrastructure / khách | 120.000 | **130.000** | 150.000 |
| → Tổng COGS / khách | 560.000 | **640.000** | 770.000 |
| Monthly Churn | 2,0% | **3,0%** | **4,5%** |
| CAC | 5.000.000 | **6.000.000** | **9.000.000** |
| Fixed cost / tháng | 240.000.000 | **170.000.000** | 133.000.000 |
| Vốn đầu tư ban đầu | 800.000.000 | **800.000.000** | 800.000.000 |
| Tiền mặt ban đầu | 4.000.000.000 | **4.000.000.000** | 4.000.000.000 |
| WACC | 20% | **20%** | 20% |

**Bóc tách AI Hidden Costs (cột Base) = 190.000đ = 59% API cost:**

| Cấu phần | Tiền | Căn cứ |
|---|---:|---|
| Data Labeling | 55.000 | ~5% lượt nhận diện bị nghi ngờ (≈121 ảnh/tháng) cần người gán nhãn lại |
| Model Retraining | 45.000 | Build model ≈400tr; retrain 20%/năm = 80tr/năm; phân bổ trên ~150 khách năm đầu |
| Human-in-the-loop QA | 65.000 | ~1,2 giờ/khách/tháng duyệt ca bất thường × ~55.000đ/giờ (= 10,2% COGS) |
| Compliance & Security | 25.000 | Ảnh khuôn mặt là dữ liệu cá nhân nhạy cảm — Nghị định 13/2023/NĐ-CP |

**Bóc tách API cost (cột Base, khách trung bình 55 nhân viên) = 320.000đ:** nhận diện khuôn mặt 55 NV × 2 lượt/ngày × 22 ngày = 2.420 lượt × ~110đ = 266.000đ · LLM trợ lý bảng công ~150 truy vấn × ~360đ = 54.000đ.

### Tab 2 — Unit Economics

| Chỉ số | Optimistic | **Base** | Pessimistic | Ngưỡng |
|---|---:|---:|---:|---|
| Gross Profit / tháng | 1.340.000 | **960.000** | 530.000 | |
| Gross Margin % | 70,5% | **60,0%** | 40,8% | 40–60% (AI product) |
| Số tháng ở lại TB | 50,0 | **33,3** | 22,2 | |
| LTV *(trên Gross Profit)* | 67.000.000 | **32.000.000** | 11.777.778 | |
| **LTV / CAC** | 13,40 | **5,33** | 1,31 | **> 3,0** |
| **CAC Payback** | 3,73 th | **6,25 th** | 16,98 th | **< 12 tháng** |
| **Verdict** | ✓ HEALTHY | **✓ HEALTHY** | ⚠ WATCH | |

> **LTV tính trên Gross Profit, không phải Revenue thô.** Nếu tính sai bằng Revenue, LTV sẽ là 53.333.333đ (thổi phồng 1,67 lần) và LTV/CAC hiện 8,89 thay vì 5,33.

> Cột Pessimistic ra `WATCH` là **đúng bản chất stress-test**. Nếu Pessimistic cũng HEALTHY thì cú sốc 1,5x đã bị làm nhẹ đi.

### Tab 3 — P&L & ROI (24 tháng)

| Chỉ số | Optimistic | **Base** | Pessimistic | Ngưỡng |
|---|---:|---:|---:|---|
| NPV (triệu đ) | 15.950,0 | **926,9** | −4.927,4 | **> 0** |
| IRR / năm | 514,8% | **43,6%** | 0,0% | **≥ 20%** |
| Project Payback | 12 th | **21 th** | > 24 th | **< 24 tháng** |
| **Runway** | ≥ 24 th | ≥ 24 th | **14 tháng** | **≥ 12 tháng** |
| Verdict | ✓ GO | **✓ GO** | ✗ NO-GO | |

**Dòng tiền mặt kịch bản Base** (triệu đồng) — không âm tháng nào, chạm đáy 529tr ở M9:

```
M1     M2     M3     M4     M5     M6     M7     M8     M9    M10    M11    M12
2.622  2.119  1.689  1.331  1.041    818    659    564    529    554    636    774
M13    M14    M15    M16    M17    M18    M19    M20    M21    M22    M23    M24
  965  1.209  1.504  1.847  2.239  2.677  3.160  3.686  4.255  4.865  5.514  6.203
```

**Dòng tiền mặt kịch bản Pessimistic** — cạn ở M15, Runway = 14 tháng:

```
M10    M11    M12    M13    M14    M15    M16    M17
  839    637    440    248     60   -123   -302   -476
```

### Plan B — vì sao Runway Pessimistic đạt 14 tháng

Bộ giả định đầu tiên cho Runway chỉ **7 tháng**, vì mô hình mặc định giả định vẫn đốt 9 triệu/khách để mua khách trong khi LTV chỉ còn 11,8 triệu (LTV/CAC 1,31). Không founder nào làm vậy. Kịch bản Pessimistic đúng phải bao gồm **phản ứng của founder**:

| Hành động | Từ → đến | Tiết kiệm |
|---|---|---:|
| Dừng acquisition trả phí, chỉ giữ inbound & giới thiệu | 81 → 16 khách mới/tháng | 342 tr/tháng |
| Đóng băng tuyển dụng (6 → 5 người) | 130tr → 110tr | 20 tr/tháng |
| Cắt ngân sách brand | 15tr → 3tr | 12 tr/tháng |

→ Runway **7 → 14 tháng**. Đây là Plan B đã được định lượng, không phải lời hứa "sẽ tối ưu chi phí".

---

## Đối chiếu 5 Gate

| Gate | Yêu cầu | Kết quả | |
|---|---|---|:-:|
| **1** | 100% ô vàng Tab 1 có số, cả 3 kịch bản | 42/42 ô | ✅ |
| **1** | AI Hidden Costs ≥ 30% API cost | 52% / **59%** / 63% | ✅ |
| **1** | Pessimistic Churn ≥ 1,5× Base | 4,5% / 3,0% = **1,50×** | ✅ |
| **1** | Pessimistic CAC ≥ 1,5× Base | 9tr / 6tr = **1,50×** | ✅ |
| **2** | Base LTV/CAC > 3,0 | **5,33** | ✅ |
| **2** | Base CAC Payback < 12 tháng | **6,25 tháng** | ✅ |
| **2** | LTV tính trên Gross Margin | 32,0tr *(không phải 53,3tr)* | ✅ |
| **3** | Base NPV > 0 | **+926,9 triệu** | ✅ |
| **3** | Base IRR ≥ 20% | **43,6%** | ✅ |
| **3** | Project Payback < 24 tháng | **21 tháng** | ✅ |
| **3** | **Pessimistic Runway ≥ 12 tháng** | **14 tháng** | ✅ |
| **4** | Decision Note có benchmark & Plan B | 296 từ, xem mục trên | ✅ |
| **5** | Đúng tên file + đủ deliverable | Excel + README.md | ✅ |

---

## Nguồn tham khảo

**TAM — phễu top-down:**

| Bước lọc | Logic | Còn lại |
|---|---|---:|
| Doanh nghiệp đang hoạt động tại VN | [NSO 2025](https://www.nso.gov.vn/du-lieu-va-so-lieu-thong-ke/2026/01/buc-tranh-phat-trien-doanh-nghiep-viet-nam-nam-2025/) | ~1.000.000 |
| Là SME (~98%) | [Báo Đầu tư](https://baodautu.vn/chiem-gan-98-tong-so-doanh-nghiep-doanh-nghiep-nho-va-vua-dang-o-dau-trong-nen-kinh-te-d249574.html) | ~980.000 |
| Có ≥ 10 lao động (loại DN siêu nhỏ ~68%) | Siêu nhỏ chưa đủ nhu cầu phần mềm chấm công | ~314.000 |
| Ngành có lao động làm ca cố định tại chỗ (~40%) | Sản xuất, bán lẻ, F&B, khách sạn, logistics, y tế | ~125.000 |
| Quy mô 20–200 LĐ, tại HN/HCM/ĐN/Bình Dương/Đồng Nai, đã số hoá cơ bản (~22%) | Vùng go-to-market năm 1–2 | **~27.000** |

**Benchmark khác:**

- Giá đối thủ: ACheckin gói Starter **25.000đ/nhân viên/tháng** — [acheckin.vn](https://acheckin.vn/)
- Adoption rate B2B Việt Nam 0,2–1%/tháng · Churn B2B SaaS <2%, AI product <5% · CAC Payback <12 tháng · Tiền mặt pre-seed VN 1–5 tỷ · WACC AI startup 20–25% — Handbook Day 24 §2, §3
- LTV/CAC median public SaaS **4,2** — KeyBanc SaaS Survey 2024
- COGS AI product 40–60% revenue (vs SaaS truyền thống 10–20%) — [a16z, *The New Business of AI*](https://a16z.com/the-new-business-of-ai-and-how-its-different-from-traditional-software/)
- Mở rộng TAM: mục tiêu 2 triệu doanh nghiệp năm 2030 theo NQ 68/NQ-TW — [Báo Chính phủ](https://baochinhphu.vn/them-mot-trieu-doanh-nghiep-tiem-nang-lon-tu-5-trieu-ho-kinh-doanh-102250411152125423.htm)
- Dữ liệu sinh trắc học thuộc dữ liệu cá nhân nhạy cảm — Nghị định 13/2023/NĐ-CP

---

## Khai báo sử dụng AI

Bài làm này có sử dụng AI (Claude Code).

**AI đã làm:** tra cứu benchmark thị trường và giá đối thủ · gợi ý danh mục AI Hidden Costs theo dạng sản phẩm · thao tác ghi số vào file Excel · viết script Python mô phỏng lại công thức Tab 3 để kiểm chứng 5 gate trước khi mở file · soạn bản nháp Decision Note từ các con số đã chốt.

**Tôi đã làm:** chọn dự án và persona · duyệt hoặc sửa từng con số giả định trước khi ghi vào file · quyết định các điểm gây tranh cãi (cắt lương thay vì hire thêm ở kịch bản Pessimistic; giữ Initial Cash và Initial Investment giống nhau ở cả 3 kịch bản) · xác nhận từng phase trước khi sang phase tiếp theo.

Mọi con số trong file đều có căn cứ dẫn nguồn ở mục **Nguồn tham khảo** hoặc bóc tách bottom-up ở mục **Kết quả 3 kịch bản**.

---

### 🏛️ VinUniversity Codelab
* **Program:** AI Talent Incubation (Cohort 2026)
* **Track:** Track 1 — AI Product Management
