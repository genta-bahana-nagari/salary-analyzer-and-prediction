# Data Science Project

Repository ini berisi notebook Python untuk analisis data, eksplorasi dataset, dan visualisasi menggunakan Jupyter Notebook.

## Project Structure

```text
my-data-science/
├── datasets/
│   └── dataset.csv
│
├── notebook/
│   └── 01-visual.ipynb
│
├── .gitignore
├── requirements.txt
└── README.md
```

## Requirements

Pastikan perangkat sudah memiliki:

- Python 3.10 atau lebih baru.
- pip (Python Package Installer).
- Visual Studio Code.
- VS Code Extensions:
  - Python (Microsoft)
  - Jupyter (Microsoft)

## Installation

### 1. Clone Repository

```bash
git clone https://github.com/genta-bahana-nagari/REPOSITORY.git

cd REPOSITORY
```

### 2. Create Virtual Environment

Buat virtual environment di dalam direktori project:

```bash
python3 -m venv .venv
```

Aktifkan environment.

**Linux / macOS:**

```bash
source .venv/bin/activate
```

**Windows (PowerShell):**

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

Pastikan virtual environment sudah aktif, kemudian jalankan:

```bash
python -m pip install --upgrade pip

python -m pip install -r requirements.txt
```

### 4. Register Jupyter Kernel

Daftarkan virtual environment sebagai Jupyter Kernel:

```bash
python -m ipykernel install --user \
    --name=my-data-science \
    --display-name="Python (My Data Science)"
```

### 5. Open Project in VS Code

```bash
code .
```

Buka file notebook di direktori `notebook/`.

Pilih kernel:

`Python (My Data Science)`

Pastikan notebook menggunakan interpreter dari virtual environment project, bukan Python global.

## Running the Notebook

Setelah memilih kernel yang benar:

1. Buka `notebook/01-visual.ipynb`.
2. Pastikan dataset tersedia di direktori `datasets/`.
3. Jalankan cell notebook secara berurutan.

Contoh membaca dataset:

```python
import pandas as pd

df = pd.read_csv("../datasets/dataset.csv")

display(df.head())
```

## Dependencies

Daftar library yang digunakan dalam project tersedia di `requirements.txt`.

Untuk melihat daftar dependency yang terpasang:

```bash
python -m pip list
```

## Troubleshooting

### ModuleNotFoundError

Jika muncul error:

```text
ModuleNotFoundError: No module named 'pandas'
```

Pastikan:

1. Virtual environment sudah aktif.
2. Dependency sudah di-install menggunakan `requirements.txt`.
3. Jupyter Notebook menggunakan kernel yang benar.

Untuk memeriksa interpreter yang sedang digunakan:

```python
import sys

print(sys.executable)
```

Path seharusnya mengarah ke `.venv/bin/python` pada Linux/macOS atau `.venv\Scripts\python.exe` pada Windows.

Jika kernel belum muncul, jalankan kembali perintah registrasi Jupyter Kernel.

## Notes

- Virtual environment (`.venv`) tidak disertakan dalam repository.
- Dependency dapat di-install kembali menggunakan `requirements.txt`.
- Dataset yang dibutuhkan harus tersedia di direktori `datasets/`.
- Jangan mengunggah file rahasia atau kredensial ke repository.

## License

Specify your project license here.