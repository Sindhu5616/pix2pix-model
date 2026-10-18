# Pix2Pix: Building Image Generation from Sketches

## Project Overview

This project uses **Pix2Pix**, a conditional Generative Adversarial Network (cGAN), to generate building images from sketch or outline images.

The goal is to provide a sketch as input and generate a building image as output. The notebook also displays the original uploaded image, its processed outline, and the AI-generated result side by side.

## How It Works

1. **Upload a sketch:** Choose a building sketch image from your computer.
2. **Preprocess the sketch:** Resize the image and extract its edges to create an outline image.
3. **Generate an image:** Pass the processed outline into the trained Pix2Pix generator.
4. **View the result:** Display the uploaded sketch, processed outline, and generated building image together.

## Model Architecture

- **Generator — U-Net:** Converts the input outline into a generated building image.
- **Discriminator — PatchGAN:** During training, evaluates local image patches to help the generator produce more realistic images.
- **Training approach:** Pix2Pix learns from paired outline and building-photo examples.

## Technologies Used

- Python
- PyTorch
- Google Colab
- NumPy
- Pillow (PIL)
- Matplotlib
- Pix2Pix (U-Net Generator and PatchGAN Discriminator)

## How to Run

1. Open the `.ipynb` notebook in Google Colab.
2. Connect to a runtime.
3. Make sure the trained generator checkpoint is available and load it using the notebook's model-loading code.
4. Run the notebook cells in order.
5. Upload a building sketch when prompted.
6. View the uploaded image, processed outline, and generated result.

> **Note:** The trained model checkpoint is stored separately from this notebook. Make sure the checkpoint path in the notebook points to your saved model file. Running the notebook in a fresh session may require reconnecting the runtime and loading the checkpoint again.

## Example Workflow

**Input:** Uploaded building sketch  
**Preprocessing:** Edge/outline extraction  
**Output:** AI-generated building image

The notebook visualizes all three stages side by side for demonstration.

## Project Files

- `README.md` — Project overview and instructions.
- `*.ipynb` — Google Colab/Jupyter notebook containing the project code and saved outputs, if included.
- Trained model checkpoint — Stored separately; see the note above.

## Limitations

- Results depend on the training data and how closely the uploaded sketch resembles the outlines used during training.
- Unfamiliar sketch styles may produce blurry or less realistic results.
- The generated image is an AI prediction and may not accurately represent a structurally valid building.

## Future Improvements

- Improve sketch preprocessing for different drawing styles.
- Test the model on a wider variety of building sketches.
- Improve and document the model's evaluation and results.

## Author

**Sindhu**

---

*This project was developed for learning and demonstration purposes.*
