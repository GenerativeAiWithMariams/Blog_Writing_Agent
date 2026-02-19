# 📝 LangGraph Blog Writer (Streamlit App)

This project is a **web-based AI blog writing assistant** built using **Streamlit** and **LangGraph**, designed to help users generate structured blog posts with optional images and evidence references.

---

## 📌 Project Overview

The app allows users to:

* Input a **topic** and an **as-of date**.
* Generate a **blog plan** (title, sections, tasks).
* Automatically retrieve **evidence / references** (if available).
* Produce **Markdown content** for the blog.
* View and download generated images.
* Download the final blog as **Markdown** or as a **bundle (Markdown + images)**.

The app maintains **past blog records** for quick access and review.

---

## ⚙️ Technologies Used

* Python 3
* Streamlit (for the web interface)
* Pandas (data handling)
* LangGraph (graph-based AI orchestration)
* JSON, Zipfile, Pathlib (file and directory handling)

Optional:

* Tavily / Groq API integration for evidence & AI generation

---

## 📁 Features

1. **Generate New Blog**

   * Input a topic and as-of date.
   * Generate structured blog content.

2. **Past Blogs**

   * Lists previously generated Markdown files.
   * Allows loading old blogs into the UI.

3. **Tabs in UI**

   * **Plan**: Displays blog title, audience, tone, tasks, and details.
   * **Evidence**: Shows retrieved references / sources.
   * **Markdown Preview**: Live preview of the blog content.
   * **Images**: Shows generated images and allows downloads.
   * **Logs**: Shows event logs for debugging or progress tracking.

4. **Download Options**

   * Markdown file of the blog.
   * Bundle containing Markdown + associated images.
   * Images ZIP file.

---

## ▶️ How to Run the Project

1. Install dependencies:

```bash
pip install streamlit pandas
# plus langgraph and any other project-specific dependencies
```

2. Run the Streamlit app:

```bash
streamlit run main.py
```

3. Enter a topic and click **Generate Blog**.

4. Navigate through tabs to see plan, evidence, preview, images, and logs.

---

## 🧩 Code Highlights

* `try_stream()` → Streams LangGraph app outputs progressively.

* `render_markdown_with_local_images(md)` → Safely renders Markdown with local and remote images.

* `bundle_zip()` → Prepares a downloadable ZIP of Markdown + images.

* `list_past_blogs()` → Fetches previous Markdown blogs from the current folder.

* **State Management** → Uses `st.session_state` to persist last generated blog.

* **Tabs Layout** → Provides structured UI for plan, evidence, preview, images, and logs.

---

## 🎯 Learning Outcomes

* Building a **Streamlit-based AI assistant**
* Integrating **LangGraph AI workflow** for structured blog generation
* Handling **Markdown, images, and file downloads**
* Maintaining **past outputs and session state**
* Displaying **progress and logs** in real-time

---

## 🚀 Future Improvements

* Integration with **Groq API** for AI-based text generation
* Automatic **image generation** for blog content
* Enhanced **evidence retrieval** using search APIs (like Tavily)
* Improved **UI with better progress visualization**
* Multi-topic / multi-user support

---

## 👩‍💻 Author

**MaryamS**
AI / Python / Streamlit / LangGraph Enthusiast

