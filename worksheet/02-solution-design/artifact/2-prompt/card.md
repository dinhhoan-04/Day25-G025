# card.md - Lop chi dan AI

**Tinh huong xu ly**: T-01, T-02, T-05, T-06

## 1. Giai phap la gi?

Them system prompt buoc AI: (1) khong auto reject khi uncertainty cao, (2) khong dung thuoc tinh nhay cam de cham diem, (3) neu nguoi dung ep theo keyword tho thi tu choi va de xuat quy trinh review toi thieu. Prompt cung yeu cau AI in ro `reason code` cho moi khuyen nghi.

## 2. Vi sao sua o lop chi dan AI?

- AI hien co xu huong over-confidence va de ket luan reject qua som.
- Prompt la cach sua nhanh de giam loi truoc khi thay doi model.

**Hanh dong phong ve chinh**:

- [x] Ngan cau tra loi sai ngay tu dau
- [x] Bat buoc neu nguon/bang chung voi thong tin quan trong
- [x] Tu choi tra loi khi thieu can cu
- [x] Chuyen nguoi that khi vuot pham vi

## 3. Demo nam o dau?

**File demo**: [`demo.md`](./demo.md)

Demo co:

- Rule prompt cot loi
- Mau cau khi thieu nguon
- Mau cau escalation
- Vi du test lai voi T-01, T-05, T-12

## 4. Tac dung phu

**Co the gay van de gi?**

AI co the tu choi nhieu hon, tra loi dai hon.

**Nhom giam van de do bang cach nao?**

Tach 2 muc refusal: refusal mem (yeu cau them thong tin) va refusal cung (ngoai pham vi/rui ro cao), dong thoi toi uu template cau tra loi ngan.

## 5. Checklist truoc khi nop

- [x] Luat viet du cu the de AI lam theo.
- [x] Co mau cau khi AI khong co du thong tin.
- [x] Co vi du cho tinh huong de sai.
- [x] Co thu lai bang tinh huong trong Bai 1.
- [x] Khong dung prompt nhu cach duy nhat neu loi nam o du lieu/quy trinh.

**Nguoi phu trach**: Do Dinh Hoan
