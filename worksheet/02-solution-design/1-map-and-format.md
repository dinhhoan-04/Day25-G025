---
artifact: 1 - FINAL ke hoach giai phap
bai-tap: 2 - Thiet ke giai phap
phase: Chon rui ro + chon tang + chon demo + chot 3 lop
---

# 1 - FINAL: Ke hoach giai phap

## Thong tin nhom

- **Chu de**: 7 - Tro ly sang loc CV va tuyen dung
- **Thanh vien**: Do Dinh Hoan (2A202600036); Nguyen Viet Hung (2A202600240)
- **Ngay**: 2026-05-13

## Phan A - Chon rui ro va tang giai phap

### Rui ro chinh duoc chon

- **ID tinh huong**: T-01 + T-02
- **Mo ta ngan**: Khi CV khong theo mau pho bien (gap year, truong dia phuong), AI co xu huong ha diem va de xuat loai thay vi flag review, gay bo sot ung vien phu hop.
- **Muc do**: Nang
- **Diem rui ro**: 20
- **Vi sao chon tinh huong nay**: Tac dong fairness lon nhat, lap lai de xay ra, va anh huong truc tiep den ket qua shortlist.

### Tim nguyen nhan goc

- [x] Thieu nguon du lieu dung.
- [x] AI doan khi khong biet.
- [x] Giao dien khien nguoi dung tin qua muc.
- [x] Quy trinh thieu nguoi duyet/flag review.
- [ ] Khong co theo doi sau khi ra mat.
- [ ] Khac.

### Bang noi nguyen nhan voi tang sua

| Nguyen nhan goc | Tang uu tien sua | Lop giai phap lien quan |
|---|---|---|
| Feature extraction thien ve keyword title chuan | Du lieu / tra cuu / rule ranking | `3-architecture` la chinh |
| AI de xuat "co the loai" qua tu tin | Prompt va rule refusal/escalation | `2-prompt` la chinh |
| Recruiter de anchoring vao top score | UI canh bao confidence + random-check | `1-uiux` la chinh |
| Case mo ho khong duoc chuyen review tay | Human review gate trong flow | `1-uiux` + `3-architecture` |

### 10 tang giai phap tham khao (chon ap dung)

- [x] Giao dien
- [x] Chi dan AI
- [x] Quy trinh xu ly
- [x] Du lieu / tra cuu nguon
- [x] Theo doi
- [ ] Chinh sach / thong bao gioi han
- [x] Nguoi duyet / phe duyet
- [ ] Vai tro trach nhiem
- [x] Vong phan hoi
- [x] Kien truc lai

### 4 hanh dong phong ve

- **Ngan**: Rule prompt cam auto-reject khi uncertainty > nguong.
- **Phat hien**: Architecture ghi log "bias risk flag" khi CV co pattern gap year/format la.
- **Khac phuc**: UI bat buoc recruiter review 20% CV ngoai top.
- **Thong bao**: UI hien nhan "Shortlist so bo - can review tay".

### Ket luan Phan A

**Nguyen nhan goc**: keyword bias + over-confidence + anchoring UI.

**Tang chinh can sua**: du lieu/architecture + prompt, bo tro boi UI.

**Vi sao can 3 lop giai phap**:

- Lop giao dien: giam over-reliance cua recruiter.
- Lop chi dan AI: chan tu goc cac cau de xuat reject vo can cu.
- Lop kien truc du lieu: dam bao ranking dua tren feature dung va co monitoring.

## Phan B - Chon dinh dang demo

| Lop | Thu muc | Dinh dang demo chon | Thoi gian du kien |
|---|---|---|---|
| Giao dien | `1-uiux` | ASCII wireframe trong Markdown | 20 phut |
| Chi dan AI | `2-prompt` | Prompt + test examples Markdown | 15 phut |
| Kien truc du lieu | `3-architecture` | ASCII data-flow + bang thanh phan | 20 phut |

**Ly do chon demo**

- Giao dien: ASCII du nhanh de review logic canh bao/escalation.
- Chi dan AI: Markdown de de copy test lap lai.
- Kien truc du lieu: ASCII flow de thay ro diem kiem tra nguon va logging.

## Phan C - Ba lop giai phap

### Lop 1 - Giao dien (`artifact/1-uiux/`)

- **Cach tiep can**: Them trang thai do tin cay + bat buoc random-check + nut escalation recruiter lead.
- **Hanh dong phong ve bao phu**: [Thong bao] [Khac phuc]
- **Demo**: ASCII man hinh shortlist + state canh bao.
- **Trang thai**: Xong

Link chi tiet:

- `artifact/1-uiux/card.md`
- `artifact/1-uiux/demo.md`

### Lop 2 - Chi dan AI (`artifact/2-prompt/`)

- **Cach tiep can**: Prompt rule "khong auto reject" + "yeu cau bang chung" + "flag uncertainty".
- **Hanh dong phong ve bao phu**: [Ngan] [Tu choi] [Hoi lai]
- **Demo**: Prompt tham khao + 3 test case tu bo FINAL.
- **Trang thai**: Xong

Link chi tiet:

- `artifact/2-prompt/card.md`
- `artifact/2-prompt/demo.md`

### Lop 3 - Kien truc du lieu (`artifact/3-architecture/`)

- **Cach tiep can**: Tach bu?c parse-feature-score, them fairness guardrail va monitoring loop.
- **Hanh dong phong ve bao phu**: [Ngan] [Phat hien] [Khac phuc]
- **Demo**: ASCII luong du lieu + fail-safe khi thieu du lieu.
- **Trang thai**: Xong

Link chi tiet:

- `artifact/3-architecture/card.md`
- `artifact/3-architecture/demo.md`

## Tong kiem tra

| Cau hoi | Tra loi |
|---|---|
| Rui ro chinh da chon la gi? | T-01/T-02 |
| Nguyen nhan goc la gi? | keyword bias + AI over-confidence + anchoring UI |
| 3 lop giai phap da du chua? | Giao dien: Co / Chi dan AI: Co / Kien truc: Co |
| 4 hanh dong da bao phu chua? | Ngan: Co / Phat hien: Co / Khac phuc: Co / Thong bao: Co |
| Nhom khac da gop y chua? | Tu review theo checklist |
| Da sua gi sau phan bien? | Them random-check 20% va fail-safe parse loi |

## Phan bien cheo: 4 cau phai tra loi

| Goc phan bien | Cau hoi |
|---|---|
| Dung tang | Giai phap co sua dung nguyen nhan goc khong? |
| Cu the | Demo co du ro de hieu cach van hanh khong? |
| Du lop | 3 lop co bo sung cho nhau khong? |
| Tac dung phu | Co lam cham/roi/rui ro moi khong? |
