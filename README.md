# My Resume

This repository contains my resume in JSON format, built using [JSON Resume](https://jsonresume.org/).  
It uses `resume-cli` to generate different formats, and a GitHub Actions pipeline to automate deployment to a github pages site - which can be found at [https://magicmatteo.github.io/resume](https://magicmatteo.github.io/resume).

## Installation

To set up the project, follow these steps:

1. Install `resume-cli` globally:
   ```sh
   npm install -g resume-cli
   ```
2. Install dependencies:
   ```sh
   npm install
   ```

## Usage

### Preview the Resume
To preview the resume in a browser, run:
```sh
resume serve --theme=stackoverflow
```
This will start a local server where you can view the resume in real time.

### Export as PDF
To generate a PDF version of the resume:
```sh
resume export resume.pdf --theme=stackoverflow
```

### Export as HTML
To generate an HTML file:
```sh
resume export index.html --theme=stackoverflow
```

## GitHub Actions Workflow

This repository includes a **GitHub Actions pipeline** to automate deployment.

### Deployment to GitHub Pages  
- **Trigger:** Pushing to the `main` branch.  
- **What happens:** The pipeline builds the resume and publishes it to **GitHub Pages**.  
- **Where to find it:** The site will be available at:  
  ```
  https://magicmatteo.github.io/resume/
  ```

### PDF Release on Tag Push  
- **Trigger:** Pushing a **tag** (e.g., `v1.0.0`).  
- **What happens:** The pipeline generates a **PDF version of the resume** and creates a GitHub Release containing the PDF.  
- **How to trigger it:**
  ```sh
  git tag v1.0.0
  git push origin v1.0.0
  ```
- **Where to find it:**  
  Go to the **Releases** section of the repository on GitHub.

## License

This project is open-source and available under the [MIT License](LICENSE).


