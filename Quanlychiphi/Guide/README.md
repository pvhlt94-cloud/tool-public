# Mô tả file hướng dẫn đơn giá PL02 – BHXH tỉnh Phú Thọ 2026

**File:** `19.11.2026 PL02 Đơn giá chung chi trả BHXH tỉnh Phú Thọ 2026.xlsx`
**Nội dung:** Bảng đơn giá chung áp dụng trong tỉnh năm 2026. BHXH tỉnh ban hành và gửi BHXH cơ sở trước khi cơ sở kê khai Phụ lục số 01 (sheet `Bieu_xa`).
**Dùng bởi:** công cụ `../KiemTra_PL01.html`. Công cụ đã nhúng sẵn số liệu của bản 19/11/2026. Khi có bản mới, vào mục *Tuỳ chọn → Chọn file hướng dẫn* để nạp lại.

## Tổng quan các sheet

| Sheet | Vai trò | Ai sửa |
|---|---|---|
| `Tham_so` | Tham số gốc: lương tối thiểu vùng, giá thuê, giá xe, nguyên giá thiết bị, giá in… | BHXH tỉnh (ô chữ xanh) |
| `PL02_Don_gia` | Bảng đơn giá theo 27 khoản của PL01, **tự tính từ `Tham_so`** | Không sửa trực tiếp (công thức) |
| `Quy_doi_148_xa` | Danh sách 148 xã/phường, kèm vùng lương tối thiểu và hệ số phụ cấp khu vực | BHXH tỉnh |
| `Sheet1` | Trống | – |

> Sửa giá trị trong `Tham_so` thì `PL02_Don_gia` và `Quy_doi_148_xa` tự tính lại.

---

## 1. Sheet `Tham_so` – Tham số tính đơn giá

**Cấu trúc:** tiêu đề ở dòng 4, dữ liệu từ dòng 5 đến dòng 39.

| Cột | Tên | Ý nghĩa |
|---|---|---|
| A | Mã | Mã tham số. Công thức và công cụ HTML tham chiếu theo mã này |
| B | Tham số | Tên tham số |
| C | Giá trị | Giá trị số (ô nhập) |
| D | ĐVT | Đơn vị tính |
| E | Nguồn / căn cứ | Văn bản, căn cứ |

**Danh sách tham số (bản 19/11/2026):**

