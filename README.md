Muhammad Ali Raza Tareen

AI Engineer — agentic systems, RAG, and LLM applications. Pakistan (UTC+5) · working remotely · open to remote roles

I build LLM systems that run in production rather than in notebooks: multi-agent orchestration with LangGraph, retrieval pipelines over large unstructured corpora, and real-time voice agents. Recent professional work includes a serverless AWS transcription pipeline that cleared a 260,000-record backlog, a RAG knowledge base built from 6,000+ hours of long-form audio, and a production voice agent handling live intake calls.

Before that I worked on classical ML and computer vision — which is where most of the code below comes from.

Selected work

academy-cfo-agent — LangGraph · GPT-4o · Streamlit A four-stage agent pipeline that turns messy school finance spreadsheets into P&L statements, fee-recovery risk scores, expense-leakage audits and ROI forecasts. Hybrid GPT-4o + deterministic fallback architecture, so the tool still works with no API key present.

brain-tumor-classification — TensorFlow · Keras · Flask A custom 920k-parameter CNN classifying brain MRI scans into four categories, reaching 89.7% accuracy on 1,311 held-out scans. The README includes the per-class error analysis — the model resolves uncertainty toward "no tumour", which is the wrong direction to err for screening — not just the headline number.

diabetes-prediction — scikit-learn · Flask · pytest Diabetes risk classifier at 0.837 ROC-AUC (±0.032 across 50 cross-validated fits). Recovers missing values encoded as zeros in up to 48.7% of a feature, and fits imputation inside each CV fold so no statistic leaks from the test set. Decision threshold tuned to a stated ≥75% sensitivity target on out-of-fold predictions.

sign-language-detection — MediaPipe · TensorFlow · OpenCV · Flask Real-time recognition of nine hand signs from a webcam. MediaPipe localises the hand and returns a tight crop; a CNN classifies the gesture — which is why 1.7M parameters suffice, since the network never has to learn to ignore the background. Trained on a self-collected 25,200-image dataset captured with a labelling tool built for the purpose.

Neural-Networks — NumPy Deep feedforward networks implemented in pure NumPy — manual forward and backward propagation, Sigmoid/ReLU/Tanh, loss computation, no frameworks. Exposed through both an object-oriented (fit/predict/evaluate) and a functional API, with a comparison of Zeros, Random and He initialisation and a test suite checking gradients against reference calculations.

A note on the numbers

Every metric above is reproducible from the repository it sits in, and each README states what its number does not cover.

The sign language project is the clearest example. It reports a very high training-run accuracy that I deliberately don't present as a real-world estimate: the frames came from one continuous webcam session split uniformly at random, so near-duplicate frames land on both sides of the split. The README explains this rather than quietly quoting the number.

The thing I actually care about across these projects is evaluation discipline — fitting preprocessing inside cross-validation folds, choosing metrics that suit imbalanced classes, tuning decision thresholds against a stated objective, reporting variance across resamplings instead of a single flattering split, and diagnosing which errors a model makes rather than only how many.

These are portfolio projects. None of them is a medical device or a clinically validated system, and each repository says so.

Stack
	
LLM / Agents	LangGraph · LangChain · OpenAI API (GPT-4o, o1-mini, Whisper) · Claude SDK · RAG · ChromaDB · Retell AI · Deepgram
ML / CV	TensorFlow · Keras · PyTorch · scikit-learn · OpenCV · MediaPipe · NumPy · pandas · HDBSCAN
Backend	Python · FastAPI · Node.js · Flask · Django · Streamlit · WebSockets
Cloud & Infra	AWS (Lambda, SQS, S3) · Azure · DigitalOcean · Docker · Linux
Automation	n8n · Meta Graph API · WhatsApp Business API · Selenium · Playwright

📫 tareenraza301@gmail.com · LinkedIn
