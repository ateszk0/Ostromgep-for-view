# Ostromgep Library: Detailed User Guide

Welcome to **Ostromgép**! This application was created to help you precisely log your workouts, track your progress, and consciously apply Progressive Overload.

---

## 1. Dashboard

The **Dashboard** is the main screen where you get a quick overview of your current status and your next tasks.

- **Next Mission**: The app suggests your next workout based on your saved routines. Click the **"Start Mission"** button to begin immediately.
- **Weekly Battle Log**: You see the days from Monday to Sunday. Small colored circles indicate which days you have already worked out this week.
- **Ready to Siege (Muscle Recovery)**: This heatmap shows the fatigue level of individual muscle groups.
  - **Green**: Recovered, ready for load.
  - **Yellow**: Mild fatigue, noticeable exertion.
  - **Red**: Strong fatigue, resting the specific muscle group is recommended.
- **Wall of Fame**: Here you can scroll through your latest **Personal Records**.
- **Quick Metrics**: Click the input field to record your daily body weight. Save it with the checkmark button next to it. The graph below shows the trend of your last 7 measurements.

---

## 2. Starting a Workout and Managing Routines

On the **Workout** tab (bottom navigation), you can choose how you want to exercise:

- **Start Empty Workout**: If you don't have a fixed plan and want to assemble exercises on the spot.
- **My Routines**: Here you can find the templates you have created. Click the **"Start Routine"** button on its card to start.
- **QR Code Import/Export**: Use the **QR icon** above the routine list to import workout plans shared by others. You can share your own routines by selecting **Share via QR** from the three-dot (...) menu on their cards.
- **Manage Folders**: You can organize your routines by clicking the **folder icon** in the top right corner.
  - **Create Folder**: Use the "New Folder" button to create a folder, name it, and select which routines belong to it.
  - **Active Folder**: If you select a folder from the list, only the routines belonging to it will appear in a loop on the Home screen.
- **New Routine**: You can create a new, savable workout plan (**Routine Editor**).
- **Explore Routines**: You can choose from pre-assembled workout plans (e.g., Push-Pull-Legs, Full body), which you can save for yourself using the **"Add to my routines"** button. These are absolutely not perfect routines, just temporary placeholders to fill space.

---

## 3. Active Workout Process

When you start a workout, the following tools are available for logging:

### Workout Stats Header
At the top of the screen, you constantly see the most important data: **Duration**, **Volume**, and **Sets**.

### Exercise Block Interactions
- **Thumbnail Image**: Click the small image next to the exercise. If a video is available, playback will start; otherwise, the image will be enlarged.
- **Notes**: You can write notes directly under the exercise name.
- **Rest Timer**: Click the time next to the small stopwatch (e.g., "90s") in the header to modify it.
- **More Menu (...)**: Here you can access the **Move Up/Down**, **Edit**, **Superset** (Create Superset), and **Delete** functions.

### Sets Table - Operation
- **Set Number (1, 2, 3...)**: **CLICK THE NUMBER** to change it to a **Warmup set**. The row color will change to yellow.
- **Previous**: Here you see the data from your last workout.
- **KG / Reps**: Click into the fields to enter data.
- **RPE (Rate of Perceived Exertion)**: Click the dash in the RPE column and select from the popup list (on a given scale).
- **Complete Toggle**: Click the gray square at the end of the row to finish the set. This also starts the automatic rest timer.
- **Remove Set**: **SWIPE LEFT** on the entire set to reveal the red delete icon.

---

## 4. Managing Exercises

On the **Profile** tab, you can access the **Exercises** library to manage exercises:

- **Create Exercise**: You can add your own exercise using the **"Create"** button in the top right. You can name it, set its default **Rep Range**, upload an image for it, and select the affected **Muscle Groups** and required **Equipment**.
- **Edit Exercise**: Click any exercise in the list or in the in-workout menu to modify it.
  - For custom exercises, you can edit all data (name, image, muscles).
  - For default exercises, for safety reasons, you can only modify the rep range; their image is fixed.

---

## 5. Statistics (In Progress)

The **Statistics** screen is currently under development, but it already shows a lot of useful data:

- **Weekly Heatmap**: A 7-day view at the top of the screen shows on which days you worked out.
- **Body Visualization**: Two figures (**Front** and **Back**) graphically show which muscles you worked this week. (Beta)
- **Advanced Stats**: By clicking the buttons, you get more detailed analyses (e.g., **Set Count by Muscle**, **Monthly Report**).

---

## 6. Profile and History

On the **Profile** tab, you can track your long-term progress:

- **Recent Workouts Volume Chart**: A bar chart shows the total volume of your recent workouts, so you can see if your load is increasing over time.
- **Workouts Button**: Clicking this takes you to your full workout history (**Workout Log**), where you can look back at the details of all your previous workouts. New feature: Click on a past workout and use the **AI Evaluation** button to request a detailed analysis of your performance retroactively (available in multiple languages!).
- **Calendar Button**: You can browse the past in a calendar view. Days marked with a dot indicate a workout.
- **Recent Workouts List**: At the bottom of the screen, you see cards for your last 5 workouts. Click any for details, or use the **Copy workout** or **Save as routine** functions to reuse them.
- **Settings**: Accessible via the gear icon in the top right corner of your profile. Here you can modify your name, profile picture, the app's language, and the theme color (**Red, Yellow, Green, Blue, Purple**). On this screen, you can also configure the **Machine Weight Steps** value, which helps in providing more accurate Progressive Overload suggestions during workouts.

---

## 7. AI Workout Generator (Gemini 3.0 Flash)

At the top of the **Explore Routines** screen is the **AI Workout Generator** card, which you can use to create completely unique, personalized workout plans using state-of-the-art artificial intelligence.

- **API Key**: To use the generator, you will need your own **Gemini API key**.
    1. **Obtaining a Key**: Visit [Google AI Studio](https://aistudio.google.com/), sign in with your Google account, and click the **'Get API key'** button to create a new key.
    2. **Setup in the app**: Go to the **Profile** tab, click the **Settings** (gear) icon in the top right, and scroll down to the **AI (Gemini API Key)** section. Paste the key and save it. The app stores this securely and encrypted (**EncryptedSharedPreferences**) on your device.
- **Training days per week**: Use the slider to set how many days you plan to work out in a week (1-7 days). The AI will automatically suggest an optimal split (e.g., PPL, Upper/Lower, Full Body, Arnold Split) based on the number of days.
- **Additional preferences**: This is an optional field where you can provide specific requests to the AI. For example: *"I have a shoulder injury, let's focus more on legs and back"*, or *"I want more isolation exercises for arms"*.
- **Generate Workout Plan**: After pressing the button, the AI will assemble your plan from the elements of the factory exercise library (**default_exercises.json**) and automatically save the routines for each day separately in your **My Routines** list. The AI generation is now bilingual, so it writes notes according to the app's set language.

---

## 8. Auto Updater & Maintenance

The application features a built-in update checker. Upon startup, it securely checks the app's official GitHub page (**ateszk0/Ostromgep-workout-app**) in the background. If it finds a new release:
- It immediately notifies you of the new version in a popup dialog.
- Clicking the **Update** button will redirect your browser to the corresponding GitHub page, where you can download the new `.apk` file.
- The feature is designed to never interrupt your workout: if there is no internet, it runs silently in the background.

---

*Have a great workout and successful progress with Ostromgép!*