| Ô | Mã | Tham số | Giá trị | ĐVT | Dùng cho khoản |
|---|---|---|---:|---|---|
| C5 | LT2 | Lương tối thiểu vùng II | 4.730.000 | đ/tháng | Ngày công (1, 2, 4, 6, 8, 21, 25, 26) |
| C6 | LT3 | Lương tối thiểu vùng III | 4.140.000 | đ/tháng | như trên |
| C7 | LT4 | Lương tối thiểu vùng IV | 3.700.000 | đ/tháng | như trên |
| C8 | HS | Hệ số lương nhân công, bảo vệ so với LTTV | 1,8 | lần | như trên |
| C9 | NC | Số ngày công/tháng | 26 | ngày | Ngày công, địa điểm, khấu hao dùng chung |
| C10 | PH | Số phút 01 ngày công | 480 | phút | Khoản 4, 21 |
| C11 | KH | Thời gian khấu hao thiết bị | 60 | tháng | Khoản 13–17 |
| C12 | MB2 | Giá thuê mặt bằng 20 m² – vùng II | 6.000.000 | đ/tháng | Khoản 5, 24 |
| C13 | MB3 | Giá thuê mặt bằng 20 m² – vùng III | 5.000.000 | đ/tháng | Khoản 5 |
| C14 | MB4 | Giá thuê mặt bằng 20 m² – vùng IV | 4.000.000 | đ/tháng | Khoản 5 |
| C15 | DT | Diện tích mặt bằng chuẩn | 20 | m² | Khoản 5, 24 |
| C16 | XE0 | Thuê xe chở tiền có lái – không có PCKV | 1.100.000 | đ/ngày | Khoản 7 |
| C17 | XE1 | Thuê xe chở tiền có lái – PCKV 0,1–0,2 | 1.200.000 | đ/ngày | Khoản 7 |
| C18 | XE3 | Thuê xe chở tiền có lái – PCKV từ 0,3 | 1.350.000 | đ/ngày | Khoản 7 |
| C19 | DL0 | Đi lại 01 lượt – không có PCKV | 5.000 | đ/lượt | Khoản 3, 23 |
| C20 | DL1 | Đi lại 01 lượt – PCKV 0,1–0,2 | 10.000 | đ/lượt | Khoản 3, 23 |
| C21 | DL3 | Đi lại 01 lượt – PCKV từ 0,3 | 15.000 | đ/lượt | Khoản 3, 23 |
| C22 | GL | Thời gian 01 lượt chi trả tại nhà | 0,5 | giờ | Khoản 3 |
| C23 | MT | Máy tính xách tay – nguyên giá | 18.000.000 | đ/máy | Khoản 13 |
| C24 | DD | Đầu đọc thẻ – nguyên giá | 300.000 | đ/máy | Khoản 14 |
| C25 | WC | Webcam – nguyên giá | 420.000 | đ/máy | Khoản 15 |
| C26 | MD | Máy đếm tiền – nguyên giá | 4.400.000 | đ/máy | Khoản 16 |
| C27 | TT | Thùng tôn đựng tiền – nguyên giá | 400.000 | đ/chiếc | Khoản 16 |
| C28 | IN | In, photo 01 trang A4 | 500 | đ/trang | Khoản 9, 10, 12, 19, 20 |
| C29 | NT | Số người/trang danh sách | 20 | người | Khoản 9, 12, 19 |
| C30 | SB | Số bản in danh sách | 2 | bản | Khoản 9, 12, 19 |
| C31 | TM | Số trang mẫu khai báo thay đổi thông tin (14-HSB) | 3 | trang | Khoản 10 |
| C32 | TG | Số trang mẫu báo giảm | 1 | trang | Khoản 20 |
| C33 | THE | Làm 01 thẻ chi trả | 30.000 | đ/thẻ | Khoản 11 |
| C34 | CU | Cước điện thoại | 990 | đ/phút | Khoản 22 |
| C35 | NU | Nước uống tại điểm chi trả | 100.000 | đ/điểm/ngày | Khoản 9 |
| C36 | VP | Văn phòng phẩm tại điểm chi trả | 50.000 | đ/điểm/ngày | Khoản 9 |
| C37 | LT | Diện tích lưu trữ danh sách chi trả | 2 | m² | Khoản 24 |
| C38 | LG | Số lần liên lạc người hưởng/năm | 4 | lần | Khoản 22 |
| C39 | PG | Số phút/lần liên lạc | 2 | phút | Khoản 22 |

---

## 2. Sheet `PL02_Don_gia` – Bảng đơn giá chung

**Cấu trúc:**
- Dòng 1–2: tiêu đề.
- Dòng 4: tên cột. Dòng 5: số thứ tự cột (1)…(8).
- Từ dòng 6: dữ liệu. Dòng chữ cái (A, B, C) và số La Mã (I–V) là dòng nhóm. Dòng có số ở cột A là dòng khoản (1–27). Các dòng `   – …` ngay dưới là thành phần đơn giá của khoản đó.

| Cột | Tên | Ý nghĩa |
|---|---|---|
| A | Khoản PL01 | Số thứ tự khoản chi trong Phụ lục 01 (1–27), hoặc mã nhóm (A, B, C, I–V) |
| B | Nội dung khoản chi phí / thành phần đơn giá | Tên khoản; các dòng `–` là từng mức đơn giá theo vùng, PCKV hoặc thành phần |
| C | ĐVT | Đơn vị tính của khối lượng (dòng khoản) hoặc của đơn giá (dòng thành phần) |
| D | Đơn giá (đồng) hoặc hệ số | Mức đơn giá. Phần lớn là công thức lấy từ `Tham_so`; một số dòng ghi chữ “Theo thực tế”, “Theo giá thị trường” |
| E | Phạm vi áp dụng | Áp dụng cho vùng nào, nhóm PCKV nào, toàn tỉnh hay cấp tỉnh |
| F | Cách tính, căn cứ xác định | Công thức diễn giải, văn bản căn cứ |
| G | Ghi vào Phụ lục 01 (sheet Bieu_xa) | Vị trí ghi đơn giá trong `Bieu_xa` (ví dụ “Khoản 1 – dòng 46”) |
| H | Ghi chú | Cách xác định **khối lượng** (KL), giới hạn, lưu ý khi kê khai |

