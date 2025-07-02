### **Project Blueprint: AI-Powered Code Reviewer**

- **Track:** Blackbox.ai

#### **1. Project Requirements (The MVP Scope)**

- **Core Concept & Value Proposition:** An AI-powered code reviewer that uses Blackbox.ai’s API to provide real-time feedback on GitHub pull requests, helping developers improve code quality by catching bugs and suggesting optimizations.
- **Key Features (The Absolute MVP):**
  - As a user, I can connect my GitHub repository to the app so that it monitors new pull requests.
  - As a user, I can receive automated code review comments on a pull request, powered by Blackbox.ai’s API, highlighting potential bugs or improvements.
  - As a user, I can view a simple web dashboard that summarizes the AI’s feedback for my pull request.
  - As a user, I can trigger a manual code review by submitting a code snippet directly to the app.
- **Stretch Goals (If Time Permits):**
  - Add support for multiple programming languages (beyond the initial focus, e.g., Python or JavaScript).
  - Implement a feature to generate automated test cases for the reviewed code using Blackbox.ai’s API.
  - Add a browser extension to trigger reviews directly from the GitHub UI.
- **Tech Stack & Dependencies:**
  - **Frontend:** React with Tailwind CSS for rapid UI development and a clean, responsive dashboard.
  - **Backend:** Node.js with Express for a lightweight, API-driven backend to handle GitHub and Blackbox.ai integrations.
  - **Database:** SQLite for simplicity, storing basic metadata like repository connections and review history (no complex schema needed for MVP).
  - **Sponsor's Tech:** Blackbox.ai API for code review and suggestion generation, GitHub API for pull request monitoring and commenting.
- **Data Requirements:**
  - **User-Provided Data:** GitHub repository details (via OAuth token) and code snippets from pull requests.
  - **Mock Data:** Use sample code snippets (e.g., Python or JavaScript functions) to test Blackbox.ai’s API during development.
  - **No Public Dataset Needed:** The app relies on real-time pull request data from GitHub and Blackbox.ai’s API responses.

#### **2. The 3-Day Hackathon Battle Plan**

- **Day 1: Foundation & Core Logic (First 24 hours)**

  - **Focus:** Set up the development environment, integrate Blackbox.ai and GitHub APIs, and build a functional backend for code review.

  - **Key Milestones:**

    - [ ] Project repo created on GitHub & team members invited with collaborator access.

    - [ ] Development environment set up (Node.js, React, SQLite, and necessary npm packages installed locally).

    - [ ] “Hello World” test with Blackbox.ai API: Send a sample code snippet and receive a review response.

    - [ ] Backend API endpoints created:

      - POST `/connect-repo` to authenticate GitHub repo via OAuth.
      - POST `/review-code` to send code to Blackbox.ai API and retrieve feedback.

    - [ ] Core logic functional: Backend can process a code snippet, call Blackbox.ai API, and return review comments.

- **Day 2: Build, Integrate & Test (Next 24 hours)**

  - **Focus:** Build the frontend dashboard, integrate it with the backend, and ensure end-to-end functionality for the core code review feature.

  - **Key Milestones:**

    - [ ] Basic UI/UX wireframes sketched (use Figma or pen-and-paper for a simple dashboard layout).

    - [ ] Frontend React components built:

      - Repository connection form.
      - Dashboard displaying pull request reviews.
      - Manual code snippet submission form.

    - [ ] Frontend makes successful API calls to backend for repo connection and code review.

    - [ ] End-to-end flow working: User connects a repo, submits a pull request or snippet, and sees AI-generated feedback on the dashboard.

    - [ ] Deploy to a staging environment (e.g., Vercel for frontend, Heroku or Vultr for backend).

- **Day 3: Polish, Pitch & Deploy (Final 24 hours)**

  - **Focus:** Polish the UI, fix critical bugs, and prepare a compelling demo and pitch. Stop adding new features by midday to focus on presentation.

  - **Key Milestones:**

    - [ ] Code freeze on new features by 12 PM. Focus on bug fixes (e.g., API error handling) and UI polish with Tailwind CSS.

    - [ ] Finalize visual design: Ensure the dashboard is clean, intuitive, and visually appealing (e.g., consistent fonts, colors, and spacing).

    - [ ] Create presentation slides: Include problem statement, demo walkthrough, Blackbox.ai integration, and team contributions.

    - [ ] Write a 3-minute demo script: Show connecting a repo, submitting a pull request, and displaying AI feedback.

    - [ ] Practice the pitch 3-5 times with the team to ensure smooth delivery.

    - [ ] Record a demo video (if required) showcasing the end-to-end flow.

    - [ ] Submit the project to the hackathon platform by the deadline.

- **Final Coach’s Advice:** Avoid over-relying on Blackbox.ai’s generated code for your own project without thorough testing. The API may produce suboptimal code that requires debugging, which can eat into your 3-day timeline. Always run the AI-generated reviews with sample inputs and validate outputs early (on Day 1) to catch issues before integrating with the frontend.