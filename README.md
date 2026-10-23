# Typst Academic Report Template

[![Typst](https://img.shields.io/badge/Typst-0.12+-239120?style=flat-square&logo=typst&logoColor=white)](https://typst.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-0d1117?style=flat-square)](LICENSE)
[![Format: A4](https://img.shields.io/badge/Format-A4-blue?style=flat-square)](main.pdf)
[![Institution](https://img.shields.io/badge/Style-HCMUS-00599C?style=flat-square)](https://hcmus.edu.vn)

A clean, modular, and publication-ready academic report template built with [Typst](https://typst.app). Designed for coursework, technical reports, and term projects at VNU-HCM University of Science (HCMUS) and extensible for any academic institution.

## Features

- **Centralized Metadata:** Strict decoupling of report metadata (`metadata.typ`), formatting rules (`src/`), and chapter contents (`content/`).
- **Standardized Typography:** Optimized for Vietnamese typography and complex mathematical typesetting with Times New Roman and Consolas font pairings.
- **Customizable Cover Page:** Full-page border frame, institutional branding, clear hierarchical title blocks, and boxed student credentials.
- **Header, Footer and Outline:** Automated page numbering, section header tracking via `chic-hdr`, and custom-aligned table of contents.
- **Syntax Highlighting:** Styled code blocks with line numbering and container styling.

## Directory Structure

```text
typst-report-template/
├── assets/
│   ├── border.png
│   ├── logo.png
│   └── preview.png
├── content/
│   ├── 01_intro.typ
│   └── 02_summary.typ
├── src/
│   ├── template.typ
│   └── theme.typ
├── metadata.typ
├── main.typ
├── main.pdf
├── .gitignore
└── LICENSE
```

## Getting Started

### Prerequisites

Install the Typst compiler via your preferred package manager:

```bash
winget install --id Typst.Typst
brew install typst
cargo install --locked typst-cli
```

*Recommended Editor:* **VS Code** with the **Tinymist Typst** extension for real-time preview and autocompletion.

### Compilation

Compile the report into a PDF:

```bash
typst compile main.typ
typst watch main.typ
```

## Configuration

All report parameters are centralized in `metadata.typ`. You do not need to modify formatting files to customize your document:

```typst
#let university = "ĐẠI HỌC QUỐC GIA THÀNH PHỐ HỒ CHÍ MINH \n TRƯỜNG ĐẠI HỌC KHOA HỌC TỰ NHIÊN"
#let faculty = "KHOA CÔNG NGHỆ THÔNG TIN"
#let department = "[Tên Bộ Môn / Chuyên Ngành]"
#let course = "[Tên Học Phần / Môn Học]"

#let project_title = "BÁO CÁO MÔN HỌC"
#let project_subtitle = "[Tên Đề Tài Báo Cáo]"

#let class_name = "[Lớp sinh hoạt / Mã lớp]"
#let author_name = "[Họ và tên sinh viên]"
#let author_id = "[Mã số sinh viên]"
#let author_email = "[Địa chỉ email]"
#let instructor_name = "[Họ và tên Giảng viên hướng dẫn]"

#let submission_date = "Thành phố Hồ Chí Minh, ngày [..] tháng [..] năm [..]"
```

## Preview

<p align="center">
  <img src="assets/preview.png" width="880" alt="Sample Template Preview" />
</p>

## License

This project is licensed under the [MIT License](LICENSE).
