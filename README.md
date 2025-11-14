#1.Repositoty Structure
ASSIGNMENT2
│
├── Metadata
│   ├── results.json
│   └── vocab.json
│
├── Plots
│   ├── bestfit_loss.png
│   ├── overfit_loss.png
│   └── underfit_loss.png
│
├── Neural.ipynb   # Main Colab notebook (complete implementation)
└── README.md       # Project documentation

#2. How to Run Training
Step 1 — Open the notebook
    Neural.ipynb
step2-Mount Google Drive
 from google.colab import drive
 drive.mount('/content/drive')

 step 3 — Prepare Dataset
  Pride and Prejudice – Jane Austen (Project Gutenberg)

Step 4 — Train Models
 • Underfit Model
   train_model(model_under, train_dl, val_dl, ...)

• Overfit Model
   train_model(model_over, small_train_dl, val_dl, ...)

•Best-Fit Model
  train_model(model_best, train_dl_small, val_dl, ...)

Each model automatically saves a checkpoint to Drive:
model_under.pth
model_over.pth
model_best.pth

#3.Run Inference
def generate_text(model, start_tokens, gen_len=50):
    ...

#4.Visualizations
plots/underfit_loss.png
plots/overfit_loss.png
plots/bestfit_loss.png

#5.Evaluation – Perplexity

val_ppl = exp(validation_loss)

#6.Trained Model Links (Google Drive)
model_under.pth   link:https://drive.google.com/file/d/19snCffH56jrJEK3QjZEiXWjb3sft5Pzp/view?usp=sharing

model_over.pth    link:https://drive.google.com/file/d/1cks9PE-fYJChG0gGetIENWFIcS5lPEml/view?usp=sharing

model_best.pth    link:https://drive.google.com/file/d/1wPwnGYK4jD633vsvVuIfvKI2Zg644h00/view?usp=sharing

#GOOGLE DRIVE LINK:https://drive.google.com/drive/folders/180Usaq8NNHffYEbyTDPFcDHZJbe9hBJt?usp=sharing

#GITHUB LINK:https://github.com/pranaypadole22/Assignment-2-Neural-Language-Model-Training-PyTorch-
