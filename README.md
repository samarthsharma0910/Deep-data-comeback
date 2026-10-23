# Sepsis Monitor: frontend

ICU early-sepsis dashboard for the Deep Data Hackathon 2026 (problem statement 1).

- `frontend/`: the React + TypeScript + Vite dashboard (Unit Census, Alert Queue, Patient Investigation, Assess Patient, Model Performance, Settings).
- `SUBMIT_ON_KAGGLE.md`: step-by-step guide to submit the notebook and `submission.csv` on Kaggle.

## Run the dashboard
```
cd frontend
npm install
npm run dev        # http://localhost:5173
npm run build      # type-check and production build
```

The app reads its data from `frontend/public/data/`:
- `dataset.json`: the patients shown on the census, alert queue and patient pages.
- `model.json` and `examples.json`: the trained model (gradient-boosted trees evaluated in the browser) and three real held-out records for the **Assess Patient** page, where anyone can enter a patient's values and get a prediction.

The Python training and export scripts live in the separate backend project and are not part of this repository.
This is a research demonstration trained on public PhysioNet/CinC 2019 data, not a medical device.
