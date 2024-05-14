## Quire PDF testing starter project template

In this tester, each of the `output-variant` directories are of a single layout, and each have and index and nine numbered markdown pages. The pages follow the pattern below, so that `output-variants--bibliography/5.md` and `content/output-variants--page/5.md` are the same other than their layout.

With `pdf.pagePDF.output: true`, PDFs at index, 2, 5, 8, and 9 should generate, and only index, 8, and 9 should have access links.

With `pdf.pagePDF.output: false`, only PDF 2 and 8 should generate, and only 8 should have accessLinks.

```yaml
label: 1
title: Output PDF / Page Output False
outputs: [ pdf ]
page_pdf_output: false
# output: false == no pdf
# output: true == no pdf

label: 2
title: Output PDF / Page Output True
outputs: [ pdf ]
page_pdf_output: true
# output: false == pdf
# output: true == pdf

label: 3
title: Output HTML / Page Output False
outputs: [ html ]
page_pdf_output: false
# output: false == no pdf
# output: true == no pdf

label: 4
title: Output HTML / Page Output True
outputs: [ html ]
page_pdf_output: true
# output: false == no pdf
# output: true == no pdf

label: 5
title: Output PDF / Page Output Empty
outputs: [ pdf ]
# output: false == no pdf
# output: true == pdf

label: 6
title: Output HTML / Page Output Empty
outputs: [ html ]
# output: false == no pdf
# output: true == no pdf

label: 7
title: Output ALL / Page Output False
page_pdf_output: false
# output: false == no pdf
# output: true == no pdf

label: 8
title: Output ALL / Page Output True
page_pdf_output: true
# output: false == pdf
# output: true == pdf

label: 9
title: Output ALL / Page Output Empty
# output: false == no pdf
# output: true == pdf
```