### Đơn giá theo từng khoản

Giá trị dưới đây là kết quả tính với tham số bản 19/11/2026. Cột “Dòng” là dòng trong sheet `PL02_Don_gia`; “Dòng Bieu_xa” là dòng đơn giá trong file kê khai của cơ sở (dòng khối lượng = dòng đơn giá − 1, dòng thành tiền = dòng đơn giá + 1).

#### A. Chi trả bằng tiền mặt

| Khoản | Dòng | Thành phần | Công thức | Vùng II | Vùng III | Vùng IV | Dòng Bieu_xa | Khối lượng (cột H) |
|---|---|---|---|---:|---:|---:|---|---|
| 1. Nhân công chi trả theo lịch tại các điểm | 9–11 | Ngày công | LT × HS : NC | 327.462 | 286.615 | 256.154 | 46 | Số ngày chi trả theo lịch × số NV/ngày |
| 2. Nhân công tại trụ sở GD ngày còn lại | 13–15 | Ngày công | = khoản 1 | 327.462 | 286.615 | 256.154 | 49 | Số ngày ngoài lịch × (giờ chi trả/ngày : 8) |
| 4. Nhân công theo dõi ủy quyền nhận thay | 21–23 | Ngày công | = khoản 1 | 327.462 | 286.615 | 256.154 | 55 | Số lượt ủy quyền × 10 phút : 480 |
| 5. Địa điểm chi trả | 26–28 | Điểm 20 m²/ngày | MB : NC | 230.769 | 192.308 | 153.846 | 58 | Số ngày. Nhiều loại điểm thì lấy bình quân; điểm mượn chỉ tính chi phí thực tế |
| 6. Thuê bảo vệ tại điểm | 30–32 | 01 bảo vệ/ngày | = khoản 1 | 327.462 | 286.615 | 256.154 | 61 | Bảo vệ sẵn có không trả tiền thì không kê |
| 8. Thuê bảo vệ xe vận chuyển tiền | 38–40 | 01 bảo vệ/ngày | = khoản 1 | 327.462 | 286.615 | 256.154 | 67 | 01 người vừa bảo vệ điểm vừa áp tải xe chỉ tính 1 lần |

Khoản tính theo **nhóm phụ cấp khu vực**:

| Khoản | Dòng | Thành phần | Không có PCKV | PCKV 0,1–0,2 | PCKV từ 0,3 | Dòng Bieu_xa | Ghi chú |
|---|---|---|---:|---:|---:|---|---|
| 3. Chi trả tại nơi cư trú | 17–19 | Đi lại 01 lượt | 5.000 | 10.000 | 15.000 | 52 | KL = chỉ tiêu 2.1.3. Đơn giá = 0,5 giờ : 8 × ngày công vùng + đi lại 01 lượt |
| 7. Thuê phương tiện vận chuyển tiền | 34–36 | Xe 7 chỗ có lái/ngày | 1.100.000 | 1.200.000 | 1.350.000 | 64 | Xe phục vụ nhiều xã trong ngày chỉ ghi tại 01 xã; mức cao hơn phải thuyết minh cung đường, số km |

Khoản áp dụng **toàn tỉnh**:

