# CSC15006 - Đồ Án Cuối Kỳ: Chinese-to-Vietnamese MT

## 1. Giới thiệu

Đồ án khảo sát 3 mô hình dịch máy (NMT/LLM) cho cặp ngôn ngữ **Chinese - Vietnamese**, thực hiện so sánh hiệu năng và lựa chọn 1 mô hình tối ưu nhất để fine-tune.

- **Thành viên nhóm:**
- 22127078 - Lương Quốc Dũng
- 22127250 - Trần Thành Long
- 22127260 - Bùi Công Mậu
- 22127351 - Trần Thái Minh Quân

## 2. Cấu trúc thư mục

```text
./
├── Alignment/          # Thư mục chứa dữ liệu đã được alignment (GK)
├── OCR/                # Thư mục chứa các hình ảnh được OCR để lấy dữ liệu
├── README.md           # Thông tin về dự án và hướng dẫn chạy mô hình chính
├── data/               # Chứa dữ liệu để thực hiện đồ án này
└── notebooks/          # Chứa các file notebook để thực hiện các yêu cầu của đồ án
```

## 3. Dữ liệu

Dữ liệu được dùng trong các mô hình là dữ liệu đã được alignment từ data trước đó.

- Dữ liệu được gộp từ các phần alignment nhóm đã làm từ các file JSON1, JSON2 và
  PDF1, gồm có 32212 mẫu.
- Dữ liệu sẽ được chia thành 3 tập train/val/test theo tỉ lệ xấp xỉ 80/10/10:
  o Tập train: Gồm 25769 mẫu, dùng để huấn luyện fine-tune mô hình Llama3.
  o Tập val: Gồm 3221 mẫu, dùng để kiểm định mô hình fine-tune.
  o Tập test: Gồm 3222 mẫu, dùng để đưa ra đánh giá cuối cùng cho mô hình
  Llama3 sau khi fine-tune

## 4. Chạy khảo sát các mô hình

Tiến hành chạy khảo sát các mô hình để chọn ra mô hình tốt nhất. Các mô hình được tiến hành chạy kiểm tra trên colab. Dữ liệu được dùng để khảo sát là 50 câu đầu đã được alignment của file JSON2_4653_5815.csv

#### MarianMT

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/MarianMT_pretrained_model.ipynb)

#### mBART50

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/mbart-test.ipynb)

#### Llama3

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](<https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/Llama3_1_(8B)_zeroshot.ipynb>)

## 5. Data cho fine tune

Đây là data được dùng để tiến hành fine-tune [link](https://drive.google.com/file/d/1L4OfhB-DTaHvP_LhOAZ52CICoeylapEk/view?usp=sharing). Đây là dữ liệu được tổng hơp từ các file JSON1, JSON2, PDF1.

## 6. Mô hình được lựa chọn để fine-tune

### Code thực thi mô hình chính

Sau quá trình đánh giá và lựa chọn. Nhóm quyết định lựa chọn mô hình Meta-Llama-3.1-8B-Instruct-bnb-4bit và được tiếp hành chạy fine tune trên nên tảng Google Colab (Google Colab hoặc Local GPU > 16GB VRAM). File code chính được đặt tên là Final.ipynb

### Open Colab

Tiến hành quá trình fine-tune mô hình trên colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/Final.ipynb)
