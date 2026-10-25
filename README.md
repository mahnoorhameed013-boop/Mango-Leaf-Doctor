# Mango Leaf Doctor

Final Year Project, BS Information Technology, The Islamia University of Bahawalpur
**Student:** Mah Noor (F23BINFT1E02048) | **Supervisor:** Mr. Abdul Karim Nawaz

**Status:** In development.

Mango Leaf Doctor is a web app where a grower uploads or captures a photo of a mango leaf and receives the
likely disease, a confidence score and basic treatment advice. Two transfer-learning models (MobileNetV2 and
EfficientNet-B0) are trained and compared, and the better one is used by the app.

| Crop | Classes |
| --- | --- |
| Mango | anthracnose, bacterial canker, cutting weevil, die back, gall midge, powdery mildew, sooty mould, healthy |

## Planned features

- Upload a JPG or PNG photo or take a photo with the phone camera
- Disease name, confidence percentage and top three results
- Warning when the model is not sure or the image is not a mango leaf
- Symptoms, treatment and prevention advice from an editable file
- "This result is wrong" button that saves the photo for review

## Dataset

- Public dataset: [MangoLeafBD](https://data.mendeley.com/datasets/hxsnvwty3r/1) (licence CC BY-NC, non-commercial use with attribution).
  It has about 4,000 images, but only about 1,800 show distinct leaves; the rest are zoomed or rotated copies.
  Images are split by original photo so that copies of one leaf never appear in both training and test sets.
- Own photos: mango leaf photos taken in local orchards, used only as a separate test set.
- The dataset itself is not stored in this repository.

## Project structure

| Path | Purpose |
| --- | --- |
| `src/` | Data preparation, training, evaluation, prediction |
| `app/` | Streamlit web app and advice text |
| `notebooks/` | Training on Google Colab |
| `tests/` | Automated tests |
| `docs/` | Proposal, SRS and SDD |

## Technologies

Python 3, PyTorch and torchvision, scikit-learn, pandas, NumPy, matplotlib, Pillow, Streamlit,
pytest, Google Colab, Git and GitHub.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Results

To be filled in after training on real data.

| Model | Public test accuracy | Orchard-photo accuracy |
| --- | --- | --- |
| MobileNetV2 | | |
| EfficientNet-B0 | | |

## Limitations

- Decision support only; it does not replace an agriculture expert.
- Treatment advice must be checked by an agriculture expert.
- Accuracy on orchard photos is expected to be lower than on public images.

## Documents

Project documents are in the `docs/` folder: proposal, SRS and SDD.
