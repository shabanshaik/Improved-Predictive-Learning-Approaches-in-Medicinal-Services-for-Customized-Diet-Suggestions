# Vitamin Deficiency Prediction & Diet Recommendation System

A machine learning-based web application that predicts vitamin deficiencies (A, B, C, D, E, K) based on user input values and recommends appropriate food items to address nutritional gaps.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.x-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Published](https://img.shields.io/badge/Published-IJIEMR%202022-orange.svg)

## 📋 Overview

In today's fast-paced world, many people suffer from vitamin deficiencies due to imbalanced food consumption. According to WHO:
- ~9% of heart attack deaths are caused by insufficient/imbalanced food consumption
- ~11% of ischemic heart disease deaths worldwide
- ~0.25 billion teenagers suffer from Vitamin A to K deficiencies
- ~0.2 billion people suffer from Iron deficiency (Anemia)

This system automates the process of:
1. Detecting vitamin deficiencies based on input values
2. Recommending appropriate foods to address deficiencies

## 🏗️ System Architecture

```
┌─────────────┐     ┌─────────────┐     ┌─────────────────────┐
│   User      │────▶│   Flask     │────▶│  ML Models          │
│   Input     │     │   Web App   │     │  (KNN, RF, DT, LR)  │
└─────────────┘     └─────────────┘     └─────────────────────┘
                           │                      │
                           ▼                      ▼
                    ┌─────────────┐     ┌─────────────────────┐
                    │   MySQL     │     │  Prediction &       │
                    │   Database  │     │  Recommendation     │
                    └─────────────┘     └─────────────────────┘
```

## 🔬 Machine Learning Algorithms Used

| Algorithm | Purpose | Accuracy |
|-----------|---------|----------|
| K-Nearest Neighbors (KNN) | Classification | Varies by dataset |
| Decision Tree | Classification | Varies by dataset |
| Random Forest | Classification (Best performing) | Highest |
| Logistic Regression | Classification | Varies by dataset |
| Voting Classifier | Ensemble method | Combined |

The system uses an **ensemble approach** combining multiple algorithms and selects the best-performing model for predictions.

## 🛠️ Tech Stack

- **Backend:** Python 3.x, Flask
- **Frontend:** HTML5, CSS3, JavaScript
- **Database:** MySQL (SQLyog)
- **ML Libraries:** scikit-learn, pandas, numpy
- **Development Environment:** Anaconda, Jupyter Notebook

## 📁 Project Structure

```
vitamin-deficiency-predictor/
├── app.py                    # Main Flask application
├── templates/
│   ├── index.html           # Home page
│   ├── login.html           # Login page
│   ├── register.html        # Registration page
│   ├── vitaminform.html     # Vitamin input form
│   └── viewimage.html       # Results display
├── static/
│   ├── css/
│   └── images/
├── datasets/
│   ├── VITAMINDATASET.xlsx  # Vitamin deficiency dataset
│   └── recommend.xlsx       # Food recommendation dataset
├── models/                   # Trained ML models (pickle files)
├── requirements.txt
└── README.md
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.x
- Anaconda (recommended)
- MySQL Server

### Step-by-step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/vitamin-deficiency-predictor.git
   cd vitamin-deficiency-predictor
   ```

2. **Create and activate virtual environment** (optional but recommended)
   ```bash
   conda create -n vitamin python=3.8
   conda activate vitamin
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**
   - Create a MySQL database
   - Update database credentials in `app.py`

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Access the application**
   - Open browser and navigate to: `http://127.0.0.1:5000/`

## 📊 Datasets

### Vitamin Dataset
Contains vitamin values (A, B, C, D, E, K) with:
- Min and max reference values
- Deficiency indicators (0 = Normal, 1 = Deficient)

### Food Recommendation Dataset
Contains various combinations of vitamin deficiencies mapped to recommended foods:
- Fruits, cereals, vegetables
- Millets, dry fruits, cheese
- Curd, milk, meat

## 💻 Usage

1. **Register/Login** - Create an account or login with existing credentials
2. **Enter Vitamin Values** - Input your vitamin A, B, C, D, E, K test results
3. **Submit** - Click submit to get predictions
4. **View Results** - See which vitamins are deficient and get food recommendations

## 📸 Screenshots

### Login Page
![Login](screenshots/login.png)

### Vitamin Input Form
![Form](screenshots/vitamin-form.png)

### Results Page
![Results](screenshots/results.png)

## 📚 Publication

This project was published in:

**International Journal for Innovative Engineering and Management Research (IJIEMR)**
- **Volume:** 11, Issue 04
- **Date:** April 2022
- **Pages:** 131-136
- **DOI:** [10.48047/IJIEMR/V11/I04/21](https://doi.org/10.48047/IJIEMR/V11/I04/21)
- **ISSN:** 2456-5083

## 👥 Team

| Name | Role | Contact |
|------|------|---------|
| **Shaik Shabana** | Developer | [LinkedIn](https://linkedin.com/in/yourprofile) |
| V.S.N.S. Gayathri | Developer | |
| R. Lakshmi Naveen Kumar | Developer | |
| V. Rahul Nadh | Developer | |

**Project Guide:** Dr. S. Narayana, Professor & Mentor (AS&A), Department of CSE

**Institution:** Seshadri Rao Gudlavalleru Engineering College (JNTUK), Andhra Pradesh, India

## 🔮 Future Enhancements

- [ ] Add more nutrients (Iron, Calcium, Iodine, etc.)
- [ ] Implement user dietary history tracking
- [ ] Add mobile responsive design
- [ ] Include recipe suggestions
- [ ] Deploy on cloud (AWS/Heroku/Railway)
- [ ] Add REST API endpoints
- [ ] Implement user authentication with JWT
- [ ] Add data visualization dashboard

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Dr. S. Narayana for guidance and supervision
- Department of Computer Science and Engineering, SRGEC
- IJIEMR for publication

## 📞 Contact

For any queries or suggestions:
- **Email:** shabanashabbughf@gmail.com
- **LinkedIn:** [Your LinkedIn Profile]

---

⭐ **If you found this project helpful, please give it a star!**
