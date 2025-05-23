# 📊 PDF Table Extraction Comparison

This repository was created to **compare various tools** that can be used to extract **tabular data** from PDF files — whether the data is embedded as **text** or present in **image-based** formats.

---

## 🧪 Comparison Metrics

Each tool is evaluated on the following criteria:

1. ⚡ **Speed** of table extraction  
2. 🎯 **Accuracy** of the extracted data  
3. 🧠 **Versatility** – handles both image-based and text-based PDFs  
4. 💻 **Resource Utilization** (e.g., CPU/GPU use)  
5. 🛠️ **Ease of Post-processing** (conversion to CSV, Excel, or DataFrames)
6. 🧩 **Structural fidelity i.e. Table layout preservation for merged cells

---

## 🔧 Tools Evaluated

| Tool              | Status                                      |
|-------------------|---------------------------------------------|
| ✅ `img2table`     | Included                                     |
| ✅ `pdf2table`     | Included                                     |
| ✅ `pdfplumber`    | Included                                     |
| ✅ `pymupdf`       | Included                                     |
| ⚠️ `image-to-excel` | Not included (limited documentation)        |
| ❌ `camelot`       | Not included (performance not satisfactory) |

---

## 📂 Source Code

All implementation and benchmarking code is available in the form of a **Jupyter Notebook**.

---

## 📊 Tool Comparison Summary

| Tool        | ⏱️ Time (CPU)              | ⏱️ Time (GPU)         |Image or Text | CPU or GPU Utilization | CSV, Dataframe| 🎯 Accuracy        | 📝 Remarks |
|-------------|----------------------------|------------------------|-----------------|-------------------------|---------------|--------------------|------------|
| **img2table** | 2.5 sec                  | 2.5 sec                |Both Image and Text | CPU, GPU | Dataframe | ✅ ~60%             | Promising results for both image and text-based PDFs, but requires manual post-processing for reliable output. |
| **pdf2table** | ❗ Very slow (heavy models) | 3–4 sec per image      |Both Image and Text | CPU, GPU | Dataframe | ✅ ~90%             | Highly accurate for scanned/image PDFs. Best option when working with image-based tables. |
| **pdfplumber** | 1.2 sec for 4 PDFs        | N/A                    | Only Text | CPU | Dataframe | ✅ High (text PDFs) | Excellent for text-based PDFs. Not very effective for image-based extraction. |
| **pymupdf** | 1.2 sec for 4 PDFs        | N/A                    | Only Text| CPU | Dataframe | ✅ High (text PDFs) | Fast and accurate for text PDFs. OCR-based extraction not very reliable. |
