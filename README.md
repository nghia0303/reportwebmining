# Overleaf IEEE Report Project

Folder này là project LaTeX hoàn chỉnh cho báo cáo bài tập lớn theo phong cách IEEE Conference.

## Files

- `main.tex`: nội dung báo cáo chính.
- `references.bib`: bibliography theo BibTeX/IEEEtran.
- `latexmkrc`: ép Overleaf dùng XeLaTeX để compile tiếng Việt ổn định.

## Cách dùng trên Overleaf

1. Nén hoặc upload toàn bộ folder này lên Overleaf.
2. Đặt `main.tex` làm main document.
3. Compiler nên là `XeLaTeX`. File `latexmkrc` đã cấu hình sẵn cho Overleaf.
4. Compile theo chu trình bình thường; bibliography dùng `IEEEtran`.

## Ghi chú nội dung

- Báo cáo dùng số liệu từ final benchmark:
  `data/eval/runs/final_coverage_20260428T175804Z`.
- Search/Chat production metrics dùng Milvus `partial-index-39336`.
- Analytics metrics dùng SQLite full `557,134` papers.
- Các lỗi runtime model như `BAAI/bge-m3` được ghi là stability/configuration finding, không phải kết luận chất lượng model.

## Nguồn template

IEEE khuyến nghị dùng conference manuscript templates và conference mode cho LaTeX. Trang chính thức:

https://www.ieee.org/conferences/publishing/templates.html

