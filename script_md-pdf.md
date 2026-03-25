- Конвертування markdown у PDF
```bash
pandoc README.md -s \
  --pdf-engine=xelatex \
  -V mainfont="DejaVu Serif" \
  -V monofont="DejaVu Sans Mono" \
  -V fontsize=12pt \
  -V linestretch=1.15 \
  -V geometry:a4paper \
  -V geometry:margin=20mm \
  -V geometry:landscape \
  --toc --toc-depth=3 \
  --number-sections \
  --metadata title="PostgreSQL" \
  --metadata subtitle="Огляд процедурної мови PL/pgSQL" \
  --metadata author=" " \
  --metadata date="2026-03-25" \
  -H ./header.tex \
  -o PL_pgSQL.pdf
```