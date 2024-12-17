## CMU Accessibility Lunch Seminar Website

This repository hosts the website for the **CMU Accessibility Lunch Seminar** series. The site is designed to be accessible, responsive, and easy to update.

**Live Site:** [https://cmubiglab.github.io/lunch](https://cmubiglab.github.io/lunch)

### About the Seminar

The CMU Accessibility Lunch Seminar is a series that explores the evolution and future directions of accessibility research and practice. Each week, we feature sessions on various aspects of accessible and assistive technologies, inviting speakers from academia, industry, and beyond.

### How to Update the Schedule

The weekly schedule is populated dynamically from a `schedule.json` file. To change the lineup, edit `schedule.json` and commit your changes.

**Steps to Update the Schedule:**

1. **Open `schedule.json`:**
   Located in the root of the repository, `schedule.json` is a JSON file containing an array of session entries. Each entry looks like this:
   ```json
   {
     "date": "1/27/2025",
     "speakers": [
       {
         "name": "Yi-Hao Peng",
         "link": "https://yihaopeng.tw"
       }
     ],
     "topic": "AI for Accessibility: Past, Present, and Future",
     "topicSlides": "https://example.com/slides"
   }
   ```

2. **Add or Modify Entries:**
   - **Date (required):** Provide the session date in a recognizable format (e.g., `MM/DD/YYYY`).
   - **Speakers (optional):** Add an array of speaker objects, each with `name` and optional `link`. If multiple speakers are used, they’ll be displayed inline, separated by spaces.
     ```json
     "speakers": [
       { "name": "Speaker Name", "link": "https://theirprofile.com" },
       { "name": "Another Speaker" }
     ]
     ```
     If no speakers are listed or if the `speaker` field is empty, it will show "TBA."
   
   - **Topic (optional):** Provide a short title or description for the week’s talk. If empty, it will display as "TBA."
   - **topicSlides (optional):** Add a link to slides or related materials. If provided, the entire topic text becomes clickable. If omitted, the topic will be plain text.
   
3. **Commit Your Changes:**
   Once you’ve edited and saved `schedule.json`, commit and push your changes to the `main` branch. The website, hosted on GitHub Pages, will automatically update within minutes.

### Running Locally

If you want to test changes before pushing:

1. **Clone the Repo:**
   ```bash
   git clone https://github.com/cmubiglab/lunch.git
   cd lunch
   ```

2. **Serve Locally:**
   You can use a simple HTTP server. For example, with Python:
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser.

### Contributing

- **Accessibility:** Contributions that improve web accessibility with assistive technologies are highly encouraged.  
- **New Features or Layout Changes:** Please open an issue to discuss your ideas before submitting a pull request.

### License

This repository is released under the [MIT License](LICENSE).
