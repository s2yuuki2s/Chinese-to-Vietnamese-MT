# CSC15006 - Đồ Án Cuối Kỳ: Chinese-to-Vietnamese MT

## 1. Giới thiệu (Introduction)

Đồ án khảo sát 3 mô hình dịch máy (NMT/LLM) cho cặp ngôn ngữ **Chinese - Vietnamese**, thực hiện so sánh hiệu năng và lựa chọn 1 mô hình tối ưu nhất để fine-tune.

- **Thành viên nhóm:**
- 22127078 - Lương Quốc Dũng
- 22127250 - Trần Thành Long
- 22127260 - Bùi Công Mậu
- 22127351 - Trần Thái Minh Quân

## 2. Cấu trúc thư mục (Directory Structure)

```text
./
├── Alignment/          # Thư mục chứa dữ liệu đã được alignment (GK)
├── OCR/                # Thư mục chứa các hình ảnh được OCR để lấy dữ liệu
├── README.md           # Thông tin về dự án và hướng dẫn chạy mô hình chính
├── data/               # Chứa dữ liệu để thực hiện đồ án này
└── notebooks/          # Chứa các file notebook để thực hiện các yêu cầu của đồ án
```

## 3. Chạy khảo sát các mô hình

Tiến hành chạy khảo sát các mô hình để chọn ra mô hình tốt nhất. Các mô hình được tiến hành chạy kiểm tra trên colab.

#### MarianMT

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/MarianMT_pretrained_model.ipynb)

#### mBART50

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/mbart-test.ipynb)

#### Llama3

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](<https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/Llama3_1_(8B)_zeroshot.ipynb>)

## 3. Data cho fine tune

Đây là data được dùng để tiến hành fine-tune [link](https://drive.google.com/file/d/1L4OfhB-DTaHvP_LhOAZ52CICoeylapEk/view?usp=sharing)

## 4. Mô hình được lựa chọn để fine-tune

### Code thực thi mô hình chính

Sau quá trình đánh giá và lựa chọn. Nhóm quyết định lựa chọn mô hình Meta-Llama-3.1-8B-Instruct-bnb-4bit và được tiếp hành chạy fine tune trên nên tảng Google Colab (Google Colab hoặc Local GPU > 16GB VRAM). File code chính được đặt tên là Final.ipynb

### Open Colab

Tiến hành quá trình fine-tune mô hình trên colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/s2yuuki2s/Chinese-to-Vietnamese-MT/blob/main/notebooks/Final.ipynb)
