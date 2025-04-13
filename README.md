# Calories Advisor App

Demo Video Link :- https://drive.google.com/file/d/1fJllPSrD-wqv_UF4VaTtQjrPqLvtUpyA/view?usp=sharing

A Streamlit-based web application that leverages **Google Gemini Vision AI** to analyze food images, estimate total calorie content, and provide a detailed nutritional breakdown of the items in the image.

---

## Features

-  Upload an image of food items (jpg, jpeg, png)
-  Uses Gemini Vision model to analyze the image and identify the food items
-  Calculates total calorie count and per-item breakdown
-  Evaluates whether the food is healthy or not
-  Gives a percentage breakdown of:
  - Carbohydrates
  - Fats
  - Fibers
  - Sugar
  - Other important dietary elements

---

##  How It Works

1. User uploads an image of food.
2. The image is processed and sent to **Google Gemini (Pro Vision model)** along with a detailed prompt.
3. Gemini responds with an analysis of:
   - List of food items
   - Calorie per item
   - Total calories
   - Nutritional breakdown and health suggestions
4. Results are displayed in a clean and simple Streamlit interface.

---

##  Tech Stack

| Technology | Usage |
|------------|--------|
| Python | Backend logic and integration |
| Streamlit | Web Interface |
| PIL (Pillow) | Image processing |
| Google Generative AI | Gemini Vision model |
| dotenv | Securely load API keys from `.env` file |

---

## Installation

1. **Clone the Repository**

2. **Create a Virtual Environment (Optional but Recommended)**

3. **Install Required Packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` File**
   Create a `.env` file in the root directory with your Google API key:
   ```
   GOOGLE_API_KEY=your_google_api_key
   ```

5. **Run the App**
   ```bash
   streamlit run app.py
   ```

---

##  Example Prompt Used

```
You are an expert in nutritionist where you need to see the food items from the image
and calculate the total calories, also provide the details of every food items with calories intake in below format:
1. Item 1 - number of calories
2. Item 2 - number of calories
---
Finally you can also mention whether the food is healthy or not and also mention the percentage
split of the ratio of carbohydrates, fats, fibers, sugar and other important things required in our diet.
```

---

##  Requirements

Create a `requirements.txt` file with the following:

```
streamlit
python-dotenv
google-generativeai
```

---

##  Project Structure

```
calories-advisor-app/
│
├── app.py                 # Main application logic
├── .env                  # API Key (not to be shared)
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
```

---

##  Future Improvements

- Add speech output using TTS (Text-to-Speech)
- Save and download reports
- Add multi-food image support and segmentation
- Improve prompt tuning for more accurate results