| Khoản | Dòng | Thành phần | Đơn giá | Công thức | Dòng Bieu_xa | Khối lượng / ghi chú |
|---|---|---|---:|---|---|---|
| 9. In DS chi trả, nước uống, VPP | 43 | (a) In DS – 01 trang | 500 đ/trang | IN | 70 | Đơn giá = [(a)+(b)+(c)] : chỉ tiêu 2.1, tính riêng từng xã |
| | 44 | (b) Nước uống | 100.000 đ/điểm/ngày | NU | | (b) = số ngày chi trả theo lịch × mức |
| | 45 | (c) Văn phòng phẩm | 50.000 đ/điểm/ngày | VP | | (c) = số ngày chi trả theo lịch × mức |
| | | (a) cụ thể | | ⌈người TM bình quân/tháng : 20⌉ × 2 bản × 12 tháng × 500 | | Xã không đặt điểm chi trả chỉ tính (a) |
| 10. Photo mẫu 14-HSB | 47 | 01 mẫu (3 trang) | 1.500 đ/mẫu | TM × IN | 73 | KL = số mẫu thực tế |
| 11. Làm thẻ chi trả | 49 | 01 thẻ | 30.000 đ/thẻ | THE | 76 | KL = số thẻ làm mới thực tế |
| 12. In DS ủy quyền nhận thay | 51 | 01 lượt | 50 đ/lượt | IN × SB : NT | 79 | KL = số lượt ủy quyền, ≤ chỉ tiêu 2.1 |
| 13. Khấu hao máy tính xách tay | 54–55 | Nguyên giá / khấu hao 100% | 18.000.000 / 300.000 đ/tháng | MT : KH | 82 | KL ≤ chỉ tiêu 1 × 12. Dùng chung: × số ngày chi trả/tháng : 26. Không kê máy quá 5 năm, máy mượn |
| 14. Khấu hao đầu đọc thẻ | 57–58 | Nguyên giá / khấu hao 100% | 300.000 / 5.000 đ/tháng | DD : KH | 85 | KL ≤ chỉ tiêu 1 × 12 |
| 15. Khấu hao webcam | 60–61 | Nguyên giá / khấu hao 100% | 420.000 / 7.000 đ/tháng | WC : KH | 88 | KL ≤ chỉ tiêu 1 × 12 |
| 16. Khấu hao máy đếm tiền, thùng tôn | 63–66 | Máy đếm + thùng / chỉ máy đếm | 80.000 / 73.333 đ/tháng | (MD+TT) : KH / MD : KH | 91 | Không có thùng tôn thì chỉ tính máy đếm |
| 17. Thiết bị khác | 68 | – | Theo giá thị trường | Nguyên giá × tỷ lệ dùng : 60 | 94 | Ghi rõ tên thiết bị, nguồn giá tại Thuyet_minh |
| 18. Chi phí khác (tiền mặt) | 71 | – | Theo thực tế | KL = 1; ĐG = tổng chi phí | 97 | Bắt buộc thuyết minh |

#### B. Quản lý người hưởng

| Khoản | Dòng | Đơn giá | Công thức | Dòng Bieu_xa | Khối lượng / ghi chú |
|---|---|---:|---|---|---|
| 19. In DS rà soát, đối chiếu | 74 | 50 đ/lượt | IN × SB : NT | 102 | KL = chỉ tiêu 3.1 |
| 20. In mẫu báo giảm | 76 | 500 đ/mẫu | TG × IN | 105 | KL = chỉ tiêu 3.3.1 |
| 21. Nhân công quản lý, theo dõi người hưởng | 78–80 | 327.462 / 286.615 / 256.154 (vùng II/III/IV) | = khoản 1 | 108 | KL theo công việc thực tế hoặc số người bố trí × ngày công × tháng (kiêm nhiệm tính theo phần thời gian); không trùng khoản 1, 2, 4 |
| 22. Liên lạc điện thoại | 82 | 990 đ/phút | CU | 111 | KL = số người hưởng × 4 lần/năm × 2 phút/lần |
| 23. Chi phí khác (quản lý) | 84–86 | Đi lại xác minh (xe máy): 5.000 / 10.000 / 15.000 đ/lượt theo nhóm PCKV | DL0 / DL1 / DL3 | 114 | KL = số lượt xác minh thực tế (CV 3018/BHXH-CĐBHXH). Kê theo phương án khác (KL = 1, ĐG = tổng chi phí) thì khoản 19–22 ghi 0 |

#### C. Chi phí tính theo đơn vị (chỉ BHXH tỉnh nhập ở cột CỘNG – cơ sở không kê)

