# Shawn Lemuel Evora Dabi | Software Engineering Portfolio

Singapore · Singapore Institute of Technology, ICT (Software Engineering), Honours

I build full-stack applications and applied machine learning tools. My work includes turning Singapore job listings into explainable shortlists, testing whether video engagement can be predicted before publication, and processing images on the user's device.

## Selected engineering work

| Project | Problem and engineering decision | Explore |
| --- | --- | --- |
| **VizJobs** · TypeScript, React, Hono, Cloudflare D1 | The same vacancy can appear on several boards. The ingestion pipeline normalises listings, groups duplicates and retains the original sources. Career fit and employment eligibility have separate rules so a user can understand each finding. | Private deployment · architecture case study below |
| **Predicting Short-Form Video Performance** · Python, scikit-learn, Whisper | For my SIT capstone, I evaluated models on 60 external videos. Removing features derived from final engagement exposed how poorly the models predicted likes before publication. | [Code, experiment and results](https://github.com/shawnva-1996/short-form-video-performance) |
| **VizWealth** · Financial analytics | A fund distribution can be paid out or reinvested. The simulator models both paths and separates distributions from total return so the same gain is counted once. | [Explore VizWealth](https://vizwealth-sigma.vercel.app) |
| **VizDocs** · Browser-based office tools | A spreadsheet editor needs a formula engine, file import/export and a grid that agree on the value of a cell. VizDocs separates these responsibilities and stores documents on the device. | [Explore VizDocs](https://vizdocs.vercel.app) |
| **VizPresenter** · Browser presentation software | A church media team needs to operate a service while the audience sees the presentation. The browser-based presenter supports service cues and countdowns. | [Explore VizPresenter](https://vizpresenter.vercel.app) |
| **Sticker Studio** · Browser image processing | Removing every white pixel erases white lettering too. This tool estimates the background from the image corners, preserves the artwork and rebuilds its white outline. | [Download the standalone demo](https://github.com/shawnva-1996/Shawn-dabi-site-react/raw/refs/heads/main/public/sticker-studio.html) and open it in a browser. The illustrated sample runs locally. |

### Inside VizJobs

A source adapter captures a listing and its origin. Normalisation turns salary, title and location into comparable fields. Deduplication groups equivalent listings while retaining the source links. Two independent modules then answer “How well does this role fit?” and “Which employment requirements apply?” The React client gets both explanations through a Hono API. Deterministic tests exercise the rules with synthetic records. In the November 2026 research run, 5,260 input records became 5,094 distinct listings after exclusions and merges.
