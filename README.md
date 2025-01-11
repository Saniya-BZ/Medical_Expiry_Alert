# Learning Style Assessment API

## Available Endpoints

### 1. MCQ-Based Learning Style Assessment
Endpoint URL: /mcq/
Input Format (JSON):
{
  "responses": [
    "Strongly Agree",
    "Agree",
    "Neutral",
    "Disagree",
    "Strongly Disagree",
    "Agree",
    "Strongly Agree",
    "Neutral",
    "Disagree",
    "Strongly Agree"
  ]
}

Output Format (JSON):
{
  "scores": {
    "Visual": 25.0,
    "Story-based": 15.0,
    "Application-based": 30.0,
    "Creativity-based": 10.0,
    "Analytical": 20.0
  },
  "dominant_style": "Application-based"
}
scores: A dictionary containing percentage scores for each learning style.
dominant_style: The learning style with the highest score.

### 2. Written Response Learning Style Analysis

Endpoint URL: /written/
Input Format (JSON):
{
  "response": "I enjoy solving puzzles and breaking problems into smaller parts to understand them."
}

Output Format (JSON):
{
  "scores": {
    "Visual Learner": 10.5,
    "Story-Based Learner": 5.0,
    "Application-Based Learner": 20.3,
    "Creativity-Based Learner": 15.2,
    "Analytical Learner": 49.0
  },
  "dominant_style": "Analytical Learner"
}
scores: A dictionary containing similarity scores for each learning style.
dominant_style: The learning style with the highest score.

Start the server using:
uvicorn main:app --reload

Access the interactive API documentation at:

http://127.0.0.1:8000/docs
