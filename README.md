# Muhammad Ali Raza Tareen

**AI Engineer — agentic systems, retrieval, and applied ML**
Pakistan (UTC+5) · working remotely · [Email](mailto:tareenraza301@gmail.com) · [LinkedIn](https://linkedin.com/in/ali-raza-tareen)

I build LLM systems that hold up outside a notebook. Most of what makes them work isn't the
model — it's queue design, failure handling, deduplication, and deciding what the system does
when retrieval comes back with nothing useful.

**Recent production work**

- **Serverless transcription at scale** — cleared a 260,000-record backlog at ~65,000 calls/day on AWS SQS + Lambda + S3, with retry logic, dead-letter queues and rate limiting
- **RAG over 6,000+ hours of audio** — HDBSCAN clustering and cosine-similarity matching to strip duplicate and contradictory source material before indexing
- **Real-time voice agent** — live intake calls with branching qualification logic and human handoff

---

## Selected work

> Each repository ships a working application and a test suite, not a notebook.

### [sign-language-detection](https://github.com/aliraza908/sign-language-detection)
`MediaPipe` `TensorFlow` `OpenCV` `Flask`

Nine-class real-time gesture recognition from a webcam. MediaPipe returns a tight hand crop and a
CNN classifies it — so the network never has to learn to ignore backgrounds, which is why 1.7M
parameters are enough. Trained on **25,200 self-collected images**, captured with a tool that
shares its bounding-box function with the inference path so the two cannot silently drift apart.

### [academy-cfo-agent](https://github.com/aliraza908/academy-cfo-agent)
`LangGraph` `LangChain` `GPT-4o` `Streamlit`

Four-stage agent pipeline turning messy school finance spreadsheets into P&L statements,
fee-recovery risk scores, expense-leakage audits and ROI forecasts. Every LLM step has a
deterministic fallback, so the tool degrades to rule-based output rather than failing when no API
key is present.

### [brain-tumor-classification](https://github.com/aliraza908/brain-tumor-classification)
`TensorFlow` `Keras` `Flask`

Custom 920k-parameter CNN across four MRI classes — **89.7% accuracy on 1,311 held-out scans**.
The interesting part is the confusion matrix: the model resolves uncertainty toward "no tumour",
buying that class perfect recall at the cost of the worst precision in the set. For a screening
tool that's the wrong direction to err, and the README says so.

### [diabetes-prediction](https://github.com/aliraza908/diabetes-prediction)
`scikit-learn` `Flask` `pytest`

**0.837 ROC-AUC (±0.032 across 50 cross-validated fits).** Five features encode missing data as
physiologically impossible zeros — insulin in 48.7% of rows — so imputation is fitted inside each
CV fold rather than up front, and the decision threshold is chosen against a stated ≥75%
sensitivity target on out-of-fold predictions instead of left at 0.5.

### [Neural-Networks](https://github.com/aliraza908/Neural-Networks)
`NumPy`

Feedforward networks in pure NumPy — manual forward and backward passes, no framework. Exposed
through both an object-oriented (`fit`/`predict`/`evaluate`) and a functional API, with a
Zeros/Random/He initialisation comparison and unit tests checking gradients against reference
calculations.

---

## How I evaluate

Fitting preprocessing inside cross-validation folds so nothing leaks · choosing metrics that suit
imbalanced classes · tuning decision thresholds against a stated objective · reporting variance
across resamplings instead of a single flattering split · diagnosing *which* errors a model makes
rather than only how many.

Every metric above is reproducible from its repository, and each README states what its number
does *not* cover — including the sign language project, whose very high training-run accuracy came
from one continuous webcam session split at random, and which I therefore don't present as a
real-world estimate.

---

## Stack

| | |
|---|---|
| **Agents & retrieval** | LangGraph · LangChain · OpenAI API · Claude SDK · RAG · ChromaDB · Retell AI · Deepgram |
| **ML & vision** | TensorFlow · Keras · PyTorch · scikit-learn · OpenCV · MediaPipe · NumPy · pandas · HDBSCAN |
| **Services** | Python · FastAPI · Node.js · Flask · Django · Streamlit · WebSockets |
| **Infrastructure** | AWS (Lambda, SQS, S3) · Azure · DigitalOcean · Docker · Linux |

---

Available for remote roles — **tareenraza301@gmail.com**
