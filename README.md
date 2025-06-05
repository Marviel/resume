# What?
An attempt to condense every nugget that is relevant to my professional life into one page of text.

```
¯\_(ツ)_/¯
```

# Building

## Resume Versions
This repository contains two versions of Luke Bechtel's resume:
- **`luke_bechtel_resume.tex`** - Detailed 5-page version with comprehensive experience details
- **`luke_bechtel_resume_concise.tex`** - Concise 2-page version optimized for quick screening

## Quick Start (Recommended)
Use the pre-built Docker image from Docker Hub:

### Detailed Version (5 pages)
```bash
docker run --rm -v "$PWD":/data lukebechtel/resume-builder pdflatex luke_bechtel_resume.tex
```

### Concise Version (2 pages)
```bash
docker run --rm -v "$PWD":/data lukebechtel/resume-builder pdflatex luke_bechtel_resume_concise.tex
```

## Building from Source
If you prefer to build the Docker image locally:
```bash
docker build -t resume-builder .

# Detailed version
docker run --rm -v "$PWD":/data resume-builder pdflatex luke_bechtel_resume.tex

# Concise version
docker run --rm -v "$PWD":/data resume-builder pdflatex luke_bechtel_resume_concise.tex
```

The Docker image includes:
- Debian Bookworm base
- LaTeX (minimal installation with required packages)
- Python 3 with Pygments for syntax highlighting
- Essential build tools (make, git, curl, jq)

## Output Files
After compilation, you'll have:
- `luke_bechtel_resume.pdf` - Detailed version
- `luke_bechtel_resume_concise.pdf` - Concise version

# Source 🙏
Forked from Sourabh Bajaj's excellent [resume template](https://github.com/sb2nov/resume).

### License
Format is MIT but all the data is owned by Luke Bechtel.
