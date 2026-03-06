# 💬 Chatbot template

A simple Streamlit app that shows how to build a chatbot using OpenAI's GPT-3.5.

[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://chatbot-template.streamlit.app/)

### How to run it on your own machine

1. Install the requirements

   ```
   $ pip install -r requirements.txt
   ```

2. Run the app

   ```
   $ streamlit run streamlit_app.py
   ```




public class Employee {
    private String essn;
    private double priceByHour;
    private int workingYear;
    private boolean isRetired;

    public Employee(String essn, int workingYear, double priceByHour, boolean isRetired) {
        this.essn = essn;
        this.workingYear = workingYear;
        this.priceByHour = priceByHour;
        this.isRetired = isRetired;
    }

    public int getWorkingYear() {
        return workingYear;
    }

    public boolean getIsRetired() {
        return isRetired;
    }

    public void setIsRetired(boolean isRetired) {
        this.isRetired = isRetired;
    }

    public void setWorkingYear(int workingYear) {
        this.workingYear = workingYear;
        Retiring();
    }

    public boolean deserveBonus() {
        if (workingYear >= 10 && isRetired == false) {
            return true;
        }
        return false;
    }

    public double calculateSalary(int workingHour, int workingDays) {
        return workingHour * workingDays * priceByHour;
    }

    public void Retiring() {
        if (workingYear >= 20) {
            isRetired = true;
        }
    }
}