| Khoản | Dòng | Đơn giá | Công thức | Dòng Bieu_xa | Ghi chú |
|---|---|---:|---|---|---|
| 24. Bảo quản, lưu trữ DS chi trả có chữ ký | 89 | 600.000 đ/tháng | LT × MB2 : DT (2 m² giá vùng II) | 119 | KL = 12 tháng |
| 25. Chi phí khác chi trả tiền mặt (giám sát điểm, đối chiếu tiền) | 91 | 327.462 đ/ngày công | = ngày công vùng II | 122 | Nội dung khác theo thực tế, có thuyết minh |
| 26. Nhân công đầu mối quản lý người hưởng | 93 | 327.462 đ/ngày công | = ngày công vùng II | 125 | Tổng hợp toàn tỉnh, không trùng khoản 21 |
| 27. Chi phí khác quản lý người hưởng | 95 | Theo thực tế | – | 128 | Hồ sơ, biên bản từng trường hợp |

---

## 3. Sheet `Quy_doi_148_xa` – Vùng lương và phụ cấp khu vực theo xã

**Căn cứ:** vùng lương tối thiểu theo NĐ 293/2025/NĐ-CP; phụ cấp khu vực theo Thông tư 15/2026/TT-BNV (VBHN 11/2026/VBHN-BNV, mục IX – Phú Thọ).
**Cấu trúc:** tiêu đề ở dòng 4; dữ liệu từ dòng 5 đến dòng 152 (148 đơn vị); bảng tổng hợp ở dòng 154–163.

| Cột | Tên | Kiểu | Ý nghĩa |
|---|---|---|---|
| A | STT | Số | 1–148 |
| B | Tên xã, phường | Chữ | Tên không kèm tiền tố “xã/phường” (ví dụ `Lâm Thao`) |
| C | Loại | `Xã` / `Phường` | |
| D | Vùng LTTV | `II` / `III` / `IV` | Quyết định mức **ngày công** (khoản 1, 2, 4, 6, 8, 21) và **giá mặt bằng** (khoản 5) |
| E | Hệ số PCKV | Số: 0; 0,1; 0,2; 0,3; 0,4; 0,5 | Hệ số phụ cấp khu vực của xã |
| F | Nhóm địa bàn | Công thức | `Không có PCKV` (E = 0), `PCKV 0,1 – 0,2` (E ≤ 0,2), `PCKV 0,3 – 0,5` (E > 0,2). Quyết định giá **thuê xe** (khoản 7) và **đi lại** (khoản 3, 23) |

**Thống kê (bản 19/11/2026):**

| | Số đơn vị |
|---|---:|
| Vùng II / III / IV | 26 / 45 / 77 |
| Phường / Xã | 15 / 133 |
| PCKV 0 / 0,1 / 0,2 / 0,3 / 0,4 / 0,5 | 34 / 47 / 28 / 25 / 6 / 8 |
| Nhóm: Không có PCKV / 0,1–0,2 / 0,3–0,5 | 34 / 75 / 39 |

Thứ tự dòng: dòng 5–30 vùng II, dòng 31–75 vùng III, dòng 76–152 vùng IV (trong vùng IV xếp theo PCKV giảm dần).

**Cách tra:** tìm tên xã ở cột B, lấy vùng ở cột D và nhóm địa bàn ở cột F, rồi đối chiếu với bảng đơn giá ở mục 2.
Ví dụ: *Lâm Thao* → vùng III, không có PCKV → ngày công 286.615 đ, mặt bằng 192.308 đ/ngày, thuê xe 1.100.000 đ/ngày.

---

## 4. Liên hệ với file kê khai của cơ sở và công cụ kiểm tra

- Trong file kê khai (sheet `Bieu_xa`), dòng 6 là vùng lương và dòng 7 là mức phụ cấp khu vực (`Không có`, `Mức 0,1`…). Hai dòng này phải khớp cột D, E của `Quy_doi_148_xa`.
- Công cụ `KiemTra_PL01.html` đọc từ file này:
  - `Tham_so`: cột A (mã) và cột C (giá trị), mọi dòng có giá trị số.
  - `Quy_doi_148_xa`: từ dòng 5, cột B (tên), C (loại), D (vùng), E (hệ số PCKV).
  - Không đọc `PL02_Don_gia`. Công cụ tự tính lại đơn giá từ `Tham_so` theo đúng công thức ở cột D của sheet này.
- Nếu BHXH tỉnh thêm tham số hoặc đổi mã ở cột A của `Tham_so`, phải cập nhật lại công cụ cho tương ứng.
