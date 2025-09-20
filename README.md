# Resume Analyzer - AI-Powered Job Matching

A professional web application that analyzes resumes against job requirements using AI-powered keyword matching and provides improvement suggestions.

## Features

- **Resume Upload**: Support for PDF, DOCX, and TXT files
- **AI Analysis**: Intelligent text extraction and keyword matching
- **Job Matching**: Compare resume against target job descriptions
- **Scoring System**: Get a compatibility score (0-100%)
- **Skill Analysis**: See matched and missing skills
- **Improvement Suggestions**: Get actionable advice to improve your resume
- **Professional UI**: Modern, responsive design with Tailwind CSS

## Technology Stack

- **Backend**: Django 4.2.7
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **File Processing**: PyPDF2, python-docx
- **Database**: SQLite (development)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd resume
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Populate sample data**
   ```bash
   python manage.py populate_job_roles
   ```

6. **Create superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Open your browser**
   Navigate to `http://127.0.0.1:8000`

## Usage

1. **Upload Resume**: Drag and drop or select your resume file (PDF, DOCX, or TXT)
2. **Enter Job Details**: Provide the target job title and paste the job description
3. **Analyze**: Click "Analyze Resume" to get instant feedback
4. **Review Results**: Check your compatibility score, matched/missing skills, and suggestions
5. **Improve**: Use the suggestions to enhance your resume

## File Structure

```
resume/
├── manage.py
├── requirements.txt
├── resume_analyzer/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── analyzer/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── utils.py
│   └── management/
│       └── commands/
│           └── populate_job_roles.py
├── templates/
│   └── analyzer/
│       └── home.html
├── static/
├── media/
└── README.md
```

## API Endpoints

- `GET /` - Home page with upload form
- `POST /analyze/` - Analyze uploaded resume
- `GET /api/job-roles/` - Get available job roles

## Customization

### Adding New Job Roles
1. Go to Django admin: `http://127.0.0.1:8000/admin`
2. Navigate to "Job roles" section
3. Add new roles with relevant keywords

### Modifying Analysis Logic
Edit `analyzer/utils.py` to customize:
- Skill keyword lists
- Scoring algorithm
- Suggestion generation
- Text extraction methods

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For issues and questions, please open an issue on GitHub.
"# Resume-Analyser-using-Cursor-AI" 
