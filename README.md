# Luis Machado Reis - Resume

![Markdown](https://img.shields.io/badge/Markdown-validated-blue.svg?style=for-the-badge&logo=markdown&logoColor=white)
![PDF](https://img.shields.io/badge/PDF-Generated-brightgreen?style=for-the-badge&logo=adobeacrobatreader&logoColor=red)
![GitHub Actions](https://github.com/luismr/resume/actions/workflows/convert-md-to-pdf.yml/badge.svg)

Welcome to my resume repository! This project contains my professional resume, and while contributions to improve **GitHub Actions automation** and repository workflows are welcome, **the content of the resume itself belongs to me**.

## 📄 Resume

You can view my resume in Markdown format [here](RESUME.md).

## 🔒 Ownership & Usage

This resume is **my personal document**, and its content should not be altered except for **GitHub Actions automation improvements**. Any changes modifying personal details, experience, or professional background will not be accepted.

## 🚀 Contributing

I encourage contributions that enhance the **automation and CI/CD workflows** for generating and maintaining this resume. Possible improvements include:
- Enhancing the **GitHub Actions pipeline** for automatic PDF generation.
- Automating formatting checks or linting for Markdown files.
- Improving **workflow efficiency** for CI/CD processes.
- Adding features to automatically publish updates to a GitHub Pages site or a dedicated branch.

### 📜 **GitHub Actions Workflow**  

This repository includes a **GitHub Actions workflow** that automatically converts `RESUME.md` into a **PDF** whenever changes are pushed.  

The workflow:  
✅ Uses **md-to-pdf** with **Puppeteer** for **accurate PDF rendering**.  
✅ Generates the file as `pdf/RESUME-YYYYMMDD.pdf`, based on the current date.  
✅ Automatically **commits the generated PDF** to the repository.  
✅ (Optional) **Sends an email with the latest resume PDF** if Gmail credentials are configured.  

👀 **Ensure Workflow Permissions**: Verify that your repository's settings allow workflows to have write permissions:

   - Navigate to your repository on GitHub.
   - Click on the "Settings" tab.
   - In the left sidebar, select "Actions" and then "General".
   - Under "Workflow permissions", ensure "Read and write permissions" is selected.
   - Click "Save" to apply the changes.

   This setting ensures that workflows have the necessary permissions to make changes to the repository.

You can find the workflow configuration in `.github/workflows/convert-md-to-pdf.yml`.  

### **📬 Email Notifications with Gmail**
Your **GitHub Actions workflow** includes an **optional feature** that automatically sends an email with your **latest resume PDF** whenever `RESUME.md` is updated. 📄📩  

#### **🔹 How It Works**
- The workflow **checks for Gmail credentials** before attempting to send an email.  
- If credentials exist, it will:
  ✅ Convert `RESUME.md` into `pdf/RESUME-YYYYMMDD.pdf`  
  ✅ Attach the **latest resume PDF** to an email  
  ✅ Send the email using **Gmail SMTP**  

- If credentials are **not configured**, the email step is **skipped** to prevent errors.

#### **🔹 How to Enable Email Sending**
1. **Generate a Gmail App Password**  
   - Go to [Google App Passwords](https://myaccount.google.com/apppasswords)  
   - Select **"Mail"** and generate a password  
   - Copy the **16-character password**  

2. **Set Up GitHub Secrets**  
   - Go to your **GitHub Repository → Settings → Secrets and Variables → Actions**  
   - Click **"New Repository Secret"**  
   - Add the following secrets:
     - **`GMAIL_USERNAME`** → Your Gmail (e.g., `your-email@gmail.com`)  
     - **`GMAIL_PASSWORD`** → Paste the **App Password**  

3. **Push an Update to `RESUME.md`**  
   - GitHub Actions will generate a **new PDF** and send it via email! 🚀  

#### **🔹 Disabling Email Notifications**
- If you **do not set** `GMAIL_USERNAME` and `GMAIL_PASSWORD`, the email step will be **skipped** automatically.

📌 This ensures **error-free execution**, whether or not you choose to enable email notifications.

### 🛠 How to Contribute

1. **Fork** this repository.
2. **Clone** your fork:
   ```sh
   git clone https://github.com/YOUR-USERNAME/resume.git
   ```
3. **Create a new branch** for your changes:
   ```sh
   git checkout -b feature-github-actions
   ```
4. **Make your edits and commit**:
   ```sh
   git commit -am "Enhance GitHub Actions workflow"
   ```
5. **Push to your fork**:
   ```sh
   git push origin feature-github-actions
   ```
6. **Submit a Pull Request (PR)** with a clear description of your improvements.

## 📜 License

This repository is publicly available, but **the resume content is owned by Luis Machado Reis**. Feel free to contribute automation scripts, but do not reuse or redistribute the resume's content without permission.

## 📬 Contact

If you have any questions or suggestions about **GitHub Actions or automation**, feel free to reach out:
- [LinkedIn](https://linkedin.com/in/luismachadoreis)
- [GitHub](https://github.com/luismr)
- [Website](https://luismachadoreis.dev.br)

---
Thanks for helping improve the automation of this project! 😊

