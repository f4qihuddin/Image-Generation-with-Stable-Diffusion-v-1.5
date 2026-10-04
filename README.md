# Image Generation with Stable Diffusion v 1.5

## About
Developing an AI web application for generating images based on prompts. The app features include text to image and also image to image (inpainting & outpainting). The model parameters such as CFG, steps, and more can be freely adjusted to enhance image generation

## How to run the web app?
The streamlit-app.ipynb notebook has some logic functions for generating images and also UI code in python (using Streamlit). You can tweak the code or just run it directly. Here's how:

1. Open streamlit-app.ipynb
2. Change kernel to T4 GPU in Google Colab (alternatively you can also use Kaggle Notebook)
3. Set auth_token with your NGROK auth token to host the app
4. Click Run All
5. Scroll below until you find a link to the streamlit app and click to open

## App Features
### 1. Stable Diffusion 1.5 Parameter Settings
In the sidebar, you'll find settings to adjust Stable Diffusion parameters. Here's the detail:
- **Quality Steps**: Control the number of iteration to generate images, the higher, the more likely the image generated to follow your prompt and add more details
- **Creativity (CFG)**: Control the creativity of the models (Classifier Free Guidance). The higher the value means more likely for the model to generate an accurate image based on prompt, while lower values will make the model more creative.
- **Seed**: Set random seed to specific number for reproducibility
- **Scheduler**: Pick your prefered scheduler. Different scheduler will produce different results, some will make the image more artistic.
- **Batch**: Control the number of images you want to creae at a time (from 1 to 4).

### 2. Creative Studio
In the main menu, you'll find Creative Studio where you can experiments with prompts and also edit generated images with inpainting & outpainting. Here's the detail:
- Generate Tab
This tab will let you experiment with prompts. You can also set negative prompt to tell the model what to avoid during generation. Once you click "Initialize Generation", the model will start generating and display the images when done.
- Edit Tab
Edit tab will let you pick between inpainting or outpainting feature to enhance or change your image. Here's the detail:
    - inpainting: Where you can edit some objects in your images for example changing the color of an object or add new object. First you need to draw a mask, make prompt, then generate
    - Outpainting: Where you can expand the image based on given prompt.

## Demo Video
<video controls width="640">
  <source src="https://raw.githubusercontent.com/f4qihuddin/Image-Generation-with-Stable-Diffusion-v-1.5/main/video.mp4" type="video/mp4">
  Your browser doesn't support video player
</video>