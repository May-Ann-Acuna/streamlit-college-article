import streamlit as st
from streamlit_lottie import st_lottie
import requests

# Find more emojis here: https://www.webfx.com/tools/emoji-cheat-sheet/
st.set_page_config(page_title="My Webpage", page_icon=":tada:", layout="wide")

# Lottie animation function
def load_lottie_url(url: str):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()

# ---- HEADER SECTION ----
st.title("May-Ann B. Acuna 👩‍💻")
st.subheader("Computer Engineering Student at SNSU 🎓")

# Lottie animation for welcome message
lottie_url = "https://assets3.lottiefiles.com/packages/lf20_gjc6d5xg.json"  # Lottie animation URL (you can replace this with any animation URL)
lottie_animation = load_lottie_url(lottie_url)
if lottie_animation:
    st_lottie(lottie_animation, speed=1, width=600, height=400, key="welcome")

# Introduction
st.markdown("""
Hello! I'm **May-Ann B. Acuna**, a Computer Engineering student at SNSU. 🎓  
In this article, I'll talk about the college life experience and some challenges that students face. 🌱
""")

st.markdown("""
## 🌟 The College Journey

College is an exciting time, but it comes with its own challenges. As a student, you will learn not only about your courses 📚 but also about life 🌍. Here’s what I think are some of the most important parts of being a college student.

### 1. 📖 Academic Life

When you first start college, you might notice that the work is more difficult than high school. You will have to manage your time well because there will be assignments, exams, and projects to complete. Sometimes, this can be stressful 😰, but with good planning, you can do well!

### 2. 👯‍♀️ Making New Friends

College is also a great time to meet new people. You will make friends in class, clubs, and activities 🎉. It's important to find people who support you, especially during tough times. Making friends is one of the best parts of the college experience! 💕

### 3. 💵 Money Worries

A big challenge for many students is managing money 💸. College costs money, and sometimes it’s hard to balance work and studies. It’s helpful to look for scholarships or part-time jobs to support yourself. Managing your budget well will help reduce stress. 💡

### 4. 🧠 Mental Health Matters

College can be stressful. Many students feel pressure from schoolwork, social life, and finances 😓. It’s okay to feel anxious or worried. Talking to a counselor or taking care of your mental health is really important 🧘‍♀️. Make sure to take breaks, relax, and reach out when you need help. 💬

### 5. 🚀 Planning for the Future

In college, you will also start thinking about your career 🧑‍💼. It’s a good idea to get internships, join clubs, and attend events where you can learn about your future job. College is a time to build your skills and get ready for life after graduation 🎯.

## 🎓 Conclusion

Overall, being a college student is a time for learning, growing, and discovering who you are 🌱. It’s okay to face challenges, but remember that these challenges help you become stronger 💪. Stay positive, and enjoy your time at college!

Good luck to all the students out there! 🍀
""")

# Lottie animation for conclusion
lottie_url_end = "https://assets8.lottiefiles.com/packages/lf20_YZNGie.json"  # Lottie animation URL for conclusion
lottie_animation_end = load_lottie_url(lottie_url_end)
if lottie_animation_end:
    st_lottie(lottie_animation_end, speed=1, width=600, height=400, key="conclusion")

st.markdown("---")

st.markdown("""
**Thanks for reading!** 😊  
Feel free to connect with me for any questions or discussions. I wish all college students the best on their journey! 💫
""")

