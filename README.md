# NVIDIA Project

# Shark AI

This model classifies 14 different species of sharks as either harmful or safe to help people protect themselves in the water. It was trained on and uses the resnet18 model. The dataset originates from Kaggle, and uses an imagenet.py program to detect whether the shark generated is deadly or safe.

Running the Project

1. Download the data (https://drive.google.com/drive/folders/1dtzYjvbSpwbALeBxCDmG8ixoRy7PgoqK)
2. Install the jetson-inference library and python3 in your nano
3. Download the resnet18 model and model_best.pth.tar (obtained through unit 6 on canvas)
4. In the terminal, type "cd jetson-inference/python/training/classification
5. Establish the NET variable (NET=models/harmful_safe)
6. Establish the DATASET variable (DATASET=data/harmful_safe)
7. Process an image with this command: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels $DATASET/test/Safe/shark3.jpg shark.jpg
8. Open the file labeled "shark.jpg" and view the result.
