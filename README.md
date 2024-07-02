# handwritten-table-extraction-ocr

**DESCRIPTION:**

This project processes scanned images of handwritten tables to automatically detect and recognize the tabular structure and content. It utilizes pretrained OCR models to accurately read handwritten entries and fill in an Excel sheet, mirroring the original layout. This project significantly reduces manual data entry effort and improves efficiency in handling handwritten documents.

(Note: This is a primary version, increasing the accuracy can be further worked upon)

**TIMELINE:**
![image](https://github.com/natashasalvi2003/handwritten-table-extraction-ocr/assets/123302023/5ba28c49-c881-4886-9343-e4e8813613ad)

**DATA FLOW DIAGRAM:**
![image](https://github.com/natashasalvi2003/handwritten-table-extraction-ocr/assets/123302023/3e238c89-c630-4026-9889-6f8fafcf8b4b)

**SAMPLE OUTPUT:**
![SAMPLE_OUTPUT](https://github.com/natashasalvi2003/handwritten-table-extraction-ocr/assets/123302023/4f664a04-7bbd-4314-b647-453f0409c552)

![SAMPLE_OUTPUT_EXCEL](https://github.com/natashasalvi2003/handwritten-table-extraction-ocr/assets/123302023/f9e48084-f2ac-4627-91ee-9e35613101cc)

**ACCURACY, LIMITATIONS AND FUTURE SCOPE:**

1. The current accuracy of the program is roughly 75-80%. It can be further improved by substituting the pretrained model used, with a model that is actively trained using the IAM dataset.

2. The current implementation of the code runs efficiently on powerful GPU machines in Google Colab but takes longer to execute on a local Jupyter notebook. As this is a preliminary version, future improvements can be made by optimizing and testing the code on a PC with a robust GPU to enhance performance.

3. There is one anamoly that needs to be worked upon that occurs when certain images are not cropped correctly, resulting in an error. This anomaly occurs when the table is unable to identify a cell in the table resulting in a NULL value being returned, which causes an error to spring up.
(UPDATE: this error has been temporarily handled (in TROCR_v2.ipynb) by replacing the unrecognized text with a blank “ ”  to avoid the program from abruptly stopping, and ensure its smooth completion)

**CREDIT:**
Pretrained model used: [TROCR](https://huggingface.co/microsoft/trocr-base-handwritten)
Table detection model used: [IMG2TABLE](https://github.com/xavctn/img2table)
