# Reporting Template in Markdown

## Setup

Needs Pandoc, Latex and Eisvogel Pandoc LaTeX PDF Template

```bash
sudo apt install pandoc texlive-full
sudo wget https://github.com/Wandmalfarbe/pandoc-latex-template/blob/master/eisvogel.tex -O /usr/share/pandoc/data/templates/eisvogel.tex
```

## Usage

Write your report in **markdown.**

### Automatic generate .pdf

```bash
./generate.sh (input.md) (output.pdf)
```

### Manual

Generate the report PDF from the markdown template:

```
pandoc input-markdown.md \
-o output-report.pdf \
--from markdown+yaml_metadata_block+raw_html \
--template eisvogel \
--table-of-contents \
--toc-depth 6 \
--number-sections \
--top-level-division=chapter \
--highlight-style breezedark
```

You can change the code syntax highlight theme
with ```[--highlight-style](https://pandoc.org/MANUAL.html#option--highlight-style)```

## Color sets

Well rendering color sets you can use in the template YAML frontmatter:

| titlepage-color | titlepage-text-color | titlepage-rule-color |
|:---------------:|:--------------------:|:--------------------:|
|```DC143C```(Crimson)|```FFFFFF```(White)|```FFFFFF```(White)|
|```00FF7F```(SpringGreen)|```006400```(DarkGreen)|```000000```(Black)|
|```1E90FF```(DodgeBlue)|```FFFAFA```(Snow)|```FFAFA```(Snow)|
|```483D8B```(DarkSlateBlue)|```FFFAFA```(Snow)|```FFFAFA```(Snow)|
|```FFD700```(Gold)|```000000```(Black)|```000000```(Black)|
|```FFEFD5```(PapayaWhip)|```000000```(Black)|```000000```(Black)|
|```FF8C00```(DarkOrange)|```000000```(Black)|```000000```(Black)|
|```FFEF96```(no name)|```50394C```(no name)|```50394C```(no name)|

## Mentions

[Markdown CheatSheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Credits

Report Templates:

- Official Offensive Security Template v3 (
  UNLICENSED): https://support.offensive-security.com/oscp-exam-guide/#suggested-documentation-templates
- whoisflynn improved template v3.2 (UNLICENSED): https://github.com/whoisflynn/OSCP-Exam-Report-Template
- Poseidon-ng Github (https://github.com/Poseidon-ng/VirtualHackingLabs_Report_Templates)